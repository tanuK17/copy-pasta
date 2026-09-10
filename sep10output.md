Administrator@EC2AMAZ-64EBKCO MINGW64 ~/lil-leap (feature/database-hardening)
$ cat backend/src/test/resources/mockito-extensions/org.mockito.plugins.MockMaker
cat: backend/src/test/resources/mockito-extensions/org.mockito.plugins.MockMaker: No such file or directory

Administrator@EC2AMAZ-64EBKCO MINGW64 ~/lil-leap (feature/database-hardening)
$ cd backend/

Administrator@EC2AMAZ-64EBKCO MINGW64 ~/lil-leap/backend (feature/database-hardening)
$ mvn clean test
WARNING: A restricted method in java.lang.System has been called
WARNING: java.lang.System::load has been called by org.fusesource.jansi.internal.JansiLoader in an unnamed module (file:/C:/ProgramData/chocolatey/lib/maven/apache-maven-3.9.9/lib/jansi-2.4.1.jar)
WARNING: Use --enable-native-access=ALL-UNNAMED to avoid a warning for callers in this module
WARNING: Restricted methods will be blocked in a future release unless native access is enabled

WARNING: A terminally deprecated method in sun.misc.Unsafe has been called
WARNING: sun.misc.Unsafe::objectFieldOffset has been called by com.google.common.util.concurrent.AbstractFuture$UnsafeAtomicHelper (file:/C:/ProgramData/chocolatey/lib/maven/apache-maven-3.9.9/lib/guava-33.2.1-jre.jar)
WARNING: Please consider reporting this to the maintainers of class com.google.common.util.concurrent.AbstractFuture$UnsafeAtomicHelper
WARNING: sun.misc.Unsafe::objectFieldOffset will be removed in a future release
[INFO] Scanning for projects...
[INFO]
[INFO] ----------------< com.neueda.leap:sprint1-greeter-app >-----------------
[INFO] Building sprint1-greeter-app 0.1.0
[INFO]   from pom.xml
[INFO] --------------------------------[ jar ]---------------------------------
[INFO]
[INFO] --- clean:3.3.2:clean (default-clean) @ sprint1-greeter-app ---
[INFO] Deleting C:\Users\Administrator\lil-leap\backend\target
[INFO]
[INFO] --- resources:3.3.1:resources (default-resources) @ sprint1-greeter-app ---
[INFO] Copying 1 resource from src\main\resources to target\classes
[INFO] Copying 0 resource from src\main\resources to target\classes
[INFO]
[INFO] --- compiler:3.13.0:compile (default-compile) @ sprint1-greeter-app ---
[INFO] Recompiling the module because of changed source code.
[INFO] Compiling 50 source files with javac [debug parameters release 17] to target\classes
[INFO]
[INFO] --- resources:3.3.1:testResources (default-testResources) @ sprint1-greeter-app ---
[INFO] Copying 1 resource from src\test\resources to target\test-classes
[INFO]
[INFO] --- compiler:3.13.0:testCompile (default-testCompile) @ sprint1-greeter-app ---
[INFO] Recompiling the module because of changed dependency.
[INFO] Compiling 9 source files with javac [debug parameters release 17] to target\test-classes
[INFO]
[INFO] --- surefire:3.2.5:test (default-test) @ sprint1-greeter-app ---
[INFO] Using auto detected provider org.apache.maven.surefire.junitplatform.JUnitPlatformProvider
[INFO]
[INFO] -------------------------------------------------------
[INFO]  T E S T S
[INFO] -------------------------------------------------------
[INFO] Running com.neueda.leap.config.SecurityConfigTest
22:24:03.851 [main] INFO org.springframework.test.context.support.AnnotationConfigContextLoaderUtils -- Could not detect default configuration classes for test class [com.neueda.leap.config.SecurityConfigTest]: SecurityConfigTest does not declare any static, non-private, non-final, nested classes annotated with @Configuration.
22:24:04.001 [main] INFO org.springframework.boot.test.context.SpringBootTestContextBootstrapper -- Found @SpringBootConfiguration com.neueda.leap.Main for test class com.neueda.leap.config.SecurityConfigTest

  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/

 :: Spring Boot ::                (v3.3.4)

22:24:04.645 [main] INFO  c.n.leap.config.SecurityConfigTest - Starting SecurityConfigTest using Java 25.0.3 with PID 13624 (started by Administrator in C:\Users\Administrator\lil-leap\backend)
22:24:04.648 [main] INFO  c.n.leap.config.SecurityConfigTest - No active profile set, falling back to 1 default profile: "default"
22:24:06.059 [main] WARN  o.s.b.a.s.s.UserDetailsServiceAutoConfiguration -

Using generated security password: 63b7de7e-21af-4c06-adc8-f0c1081de56a

