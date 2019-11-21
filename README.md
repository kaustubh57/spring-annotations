# Sprint Annotations

## Class Level
- @Configuration
- @Import(ObjectName.class)
- @PropertySource("classpath:/application.properties")
- @ComponentScan(basePackage = {"com.your.package.name"})
- @Component
- @Primary
- @Service
- @Repository

## Method Level
- @Bean
- @Scope("singelton _or_ prototype _or_ session _or_ request")
- @Value("${property.key.from.property.file}")
- @Profile("example-dev-or-prod")

## Variable / Constructor
- @Autowired

## Run configurations (set as environment variable)
- spring.profiles.active

## Spring Expression Languate (SpEL)
- @PropertySource("classpath:/application-${spring.profiles.active}.properties")
	- Here you can set `spring.profiles.active` value to dev / prod / stage etc
- @Value("#{new Boolean(environment['spring.profiles.active']=='dev')}")
	- Based on spring expression it will determine value for the variable


<hr>
## <span style="color:blue">_Check this_</span>
- @Service
- @Component
