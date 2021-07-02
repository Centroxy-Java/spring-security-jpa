# spring-security-jpa
Code for full Spring Security + JPA + MySQL tutorial:  https://youtu.be/TNt3GHuayXs


#Spring Security
###### Spring Security provides security services for the Spring IO Platform. Spring Security 5.0 requires Spring 5.0 as a minimum and also requires Java 8.
###### For a detailed list of features and access to the latest release, please visit Spring projects.

#Downloading Artifacts
###### See [Getting Spring Security](https://docs.spring.io/spring-security/site/docs/current/reference/html5/#getting) for how to obtain Spring Security.

#Procedure
###### Create a Spring starter project.
###### Choose your Artifacts
       - Spring Security
       - Spring data jpa
       - spring mysql connector
       - spring web
###### Create a class extends from WebSecurityConfigurerAdapter `public class SecurityConfiguration extends WebSecurityConfigurerAdapter`
###### Override `protected void configure(AuthenticationManagerBuilder auth) throws Exception` for the Authentication and 
###### Override `protected void configure(HttpSecurity http) throws Exception` for the Authorization
###### call `auth.userDetailsService(userDetailsService);` to check a user is a valid user or not.
###### Create a class extends from `userDetailsService` and override `public UserDetails loadUserByUsername(String userName) throws UsernameNotFoundException` method.
## Flow of the Project
###### 
