# ex7-springBoot-jpa-rest-mvc
Example Spring Boot MVC (Model View Controller) project using;
+ thymeleaf templates for view ov MVC
+ Data JPA as ORM (Object Relational Mapping) to interact with persistence
+ H2 or MySQL as DB (RDBMS)
+ MVC serving UI
+ MVC Rest serving REST Services
+ DevTool for automatic restart of app upon code changes
+ Bootstrap for styles and layout (CSS and some JS) of UI
+ jQuery for dynamic UI
+ Webjars for UI (JS and CSS) dependencies like Bootstrap and jQuery in jar dependencies

## To see it's UI running
+ start the app
+ access it's UI via browser at
http://localhost:8888/mvc/student/echoMessage
http://localhost:8888/mvc/student/echoMessage?msg=Yahooo
http://localhost:8888/mvc/student/list

## To startup postman or ARC(Advanced Rest Client)
+ open chrome browser, in url enter 
chrome://apps/
+ double click on Postman or ARC

## To see it's REST services running
+ start the app
+ access it's REST services via a REST client tool like postman, Advanced Rest Client (ARC) or even just a browser (for GET ones);
http://localhost:8888/rest/v1/students/echoMessage?msg=Hi			GET
http://localhost:8888/rest/v1/students								GET
http://localhost:8888/rest/v1/students/all							GET
http://localhost:8888/rest/v1/students								POST to create

## To access h2 db console with browser
+ start the app
+ make sure app is not protected with spring security (it is not a dependency in pom.xml). Because /h2-console will be protected by Spring security as well, if it is on
+ access the h2 db console (assuming app started at port 8888) with a browser,
 just click "Connect" leaving; 
 Driver Class: org.h2.Driver, 
 JDBC URL: jdbc:h2:mem:testdb, 
 User Name: sa, 
 Password:         leave it empty

http://localhost:8888/h2-console

## To create the project in STS
1. File -> New -> Spring Starter Project
  - Name: exp7-springBoot-mvc-thymeleaf-student
  - Packaging: Jar
  - Group: ex7.sb.mvc.thymeleaf
  - Artifact: student
  - Package: ex7.sb.mvc.thymeleaf.student
2. click Next
  * Boot Version: 2.0.1
  * (click at least, Web, Thymeleaf, JPA, H2, DevTools)
  * click Web -> Web
  * click Template Engines -> Thymeleaf
  * click SQL -> JPA, JDBC, MySQL, H2
  * click Core -> DevTools, Lombok
  * click Ops -> Actuator
3. click Finish
## To automatically populate h2 db
+ add bunch of insert statements in data.sql (or data-h2.sql or both) file in src/main/resources

## To create view file
+ right click on src/main/resources/templates , click New, select Web -> Html File -> Html5
+ then start sprinkling thymeleaf tags into the html
+ then pass data from controller to UI's view via model.addAttribute method

TEST
