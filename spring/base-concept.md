<h1> Week 1 - Spring core concept and principle </h1>

<h2> Time 23/09 - 27/09 </h2>

<h3> Table of contents </h3>

- [Inversion of Control - A principle in Software engineer](#inversion-of-control---a-principle-in-software-engineer)
- [Dependency injection](#dependency-injection)
- [Inversion of Control and Dependency Injection playing together](#inversion-of-control-and-dependency-injection-playing-together)
- [The Spring IoC container](#the-spring-ioc-container)
- [Spring bean](#spring-bean)

#### Inversion of Control - A principle in Software engineer

+ The control of objects of a program `transferred to a container or framework` (often used in OOP). So instead of writing `new MyObject` in your code, the object is created by `someone else`. This someone else is normally referred to as an `IoC container.`

#### Dependency injection

+ Dependency Injection has become one of the cornerstones of modern software engineering, as it is fundamental to allow proper testing.

+ Hardcode vs dependency injection

    ```java
        // hardcoded dependency
        public class MyClass { 
            private MyDependency myDependency = new MyDependency(); 
        }
    ```

    ```java
        // injected dependency
        public class MyClass { 
            private MyDependency myDependency;

            public MyClass(MyDependency myDependency) {
                this.myDependency = myDependency;
            }
        }
    ```

#### Inversion of Control and Dependency Injection playing together

+ IoC comes to the rescue, with IoC, the dependencies are managed by the container, and the programmer is relieved of that burden.

+ Using annotations like `@Autowired`, the container is asked to inject a dependency where it is needed, and the programmers do not need to create/manage those dependencies by themselves.

    ```java
        public class MyClass1 {
            @Autowired
            private MyClass2 myClass2;

            public void doSomething() {
                myClass2.doSomething();
            }
        }
    ```

    ```java
        public class MyClass2 {
            @Autowired
            private MyClass3 myClass3;

            @Autowired
            private MyClass4 myClass4;

            public void doSomething() {
                myClass3.doSomething();
                myClass4.doSomething();
            }
        }
    ```

#### The Spring IoC container

+ It is the `heart` of the Spring Framework. The IoC container receives `metadata` from either an `XML file, Java annotations, or Java code`. The container gets its instructions on what objects to `instantiate, configure, and assemble from simple Plain Old Java Objects (POJO)` by reading the configuration metadata provided. These created objects through this process called `Spring Beans.`

+ The responsibilities of IoC container are:
  + `Instantiating` the bean
  + `Wiring the beans` together
  + `Configuring` the beans
  + `Managing` the bean’s entire life-cycle

#### Spring bean

+ Beans are `java objects` that are managed by the `Spring container`

+ How we can access it? -> through BeanFactory or ApplicationContext - includes all functionity of the BeanFactory and much more

+ Bean scope: singleton and prototype scope

+ Nested prototype in singleton bean
