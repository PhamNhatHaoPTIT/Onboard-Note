## Week 1 (23/09 -> 27/09) - Spring core concept and principle

### IoC (Inversion of Control) a principle in SE

+ the control of objects of a program transferred to a container or framework (often used in OOP)

+ IoC control the flow of a program and make calls to our custom code

### DI

+ hardcode vs dependency injection

### Combine IoC and DI

+ IoC comes to the rescue, programmer is relieved of burden

### IoC container

+ create object (spring bean), control, config

### Spring bean

+ beans are java objects that are managed by the Spring container

+ how we can access it? -> BeanFactory and ApplicationContext (includes all functionity of the BeanFactory and much more)

+ bean scope: singleton and prototype scope

+ bonus: nested prototype in singleton bean