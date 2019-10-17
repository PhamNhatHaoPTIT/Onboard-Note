## Week 3 (07/10 -> 11/10)

### Concept of JDBC, JDBC driver and relate concept

+ JDBC -> JDBC drives (we have 4 types)

    + JDBC -> ODBC -> DB
    + native-driver
    + JDBC -> middleware -> DB (network protocol driver)
    + JDBC -> DB (directly), we have 2 advantage and 1 disadvantage

+ Three types of statement

+ ResultSet

+ Flow when we interact with JDBC

## Week 4 (14/10 -> 18/10)

### JDBC in Spring framework

+ Notice concept: jdbcTemplate, NamedParameterJdbcTemplate, RowMapper interface (create seperate class impl interface to map java bean and sql db) 
+ Transaction in Spring framework

+ PlatformTransactionManager: a service provider interface (SPI)

+ TransactionDefinition:
  + Propagation (scope of a transaction): required, requires_new, nested.
  + Isolation
  + Timeout: the time between start transaction and end -> auto rollback
  + Read-only status: 