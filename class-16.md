# Spring Authentication

+ **authentication :**  who are you?

+ **authorization :** what are you allowed to do?

+ The main strategy interface for authentication is **AuthenticationManager**

+ An AuthenticationManager can do one of **3 things** in its authenticate() method:

  1- Return an Authentication if it can verify that the input represents a valid principal.

  2- Throw an AuthenticationException if it believes that the input represents an invalid principal.

  3- Return null if it cannot decide.

+ Spring Security provides some configuration helpers to quickly get common authentication manager features set up in your application. The most commonly used helper is the **AuthenticationManagerBuilder**.

+ Once authentication is successful, we move on to authorization, and the core strategy here is AccessDecisionManager. There are 3 implementations provided  to a chain of **AccessDecisionVoter** instances .



## Web Security

Spring Securityis based on **Servlet Filters**, so it is helpful to first look at the role of Filters generally. The following picture shows the typical layering of the handlers for a single HTTP request.

![](https://miro.medium.com/max/941/1*JScorB4xO9feqZuaYTtBXg.png)

+ Creating and Customizing Filter Chains :
The default fallback filter chain in a Spring Boot application (the one with the /** request matcher) has a predefined order of **SecurityProperties.BASIC_AUTH_ORDER**.


+ **Method Security** :
Spring Security offers support for applying access rules to Java method executions. For Spring Security, this is just a different type of “protected resource”.


+ **Working with Threads** :
Spring Security is fundamentally thread-bound, because it needs to make the current authenticated principal available to a wide variety of downstream consumers. 

  The basic building block is the SecurityContext, which may contain an Authentication (and when a user is logged in it is an Authentication that is explicitly authenticated).