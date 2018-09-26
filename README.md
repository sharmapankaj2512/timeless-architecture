# Timeless architecture 
### Domain Driven Design - Meets - Clean Architecture

The idea here is to completely isolate domain from infrastructural dependencies allowing one to swap controller, messaging or persistence layer independently.

For example if you are using spring:
- spring-web dependency is added to controllers only
- spring-data dependency is added to persistence only
- spring-cloud-stream dependency is added to messaging only
    
In future if you wish to replace spring-data with something else then all you have to do is create a new persistence sub-project for it.     

![Project Structure](https://raw.githubusercontent.com/sharmapankaj2512/timeless-architecture/master/project-structure.png)

### BENEFITS 

1. Packaging of classess becomes a no-brainer. It automatically helps a developer put highly cohesive classes togather.
For example: A EventPublisher will publish events per usecase, so it is placed in the core sub-project. An auditing aspect created to used on controller methods is placed in the controllers subproject. 
