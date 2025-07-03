# Spring.io, Websockets y ReactJs

## Author: David Alfonso Barbosa Gómez

1. After creating the basic structure of the project, it is necessary to update the pom.xml file with the following dependencies.
  ```
  <dependencies>
   <dependency>
     <groupId>org.springframework.boot</groupId>
     <artifactId>spring-boot-starter-web</artifactId>
     <version>2.3.1.RELEASE</version>
   </dependency>
  </dependencies>
  ```
2. Create the main Spring Boot application class.
  ```
  package co.edu.escuelaing.websocketsprimer;
  import org.springframework.boot.SpringApplication;
  import org.springframework.boot.autoconfigure.SpringBootApplication;
  @SpringBootApplication
  public class WSStartApp {
   
   public static void main(String[] args){
   SpringApplication.run(WSStartApp.class, args);
   }
  }
  ```
3. Create a web controller that loads the minimum Web MVC settings.
  ```
    package co.edu.escuelaing.websocketsprimer;
    import org.springframework.web.bind.annotation.GetMapping;
    import org.springframework.web.bind.annotation.RestController;
    @RestController
    public class WebController {
     
     @GetMapping("/status")
     public String status() {
     return "{\"status\":\"Greetings from Spring Boot "
     + java.time.LocalDate.now() + ", "
     + java.time.LocalTime.now()
     + ". " + "The server is Runnig!\"}";
     }
    }
  ```
4. Create an html index in this location: **/src/main/resources/static**

5. Run the class we just created, and the server should start executing.
6. Verify the execution accessing to> **localhost:8080/index.html**


