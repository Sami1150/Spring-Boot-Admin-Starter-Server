# Spring-Boot-Admin-Starter-Server
This repository is configured and only needs to be run to see analytics of the actuator on port 8081 (Which can be configured). 
Add the following dependency to your project:

		<dependency>
			<groupId>de.codecentric</groupId>
			<artifactId>spring-boot-admin-starter-client</artifactId>
		</dependency>

Add the following properties in your application.properties or application.yaml

<code>
  management:
  endpoints:
    web:
      exposure:
        include: '*'
  endpoint:
    health:
      show-details: always
springdoc:
  show-login-endpoint: true
</code>
<br/>
And
<br/>

<code>
  
  spring:
      boot:
        admin:
          client:
            url: http://localhost:8081
            enabled: true
            auto-registeration: true
</code>
