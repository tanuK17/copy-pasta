None selected

Skip to content
Using Gmail with screen readers
10 of 16,115
Steps for DB creation
Inbox

Ilhan Gelle <ilhgelle@gmail.com>
Attachments
3:21 PM (4 hours ago)
to me

Below you will find the steps for creating the Database for the team:

The only thing I will mention here is that this needs to be changed to the Finalized schema, I am adding that PR right now and removing initial schema files so, the right tables get created. 

Another thing is that the password setting is tricky because we had it in the env but he said you could just expose the password in dockercompose.
 One attachment
  •  Scanned by Gmail



# Setting up a shared team database

We're currently blocked from using Supabase/Neon, and `docker compose up` gives
every developer their own private, disposable Postgres instance (each person's
`db_data` volume lives only on their own machine — nobody sees anyone else's
data). This guide sets up **one** Postgres instance on a VM that the whole
team connects to, so everyone reads and writes the same database.

This is meant for **manual/shared testing**, not automated test suites —
concurrent automated tests writing to a shared DB will collide with each
other's data (e.g. two people registering the same test email at once). Keep
using local `docker compose up` for automated tests; use the shared DB for
exploring data together / manual QA.

## Prerequisites

- A VM you control, with Docker and Docker Compose installed.
- The VM's disk must persist across restarts (rebooting the VM is fine;
  a VM that gets destroyed and rebuilt from scratch each time will lose the
  data — check this with whoever provisioned it before proceeding).
- Ability to open an inbound firewall rule on the VM (Security Group on AWS,
  NSG on Azure, firewall rules on GCP/DigitalOcean, etc).

## 1. Get the repo onto the VM

```bash
git clone <repo-url>
cd lil-leap
```

## 2. Create the `.env` file with real secrets

The repo's `.env` is currently empty — `docker-compose.yml` reads
`DB_PASSWORD` and `DB_APP_PASSWORD` from it. On the VM, set real values:

```bash
cat > .env <<'EOF'
DB_PASSWORD=<choose a strong password>
DB_APP_PASSWORD=<choose a different strong password>
EOF
```

Do **not** commit this file. Share these two passwords with the team over a
secure channel (password manager / DM), not in Slack/email in plaintext.

## 3. Start only the database service

We only need Postgres running centrally — each teammate still runs their own
backend locally, pointed at this shared DB.

```bash
docker compose up -d db
```

This runs `db/initial-schema.sql` and `db/init-app-role.sh` once, against the
empty volume, creating the schema and the restricted `app_user` role.

The `db` service already has `restart: unless-stopped` set in
`docker-compose.yml`, so if the VM stops and restarts, the container comes
back up on its own — no need to manually run `docker compose up` again.

## 4. Open the firewall for port 5432

Allow inbound TCP 5432 **only from team IPs or a VPN — not the open
internet**. Postgres exposed publicly with just a password is a real
security risk.

- **AWS**: edit the EC2 instance's Security Group → add an inbound rule,
  type Postgres (5432), source = your team's IP range or a VPN's security
  group — not `0.0.0.0/0`.
- **Azure**: edit the VM's Network Security Group → add an inbound rule for
  port 5432, restricted to your team's IP range.
- **GCP**: create a firewall rule for tcp:5432, restricted by source IP
  range, and apply it to the VM's network tag.
- **Other/on-prem**: use `ufw`/`iptables` to allow 5432 only from known IPs.

If your team's IPs change often, prefer setting up a VPN or SSH tunnel to the
VM instead of an IP allowlist.

## 5. Verify it's reachable

From your own machine (not the VM):

```bash
psql "postgresql://app_user:<DB_APP_PASSWORD>@<vm-ip-or-hostname>:5432/nexttrade" -c '\dt'
```

You should see the list of tables from `initial-schema.sql`.

## 6. Give the team the connection details

Send each teammate:

- Host: `<vm-ip-or-hostname>`
- Port: `5432`
- Database: `nexttrade`
- User: `app_user`
- Password: `<DB_APP_PASSWORD>`

## 7. Each teammate points their local backend at the shared DB

Instead of running the full `docker compose up` (which starts a local `db`
too), each person runs only their own `app` locally and overrides the
datasource to point at the VM:

```bash
export SPRING_DATASOURCE_URL=jdbc:postgresql://<vm-ip-or-hostname>:5432/nexttrade
export SPRING_DATASOURCE_USERNAME=app_user
export SPRING_DATASOURCE_PASSWORD=<DB_APP_PASSWORD>

cd backend
./mvnw spring-boot:run
```

Now everyone's backend talks to the same tables — if a teammate registers a
user or adds data, you'll see it immediately when you query the same tables.

## Notes / gotchas

- `initial-schema.sql` and `init-app-role.sh` only run on the **first**
  startup against an empty volume. If the schema changes later, migrations
  need to be applied manually against the shared DB (`docker compose down -v`
  would wipe everyone's shared data — don't run that against the shared VM
  without warning the team first).
- `app_user` intentionally cannot run `CREATE`/`DROP`/`ALTER` (see
  `db/init-app-role.sh`) — schema changes must be run as the `main`
  (`POSTGRES_USER`) role.
shared-db-setup.md
Displaying shared-db-setup.md.
