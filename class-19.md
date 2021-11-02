# Using WebSocket to build an interactive web application

You will build a server that accepts a message that carries a user’s name. In response, the server will push a greeting into a queue to which the client is subscribed.

1- use this pre-initialized project and click Generate to download a ZIP file.

2- Adding Dependencies

3- Create a Resource Representation Class :

+ The service will accept messages that contain a name in a STOMP message whose body is a JSON object. If the name is Fred, the message might resemble the following:

  {
    "name": "Fred"
  }

+ To model the message that carries the name, you can create a plain old Java object with a name property and a corresponding getName() method:
---

package com.example.messagingstompwebsocket;

public class HelloMessage {

  private String name;
  public HelloMessage() {
  }

  public HelloMessage(String name) {
    this.name = name;
  }

  public String getName() {
    return name;
  }

  public void setName(String name) {
    this.name = name;
  }
}

---
4- Create a Message-handling Controller :
In Spring’s approach to working with STOMP messaging, STOMP messages can be routed to @Controller classes. 

5- Configure Spring for STOMP messaging : configure Spring to enable WebSocket and STOMP messaging 

  + Create a Java class named WebSocketConfig :
---
  package com.example.messagingstompwebsocket;

import org.springframework.context.annotation.Configuration;
import org.springframework.messaging.simp.config.MessageBrokerRegistry;
import org.springframework.web.socket.config.annotation.EnableWebSocketMessageBroker;
import org.springframework.web.socket.config.annotation.StompEndpointRegistry;
import org.springframework.web.socket.config.annotation.WebSocketMessageBrokerConfigurer;

@Configuration
@EnableWebSocketMessageBroker
public class WebSocketConfig implements WebSocketMessageBrokerConfigurer {

  @Override
  public void configureMessageBroker(MessageBrokerRegistry config) {
    config.enableSimpleBroker("/topic");
    config.setApplicationDestinationPrefixes("/app");
  }

  @Override
  public void registerStompEndpoints(StompEndpointRegistry registry) {
    registry.addEndpoint("/gs-guide-websocket").withSockJS();
  }

}

---

6- Create a Browser Client : With the server-side pieces in place, you can turn your attention to the JavaScript client that will send messages to and receive messages from the server side.

7- Make the Application Executable : Spring Boot creates an application class for you. In this case, it needs no further modification. You can use it to run this application 

---  

package com.example.messagingstompwebsocket;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class MessagingStompWebsocketApplication {

  public static void main(String[] args) {
    SpringApplication.run(MessagingStompWebsocketApplication.class, args);
  }
}

---