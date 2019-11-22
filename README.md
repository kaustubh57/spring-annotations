# Sprint Annotations

## Class Level
- @Component
- [@Scope](#bean-scope)(*value* = ConfigurableBeanFactory.SCOPE_PROTOTYPE, *proxyMode* = ScopedProxyMode.TARGET_CLASS)
- @Primary
- @Qualifier
- @Service
- @Repository
- @Configuration
- @ComponentScan(basePackage = {"com.your.package.name"})
- @Controller
- @Import(ObjectName.class)
- @PropertySource("classpath:/application.properties")

## Method Level
- @Bean
- [@Scope](#bean-scope)("singelton *or* prototype *or* session *or* request")
- @Value("${property.key.from.property.file}")
- @Profile("example-dev-or-prod")

## Variable / Constructor
- @Autowired
- @Qualifier

## Run configurations (set as environment variable)
- spring.profiles.active

## Spring Expression Languate (SpEL)
- @PropertySource("classpath:/application-${spring.profiles.active}.properties")
	- Here you can set `spring.profiles.active` value to dev / prod / stage etc
- @Value("#{new Boolean(environment['spring.profiles.active']=='dev')}")
	- Based on spring expression it will determine value for the variable

## <a name="bean-scope"></a>Bean Scope
- singleton (default) - One instance per Spring Context
- prototype - New bean whenever requested
- request - Once bean per HTTP request
- session - One bean per HTTP session

## CDI: context and dependency injection (javax.inject)
```
  <dependency>
    <groupId>javax.inject</groupId>
    <artifactId>javax.inject</artifactId>
    <version>1</version>
  </dependency>
```
- @Inject
- @Named
- @Provider
- @Qualifier
- @Scope
- @Singleton

<hr>