This generated password is for development use only. Your security configuration must be updated before running your application in production.

22:24:06.068 [main] INFO  o.s.s.c.a.a.c.InitializeUserDetailsBeanManagerConfigurer$InitializeUserDetailsManagerConfigurer - Global AuthenticationManager configured with UserDetailsService bean with name inMemoryUserDetailsManager
22:24:06.675 [main] INFO  o.s.b.t.m.w.SpringBootMockServletContext - Initializing Spring TestDispatcherServlet ''
22:24:06.675 [main] INFO  o.s.t.w.s.TestDispatcherServlet - Initializing Servlet ''
22:24:06.677 [main] INFO  o.s.t.w.s.TestDispatcherServlet - Completed initialization in 0 ms
22:24:06.701 [main] INFO  c.n.leap.config.SecurityConfigTest - Started SecurityConfigTest in 2.639 seconds (process running for 3.731)
[INFO] Tests run: 2, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 3.288 s -- in com.neueda.leap.config.SecurityConfigTest
[INFO] Running com.neueda.leap.onboarding.RegistrationControllerTest
22:24:07.007 [main] INFO  o.s.t.c.s.AnnotationConfigContextLoaderUtils - Could not detect default configuration classes for test class [com.neueda.leap.onboarding.RegistrationControllerTest]: RegistrationControllerTest does not declare any static, non-private, non-final, nested classes annotated with @Configuration.
22:24:07.072 [main] INFO  o.s.b.t.c.SpringBootTestContextBootstrapper - Found @SpringBootConfiguration com.neueda.leap.Main for test class com.neueda.leap.onboarding.RegistrationControllerTest

  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/

 :: Spring Boot ::                (v3.3.4)

22:24:07.120 [main] INFO  c.n.l.o.RegistrationControllerTest - Starting RegistrationControllerTest using Java 25.0.3 with PID 13624 (started by Administrator in C:\Users\Administrator\lil-leap\backend)
22:24:07.120 [main] INFO  c.n.l.o.RegistrationControllerTest - No active profile set, falling back to 1 default profile: "default"
22:24:07.437 [main] WARN  o.s.b.a.s.s.UserDetailsServiceAutoConfiguration -

Using generated security password: 32b075f2-e5ed-4a95-a02e-a651ef1c26ab

This generated password is for development use only. Your security configuration must be updated before running your application in production.

