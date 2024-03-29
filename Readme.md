# attendance management application
## Description
This application automates recording monthly attendances for [Slack](https://slack.com/) and [Freee](https://www.freee.co.jp/hr/) User.


![architecture](image/architecture.png)


## Stack
- Kotlin
- Spring Boot
- TypeScript
- React
- PostgreSQL
- jooq
- liquibase
- openapi-generator
- Docker

## set up
### create application.properties
```
cd api/src/main/resources/
touch application.properties
```
application.properties needs following properties.
```
spring.datasource.url=jdbc:postgresql://db:5432/db
spring.datasource.username=root
spring.datasource.password=root
spring.datasource.driver-class-name=org.postgresql.Driver
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect
spring.liquibase.change-log=classpath:liquibase/changelog.xml
slack.token=
freee.clientId=
freee.clientSecret=
```

### initialize application & start application
```
$ make initialize
```

### start application
```
$ make start
```

### stop application
```
$ make stop
```
