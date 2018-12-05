# Spring Security Login Tutorial

Tutorial / Full Information
https://medium.com/@gustavo.ponce.ch/spring-boot-spring-mvc-spring-security-mysql-a5d8545d837d

prepare: change the database information

1. mvn clean
2. mvn clean install
3. Go to the target folder
4. java -jar login-0.0.1-SNAPSHOT.jar


- http://localhost:8080/registration
- http://localhost:8080/login

# Learned

1. Hibernate validator
- Html(Thymeleaf): th:if="${#fields.hasErrors('name')}" 
- Bean: @NotEmpty/@NotNull
- Controller: bindingResult/@Valid
2. Thymeleaf
3. BCryptPasswordEncoder
- configure()
4. Key thing: 
- AuthenticationFailureHandler
- SecurityContextHolder



# Question
1. If I change .antMatchers("/admin/**").hasAuthority("ADMIN").anyRequest() can reject user access home.html?
- yes
- 1.1 If anthentication failed, how to indicate the "error page"? 
- 1.2 Like AuthenticationFailureHandler, is there AuthorizationFailureHandler?

2. Some important method's detail and trace the related fragment:
- jdbcAuthentication()
- authorizeRequests()

3. relationship: 
- AuthenticationManager and AuthenticationManagerBuilder?

4. @Autowired:
- private UserService userService; How to inject this bean?