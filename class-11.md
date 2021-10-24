# Serving Web Content with Spring MVC

##  creating a “Hello, World” web site with Spring :

+ **What we Need :**

  + text editor or IDE.
  + JDK 1.8 or later
  + Gradle 4+ or Maven 3.2+
  + Spring Tool Suite (STS)


+ **Create a Web Controller :**


 ![](https://slidetodoc.com/presentation_image_h/76f745d07f32c5327bb18161261d0b50/image-4.jpg)

 + **Spring Boot Devtools :**

   1- Enables hot swapping.

   2- Switches template engines to disable caching.

   3- Enables LiveReload to automatically refresh the browser.

   4- Other reasonable defaults based on development instead of production.

+ **Run the Application :**

  
  + The Spring Initializr creates an application class for you. In this case, you need not further modify the class provided by the Spring Initializr.

  + The main() method uses Spring Boot’s SpringApplication.run() method to launch an application.


+ **Test the Application :**

  visit http://localhost:8080/greeting, where you should see “Hello, World!”

## Spring MVC and Thymeleaf: how to access data from templates :

1- Spring model attributes :
There are several ways of adding model attributes to a view in Spring MVC. Below you will find some common cases:

- Add attribute to Model via its addAttribute method
- Return ModelAndView with model attributes included
- Expose common attributes via methods annotated with @ModelAttribute

![](https://slidetodoc.com/presentation_image/70edb71b8b5877c8187c05f8049a0461/image-6.jpg)

2-Request parameters :
Request parameters can be easily accessed in Thymeleaf views. Request parameters are passed from the client to server like:

    https://example.com/query?q=Thymeleaf+Is+Great!


3- Session attributes :
In the below example we add mySessionAttribute to session:

    @RequestMapping({"/"})
        String index(HttpSession session) {
            session.setAttribute("mySessionAttribute", "someValue");
            return "index";
        }

4- ServletContext attributes :
The ServletContext attributes are shared between requests and sessions. In order to access ServletContext attributes in Thymeleaf you can use the **#servletContext**.

5- Spring beans :
Thymeleaf allows accessing beans registered at the Spring Application Context with the @beanName syntax, for example:

    <div th:text="${@urlService.getApplicationUrl()}">...</div> 