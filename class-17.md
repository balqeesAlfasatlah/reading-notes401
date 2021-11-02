
# Spring Boot and OAuth2

###  how to build a sample app doing various things with "social login" using OAuth 2.0 and Spring Boot:

+ There are several samples building on each other, adding new features at each step:

  1- simple: a very basic static app with just a home page and unconditional login via Spring Boot’s OAuth 2.0 configuration properties

  2- click: adds an explicit link that the user has to click to login.

  3- logout: adds a logout link as well for authenticated users.

  4- two-providers: adds a second login provider so the user can choose on the home page which one to use.

  5- custom-error: adds an error message for unauthenticated users, and a custom authentication based on GitHub’s API.

+ Securing the Application with GitHub and Spring Security :

  To make the application secure, you can simply add Spring Security as a dependency. 

+ The /user Endpoint :
add the server-side endpoint calling it /user. It will send back the currently logged-in user, which we can do quite easily in our main :

@SpringBootApplication
@RestController
public class SocialApplication {

    @GetMapping("/user")
    public Map<String, Object> user(@AuthenticationPrincipal OAuth2User principal) {
        return Collections.singletonMap("name", principal.getAttribute("name"));
    }

    public static void main(String[] args) {
        SpringApplication.run(SocialApplication.class, args);
    }

}


+ Client Side Changes :
On the client, we just need to provide a logout button  call back to the server to ask for the authentication to be cancelled and then we provide the logout() function :

var logout = function() {
    $.post("/logout", function() {
        $("#user").html('');
        $(".unauthenticated").show();
        $(".authenticated").hide();
    })
    return true;
}

+ The logout() function does a POST to /logout and then clears the dynamic content


+ Adding a Logout Endpoint :
Spring Security has built in support for a /logout endpoint which will do the right thing for us .To configure the endpoint we simply extend the existing configure() method in our WebSecurityConfigurerAdapter:

@Override
protected void configure(HttpSecurity http) throws Exception {
	// @formatter:off
    http
        // ... existing code here
        .logout(l -> l
            .logoutSuccessUrl("/").permitAll()
        )
        // ... existing code here
    // @formatter:on
}