<h1> Week 3 - Core JDBC </h1>

<h2> Time 07/10 - 11/10 </h2>

#### JDBC driver

+ A `JDBC driver` is a JDBC API `implementation` used for connecting to a particular type of database. There are several types of JDBC drivers
  + Type 1 – contains a mapping to another data access API; an example of this is the JDBC-ODBC driver
  + Type 2 – is an implementation that uses client-side libraries of the target database; also called a native-API driver
  + Type 3 – uses middleware to convert JDBC calls into database-specific calls; also known as network protocol driver
  + Type 4 – connect directly to a database by converting JDBC calls into database-specific calls; known as database protocol drivers or thin drivers,

#### Executing SQL Statements

+ The send SQL instructions to the database, we can use instances of type `Statement, PreparedStatement or CallableStatement`. These are obtained using the `Connection` object.

#### Parsing Query Results

+ ResultSet interface
  + The ResultSet uses the `next()` method to move to the next line.

+ Updatable ResultSet
  + ResultSet object can only be `traversed` forward and `cannot` be modified.

#### Flow

+ Flow when we interact with JDBC
  
  <div align="center">
    <img src="media/interact-jdbc.png" />
  </div>
