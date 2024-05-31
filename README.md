# Spring-Boot-Oracle-Connect
A Spring Boot sample application that connects to an Oracle database.
This was built with Spring Boot v.3.2.5 and Spring Security v.6.0 (Requires Java 17).

This sample application builds on top of the [Spring-Boot-Simple-Login demo application](https://github.com/salvadorvp/Spring-Boot-Simple-Login)

You need to update the `application.properties` file to change the following properties:
- spring.datasource.url=jdbc:oracle:thin:@//example.com:1521/SID
- spring.datasource.username=usernm
- spring.datasource.password=pass

The files `EndUserController.java` and `EndUser.java` have the Spring configuration/annotations for reading the EndUser database (Oracle) table and converting the data to instances of the EndUser class.

The POM file needs these two dependencies at a minimum:
```
		<!-- Database libraries -->
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-data-jpa</artifactId>
		</dependency>
		<dependency>
			<groupId>com.oracle.database.jdbc</groupId>
			<artifactId>ojdbc8</artifactId>
			<version>19.8.0.0</version>
		</dependency>
```



Sample output of reading the EndUser table:
![Sample output of reading the EndUser table](enduserlist.png)
