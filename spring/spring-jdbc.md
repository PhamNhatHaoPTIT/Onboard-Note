## Week 3 (07/10 -> 11/10) - Core JDBC

### Concept of JDBC, JDBC driver and relate concept

+ JDBC -> JDBC drives (we have 4 types)

    + JDBC -> ODBC -> DB
    + native-driver
    + JDBC -> middleware -> DB (network protocol driver)
    + JDBC -> DB (directly), we have 2 advantage and 1 disadvantage

+ Three types of statement

+ ResultSet

+ Flow when we interact with JDBC

## Week 4 (14/10 -> 18/10) - JDBC in Spring - Transaction and relate concept

### JDBC in Spring framework

+ Notice concept: jdbcTemplate, NamedParameterJdbcTemplate, RowMapper interface (create seperate class impl interface to map java bean and sql db) 
+ Transaction in Spring framework

+ PlatformTransactionManager: a service provider interface (SPI)

+ TransactionDefinition:
  + Propagation (scope of a transaction): required, requires_new, nested.
  + Isolation level
  + Timeout: the time between start transaction and end -> auto rollback
  + Read-only status: 

+ Inside @Transactional
  + Transaction work flow
  + Transaction management (2 type: programmatic and declarative)
  + Proxy class in @Transactional

+ Rollback transaction: 
  + a/0 -> runtime exception
  + try-catch -> not rollback
  + throw new Exception(); 
  + Unchecked exception -> rollback -> crash app

+ Concept of AOP in Spring
  + advice
  + pointcut
  + joinpoint

## Week 5 (21/10 -> 25/10)

+ Continue with transaction topic in Spring

+ Write test to verify