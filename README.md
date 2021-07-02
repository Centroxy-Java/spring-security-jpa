# spring-security-jpa
Code for full Spring Security + JPA + MySQL tutorial:  https://youtu.be/TNt3GHuayXs

# Written By

Biswajit Pradhan

# Spring Security

###### Spring Security provides security services for the Spring IO Platform. Spring Security 5.0 requires Spring 5.0 as a minimum and also requires Java 8.

###### For a detailed list of features and access to the latest release, please visit Spring projects.

# Downloading Artifacts

###### See [Getting Spring Security](https://docs.spring.io/spring-security/site/docs/current/reference/html5/#getting) for how to obtain Spring Security.

# Flow of the Project

###### Create a Spring starter project.

###### Choose your Artifacts

       - Spring Security
       - Spring data jpa
       - spring mysql connector
       - spring web
       
###### Create a class extends from WebSecurityConfigurerAdapter `public class SecurityConfiguration extends WebSecurityConfigurerAdapter`

###### Override `protected void configure(AuthenticationManagerBuilder auth) throws Exception` for the Authentication and 

###### Create a entity class and also create Repository interface extends from JpaRepository. 

###### Override `protected void configure(HttpSecurity http) throws Exception` for the Authorization

###### call `auth.userDetailsService(userDetailsService);` to check a user is a valid user or not.

###### Create a class extends from `userDetailsService` and override  `public UserDetails loadUserByUsername(String userName)` method.



![image](https://user-images.githubusercontent.com/80092355/124269609-b7ab6480-db58-11eb-85be-98e28339dde9.png)


###### Call  findByUserName(String userName) to check the credentials and it returns a Optional.

## Authorization(Role Base Access)

![image](https://user-images.githubusercontent.com/80092355/124270408-cba39600-db59-11eb-9cf2-76fccb1fa3f7.png)

###### Authorize a user to a particular page according to his role. 

# Development server

Click on `Run as spring boot app` . Navigate to `http://localhost:8080/`. The app will automatically reload if you change any of the source files.


# Build and Deploy the Project

 - mvn clean install

This is a Spring Boot project, so you can deploy it by simply using the main class: `Application.java`


