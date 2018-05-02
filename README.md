# Sprint Annotations

## Class Level
- @Configuration
- @Import(ObjectName.class)
- @PropertySource("classpath:/application.properties")

## Method Level
- @Bean
- @Value("${property.key.from.property.file}")
- @Profile("example-dev-or-prod")

## Run configurations (set as environment variable)
- spring.profiles.active

## Spring Expression Languate (SpEL)
- @PropertySource("classpath:/application-${spring.profiles.active}.properties")
	- Here you can set `spring.profiles.active` value to dev / prod / stage etc
- @Value("#{new Boolean(environment['spring.profiles.active']=='dev')}")
	- Based on spring expression it will determine value for the variable