22:24:07.439 [main] INFO  o.s.s.c.a.a.c.InitializeUserDetailsBeanManagerConfigurer$InitializeUserDetailsManagerConfigurer - Global AuthenticationManager configured with UserDetailsService bean with name inMemoryUserDetailsManager
22:24:07.462 [main] INFO  o.s.b.t.m.w.SpringBootMockServletContext - Initializing Spring TestDispatcherServlet ''
22:24:07.462 [main] INFO  o.s.t.w.s.TestDispatcherServlet - Initializing Servlet ''
22:24:07.463 [main] INFO  o.s.t.w.s.TestDispatcherServlet - Completed initialization in 1 ms
22:24:07.471 [main] INFO  c.n.l.o.RegistrationControllerTest - Started RegistrationControllerTest in 0.395 seconds (process running for 4.5)
22:24:07.793 [main] WARN  o.s.w.s.m.s.DefaultHandlerExceptionResolver - Resolved [org.springframework.web.bind.MethodArgumentNotValidException: Validation failed for argument [0] in public org.springframework.http.ResponseEntity<com.neueda.leap.onboarding.dto.UserResponse> com.neueda.leap.onboarding.controller.RegistrationController.register(com.neueda.leap.onboarding.dto.RegisterUserRequest): [Field error in object 'registerUserRequest' on field 'password': rejected value [123]; codes [Size.registerUserRequest.password,Size.password,Size.java.lang.String,Size]; arguments [org.springframework.context.support.DefaultMessageSourceResolvable: codes [registerUserRequest.password,password]; arguments []; default message [password],128,8]; default message [size must be between 8 and 128]] ]
22:24:07.880 [main] WARN  o.s.w.s.m.s.DefaultHandlerExceptionResolver - Resolved [org.springframework.web.bind.MethodArgumentNotValidException: Validation failed for argument [0] in public org.springframework.http.ResponseEntity<com.neueda.leap.onboarding.dto.UserResponse> com.neueda.leap.onboarding.controller.RegistrationController.register(com.neueda.leap.onboarding.dto.RegisterUserRequest): [Field error in object 'registerUserRequest' on field 'email': rejected value [not-an-email]; codes [Email.registerUserRequest.email,Email.email,Email.java.lang.String,Email]; arguments [org.springframework.context.support.DefaultMessageSourceResolvable: codes [registerUserRequest.email,email]; arguments []; default message [email],[Ljakarta.validation.constraints.Pattern$Flag;@4a3509b0,.*]; default message [must be a well-formed email address]] ]
22:24:07.888 [main] WARN  o.s.w.s.m.s.DefaultHandlerExceptionResolver - Resolved [org.springframework.web.bind.MethodArgumentNotValidException: Validation failed for argument [0] in public org.springframework.http.ResponseEntity<com.neueda.leap.onboarding.dto.UserResponse> com.neueda.leap.onboarding.controller.RegistrationController.register(com.neueda.leap.onboarding.dto.RegisterUserRequest): [Field error in object 'registerUserRequest' on field 'firstName': rejected value []; codes [NotBlank.registerUserRequest.firstName,NotBlank.firstName,NotBlank.java.lang.String,NotBlank]; arguments [org.springframework.context.support.DefaultMessageSourceResolvable: codes [registerUserRequest.firstName,firstName]; arguments []; default message [firstName]]; default message [must not be blank]] ]
[INFO] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.944 s -- in com.neueda.leap.onboarding.RegistrationControllerTest
[INFO] Running com.neueda.leap.onboarding.RegistrationServiceTest
[INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.242 s -- in com.neueda.leap.onboarding.RegistrationServiceTest
[INFO] Running com.neueda.leap.security.JwtAuthenticationFilterTest
[INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.047 s -- in com.neueda.leap.security.JwtAuthenticationFilterTest
[INFO] Running com.neueda.leap.security.JwtServiceTest
[INFO] Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.017 s -- in com.neueda.leap.security.JwtServiceTest
[INFO] Running com.neueda.leap.user.AuthControllerTest
22:24:08.262 [main] INFO  o.s.t.c.s.AnnotationConfigContextLoaderUtils - Could not detect default configuration classes for test class [com.neueda.leap.user.AuthControllerTest]: AuthControllerTest does not declare any static, non-private, non-final, nested classes annotated with @Configuration.
22:24:08.332 [main] INFO  o.s.b.t.c.SpringBootTestContextBootstrapper - Found @SpringBootConfiguration com.neueda.leap.Main for test class com.neueda.leap.user.AuthControllerTest

  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/

 :: Spring Boot ::                (v3.3.4)

22:24:08.397 [main] INFO  c.n.leap.user.AuthControllerTest - Starting AuthControllerTest using Java 25.0.3 with PID 13624 (started by Administrator in C:\Users\Administrator\lil-leap\backend)
22:24:08.398 [main] INFO  c.n.leap.user.AuthControllerTest - No active profile set, falling back to 1 default profile: "default"
22:24:08.670 [main] WARN  o.s.b.a.s.s.UserDetailsServiceAutoConfiguration -

Using generated security password: 26143b4b-a0ed-4e30-a1f6-876d55ab2bb3

This generated password is for development use only. Your security configuration must be updated before running your application in production.

22:24:08.671 [main] INFO  o.s.s.c.a.a.c.InitializeUserDetailsBeanManagerConfigurer$InitializeUserDetailsManagerConfigurer - Global AuthenticationManager configured with UserDetailsService bean with name inMemoryUserDetailsManager
22:24:08.678 [main] INFO  o.s.b.t.m.w.SpringBootMockServletContext - Initializing Spring TestDispatcherServlet ''
22:24:08.679 [main] INFO  o.s.t.w.s.TestDispatcherServlet - Initializing Servlet ''
22:24:08.679 [main] INFO  o.s.t.w.s.TestDispatcherServlet - Completed initialization in 0 ms
22:24:08.684 [main] INFO  c.n.leap.user.AuthControllerTest - Started AuthControllerTest in 0.327 seconds (process running for 5.713)
22:24:08.719 [main] WARN  o.s.w.s.m.s.DefaultHandlerExceptionResolver - Resolved [org.springframework.web.bind.MethodArgumentNotValidException: Validation failed for argument [0] in public org.springframework.http.ResponseEntity<com.neueda.leap.user.dto.LoginResponse> com.neueda.leap.user.AuthController.login(com.neueda.leap.user.dto.LoginRequest): [Field error in object 'loginRequest' on field 'email': rejected value []; codes [NotBlank.loginRequest.email,NotBlank.email,NotBlank.java.lang.String,NotBlank]; arguments [org.springframework.context.support.DefaultMessageSourceResolvable: codes [loginRequest.email,email]; arguments []; default message [email]]; default message [must not be blank]] ]
[INFO] Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.494 s -- in com.neueda.leap.user.AuthControllerTest
[INFO] Running com.neueda.leap.user.AuthenticationFlowTest
22:24:08.754 [main] INFO  o.s.t.c.s.AnnotationConfigContextLoaderUtils - Could not detect default configuration classes for test class [com.neueda.leap.user.AuthenticationFlowTest]: AuthenticationFlowTest does not declare any static, non-private, non-final, nested classes annotated with @Configuration.
22:24:08.762 [main] INFO  o.s.b.t.c.SpringBootTestContextBootstrapper - Found @SpringBootConfiguration com.neueda.leap.Main for test class com.neueda.leap.user.AuthenticationFlowTest

  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/

 :: Spring Boot ::                (v3.3.4)

22:24:08.795 [main] INFO  c.n.leap.user.AuthenticationFlowTest - Starting AuthenticationFlowTest using Java 25.0.3 with PID 13624 (started by Administrator in C:\Users\Administrator\lil-leap\backend)
22:24:08.795 [main] INFO  c.n.leap.user.AuthenticationFlowTest - No active profile set, falling back to 1 default profile: "default"
22:24:08.977 [main] WARN  o.s.b.a.s.s.UserDetailsServiceAutoConfiguration -

Using generated security password: bef009a1-2f9b-4e0d-a3b2-22dc107bec3e

This generated password is for development use only. Your security configuration must be updated before running your application in production.

22:24:08.981 [main] INFO  o.s.s.c.a.a.c.InitializeUserDetailsBeanManagerConfigurer$InitializeUserDetailsManagerConfigurer - Global AuthenticationManager configured with UserDetailsService bean with name inMemoryUserDetailsManager
22:24:09.047 [main] INFO  o.s.b.t.m.w.SpringBootMockServletContext - Initializing Spring TestDispatcherServlet ''
22:24:09.047 [main] INFO  o.s.t.w.s.TestDispatcherServlet - Initializing Servlet ''
22:24:09.047 [main] INFO  o.s.t.w.s.TestDispatcherServlet - Completed initialization in 0 ms
22:24:09.052 [main] INFO  c.n.leap.user.AuthenticationFlowTest - Started AuthenticationFlowTest in 0.285 seconds (process running for 6.081)
[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.360 s -- in com.neueda.leap.user.AuthenticationFlowTest
[INFO] Running com.neueda.leap.user.UserControllerTest
22:24:09.115 [main] INFO  o.s.t.c.s.AnnotationConfigContextLoaderUtils - Could not detect default configuration classes for test class [com.neueda.leap.user.UserControllerTest]: UserControllerTest does not declare any static, non-private, non-final, nested classes annotated with @Configuration.
22:24:09.128 [main] INFO  o.s.b.t.c.SpringBootTestContextBootstrapper - Found @SpringBootConfiguration com.neueda.leap.Main for test class com.neueda.leap.user.UserControllerTest

  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/

 :: Spring Boot ::                (v3.3.4)

22:24:09.184 [main] INFO  c.n.leap.user.UserControllerTest - Starting UserControllerTest using Java 25.0.3 with PID 13624 (started by Administrator in C:\Users\Administrator\lil-leap\backend)
22:24:09.184 [main] INFO  c.n.leap.user.UserControllerTest - No active profile set, falling back to 1 default profile: "default"
22:24:09.503 [main] WARN  o.s.b.a.s.s.UserDetailsServiceAutoConfiguration -

Using generated security password: 62dfdeb8-8b45-488b-9f58-5223d3fbf999

This generated password is for development use only. Your security configuration must be updated before running your application in production.

22:24:09.506 [main] INFO  o.s.s.c.a.a.c.InitializeUserDetailsBeanManagerConfigurer$InitializeUserDetailsManagerConfigurer - Global AuthenticationManager configured with UserDetailsService bean with name inMemoryUserDetailsManager
22:24:09.537 [main] INFO  o.s.b.t.m.w.SpringBootMockServletContext - Initializing Spring TestDispatcherServlet ''
22:24:09.565 [main] INFO  o.s.t.w.s.TestDispatcherServlet - Initializing Servlet ''
22:24:09.565 [main] INFO  o.s.t.w.s.TestDispatcherServlet - Completed initialization in 0 ms
22:24:09.609 [main] INFO  c.n.leap.user.UserControllerTest - Started UserControllerTest in 0.478 seconds (process running for 6.639)
[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.538 s -- in com.neueda.leap.user.UserControllerTest
[INFO] Running com.neueda.leap.user.UserServiceTest
[INFO] Tests run: 6, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.309 s -- in com.neueda.leap.user.UserServiceTest
[INFO]
[INFO] Results:
[INFO]
[INFO] Tests run: 29, Failures: 0, Errors: 0, Skipped: 0
[INFO]
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  13.033 s
[INFO] Finished at: 2026-09-10T22:24:10Z
[INFO] ------------------------------------------------------------------------

Administrator@EC2AMAZ-64EBKCO MINGW64 ~/lil-leap/backend (feature/database-hardening)
$
