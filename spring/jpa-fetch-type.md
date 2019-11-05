### Eager loading vs. Lazy loading in JPA

+ The EAGER strategy is a `requirement` on the persistence provider runtime that `data must be` eagerly fetched. 
+ The LAZY strategy is a `hint` to the persistence provider runtime that `data should be` fetched lazily when it is first time accessed.

+ Default fetch type value
  + @ManyToOne and @OneToOne: Eager
  + @ManyToMany and @OneToMany: Lazy

+ Notice that
  + For lazy loading to work, the `JDBC session` must still be open when the target entities want to be loaded into the memory by invoking the getter method, but sometimes this is not possible, because by the time this method is called, the session is `already closed` and the entity detached.
  + Sometimes we have a client/server architecture (e.g. Swing client/JEE server) and the entities/DTOs are `transferred over` the wire to the client and again most often in these scenarios `lazy loading won't work` due to the way the entities are serialized over the wire.

### Advantages and disadvantages

+ Lazy
  + Advantages
    + Initial load time much smaller than eager
    + Less memory consumption than eager
  + Disadvantages
    + Delayed initialization might impact performance during unwanted moments
    + In some cases you need to handle lazily-initialized objects with a special care or you might end up with an exception (`LazyInitializationException`)

+ Eager
  + Advantages
    + No delayed initialization related performance impacts
  + Disadvantages
    + Long initial loading time
    + Loading too much `unnecessary` data might impact performance

### N + 1 problem

+ Introduction
  + The N + 1 problem is a performance anti-pattern in which an application makes N + 1 database calls (where N is the number of objects fetched)
  + Like most antipatterns, this isn't necessarily a problem in itself, but under certain circumstances (where N is large, for example) it will cause performance to `degrade` by making `hundreds or even thousands` of database calls for a `single business transaction`.

+ Resolve N + 1 selects problem
  + JPQL fetch join
  + Criteria query

### How to fetch entities multiple levels deep with Hibernate