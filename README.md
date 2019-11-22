# Sprint Annotations

## Class Level
- @Configuration
- @Import(ObjectName.class)
- @PropertySource("classpath:/application.properties")
- @ComponentScan(basePackage = {"com.your.package.name"})
- @Component
- [@Scope](#bean-scope)(*value* = ConfigurableBeanFactory.SCOPE_PROTOTYPE, *proxyMode* = ScopedProxyMode.TARGET_CLASS)
- @Primary
- @Qualifier
- @Service
- @Repository

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

<hr>

# <a name="bean-scope"></a>Bean Scope
- singleton (default) - One instance per Spring Context
- prototype - New bean whenever requested
- request - Once bean per HTTP request
- session - One bean per HTTP session

<hr>

### *Check this*
- @Service
- @Component
