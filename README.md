# Timeless architecture 
### Domain Driven Design Meets Clean Architecture

The idea here is to completely isolate domain from infrastructural dependencies allowing one to swap controller, messaging or persistence layer independently.

For example if you are using spring:
- spring-web dependency is added to controllers only
- spring-data dependency is add to persistence only
- spring-cloud-stream dependency is added to messaging only
    
So in future if you wish to replace spring-data with something else then all you have to do is create a new persistence sub-project for it.     

![Project Structure](https://raw.githubusercontent.com/sharmapankaj2512/timeless-architecture/master/project-structure.png) 
