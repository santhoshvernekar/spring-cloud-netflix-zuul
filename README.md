# Spring-cloud-Netflix-Zuul gateway service
This project demonstrates spring-cloud- Netflix-zuul gateway service with routing filters

### To Build project:
run mvn clean install

Zuul acts as an API gateway or Edge service,the Zuul is built to enable dynamic routing, monitoring, resiliency, and security. 

It provides a range of different types of filters, namely:
* pre filters – are invoked before the request is routed.
* post filters – are invoked after the request has been routed.
* route filters – are used to route the request.
* error filters – are invoked when an error occurs while handling the request.

We can implement these filters by extending a class ZuulFilter, I have implemented a sample filter to add location in the request header (AddRequestHeaderFilter class) 

### Steps for demo:
* [optional] To check the service getting registered with service discovery, we need to run the service discovery on our machine, You can find project in my repo [eureka-service-discovery](https://github.com/santoshmv121/eureka-discovery-server)
* Step 1: Launch the service discovery
* Step 2: Add @EnableZuulProxy annotation on Main class to enable the Zuul proxy
* Step 3: We need to run some client apps to see routing through proxy
* Step 4: Zuul by default uses application name for routing

For example: If gateway service is running on port 8080 and hello application running on 1111 and goodbye application running on 2222 port

You can hit the hello and goodbye application end points on port 8080 only (hello and goodbye applications end points can be accessed using http://localhost/hello and http://localhost/goodbve )

* Step 5: You can find the location is getting in the request header which is coming from zuul proxy.














### Reference Documentation
For further reference, please consider the following sections:

* [Official Apache Maven documentation](https://maven.apache.org/guides/index.html)
* [Spring Boot Maven Plugin Reference Guide](https://docs.spring.io/spring-boot/docs/2.3.9.BUILD-SNAPSHOT/maven-plugin/reference/html/)
* [Create an OCI image](https://docs.spring.io/spring-boot/docs/2.3.9.BUILD-SNAPSHOT/maven-plugin/reference/html/#build-image)
* [Eureka Discovery Client](https://docs.spring.io/spring-cloud-netflix/docs/current/reference/html/#service-discovery-eureka-clients)
* [Spring Boot Actuator](https://docs.spring.io/spring-boot/docs/2.4.2/reference/htmlsingle/#production-ready)
* [Spring Web](https://docs.spring.io/spring-boot/docs/2.4.2/reference/htmlsingle/#boot-features-developing-web-applications)
* [Zuul [Maintenance]](https://docs.spring.io/spring-cloud-netflix/docs/2.2.x/reference/html/#router-and-filter-zuul)

### Guides
The following guides illustrate how to use some features concretely:

* [Service Registration and Discovery with Eureka and Spring Cloud](https://spring.io/guides/gs/service-registration-and-discovery/)
* [Building a RESTful Web Service with Spring Boot Actuator](https://spring.io/guides/gs/actuator-service/)
* [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
* [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
* [Building REST services with Spring](https://spring.io/guides/tutorials/bookmarks/)
* [Routing and Filtering](https://spring.io/guides/gs/routing-and-filtering/)

# Spring Cloud Netflix Maintenance Mode

The dependencies listed below are in maintenance mode. We do not recommend adding them to
new projects:

*  Zuul

The decision to move most of the Spring Cloud Netflix projects to maintenance mode was
a response to Netflix not continuing maintenance of many of the libraries that we provided
support for.

Please see [this blog entry](https://spring.io/blog/2018/12/12/spring-cloud-greenwich-rc1-available-now#spring-cloud-netflix-projects-entering-maintenance-mode)
for more information on maintenance mode and a list of suggested replacements for those
libraries.
