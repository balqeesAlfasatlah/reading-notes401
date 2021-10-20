# Review: High-level HTTP

## The HTTP Request Lifecycle :

+ Every Http request first contacts a DNS server which resolves the request URL domain to a IP address.

+ After fetching the Webserver IP address request is forwarded to it(via PUT request). A webserver like apache handles this request and forwards this to application which has to handle this.

+ Step 1: Local Processing :

  + Your browser extracts the "scheme"/protocol (we have established
that this will be HTTP), host (www.example.com)

  + the browser needs to resolve an IP address1 so its will look through its own cache of recently requested URLs, the operating system’s cache of recent queries, your router’s cache, and your DNS cache

+ Step 2: Resolve an IP :

  + if the cache lookup fails, your browser fires off a DNS request using UDP3.

  + Your request will now have to travel many network devices to reach its target DNS server. 

  + Once your request arrives at your configured DNS server, the server looks for the address associated with the requested hostname.

+ Step 3: Establish a TCP Connection :

  + Now that the client has an IP address

+ Step 4: Send an HTTP Request :

  + Once the response has been fully delivered, the client sends a FIN packet at the TCP level.

  + your browser begins processing what it has received. 
  

![](https://csharpcorner-mindcrackerinc.netdna-ssl.com/article/introduction-to-iis-server-http-request-life-cycle-hosting-a-website-in-iis-se/Images/image005.png)

## Simple HTTP Request in Java :

 here a way of performing HTTP requests in Java — by using the built-in Java class HttpUrlConnection :

  + HttpUrlConnection class allows us to perform basic HTTP requests without the use of any additional libraries.

  + We can create an HttpUrlConnection instance using the openConnection() method of the URL class. 

  + If we want to add parameters to a request, we have to set the doOutput property to true, then write a String of the form param1=value¶m2=value to the OutputStream of the HttpUrlConnection instance.

  + Adding headers to a request can be achieved by using the setRequestProperty() method

  + HttpUrlConnection class allows setting the connect and read timeouts.

  + The "java. net" package contains classes that ease working with cookies such as CookieManager and HttpCookie.

  + We can enable or disable automatically following redirects for a specific connection by using the setInstanceFollowRedirects() method with true or false parameter

  + Reading the response of the request can be done by parsing the InputStream of the HttpUrlConnection instance.
 
  + It's not possible to get the full response representation using the HttpUrlConnection instance.

 

