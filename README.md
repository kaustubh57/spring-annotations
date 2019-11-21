# Sprint Annotations

## Class Level
- @Configuration
- @Import(ObjectName.class)
- @PropertySource("classpath:/application.properties")
- @ComponentScan(basePackage = {"com.your.package.name"})
- @Component
- @Primary
- @Qualifier
- @Service
- @Repository

## Method Level
- [@Bean](#bean-scope)
- @Scope("singelton *or* prototype *or* session *or* request")
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

# Bean Scone
- singleton
- prototype
- request
- session

<hr>

### *Check this*
- @Service
- @Component
