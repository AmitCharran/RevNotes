# Week 2: SQL & JDBC Study Questions

You should research and be able to answer the following questions at the ned of each day:

> - Use Google and [SQL class notes](https://github.com/210726-Enterprise/demos/blob/main/week2/notes/sql.md). [AWS notes here](https://github.com/210726-Enterprise/demos/blob/main/week2/notes/aws.md)%3Cbr%3E
> - The [PostgreSQL Documentation](https://www.postgresqltutorial.com/) is a great resource (and easy to follow).
> - :star: **[W3 Schools SQL Tutorial](https://www.w3schools.com/sql/)** :star: For extra practice try the [Chinook Query Challenge](https://github.com/210726-Enterprise/demos/tree/main/week2/chinook-challenge)



## `Study Questions`

> Go over these questions to prepare for QC on August 16th or 17th (exact date TBA).

### SQL Questions

1. Explain what SQL is. What are some SQL RDBMS Vendors? *What is an RDBMS*?

   - SQL = Structured Query Language. It lets you access and manipulate databases.

   - Relational Database Management System (RDBMS) Vendors - Postres, SQLite, MYSQL
   - RDBMS -- Relational Database Management System - A relational database refers to a database that stores data in a structured format, using rows and columns. It is relational because  values  within each table are related to eachother and other tables. so queries can be run across multiple tables 

2. Draw a simple ERD for modeling Students and Classes

   - two entities, a student and a class. Many-to-Many relatioship

3. What are the 5 sublanguages of SQL? Which commands correspond to them?

   1. DML - Data Manipulation Language - UPDATE, INSERT, DELETE
   2. DDL - Data Definition Language - CREATE, ALTER, DROP, TRUNCATE, RENAME
   3. DQL - Data Query Language - SELECT
   4. DCL - Data Control Language - GRANT, REVOKE, AUDIT, COMMENT, ANALYZE
   5. TCL - Transaction Control Language - COMMIT, ROLLBACK, SAVEPOINT, ROLLBACK TO

4. What is the difference between DELETE, DROP, and TRUNCATE commands?

   1. DELETE - deletes a row
   2. DROP - deletes a table
   3. TRUNCATE - removes all rows in a table

5. What are some SQL clauses you can use with SELECT statements?'

   1. FROM - specifies the table
   2. WHERE - specifies which row to retrieve
   3. AS - optionally provides alias for columns or expression
   4. GROUP BY - groups rows sharing a property so that a function can be applied to the group
   5. HAVING - selects among the group that is defined by group by
   6. ORDER BY - specifies how the order is when returned

6. What is the difference between WHERE and HAVING? *`WHERE` is used to filter rows before grouping and `HAVING` is used to exclude records after grouping. Read more [here](https://www.java67.com/2019/06/difference-between-where-and-having-in-sql.html#ixzz6kwoJQmXd)*.

7. Explain what the ORDER BY and GROUP BY clauses do.

- Practice [here](https://www.w3schools.com/sql/sql_orderby.asp).

1. Explain the concept of relational integrity.
   1.  does not allow to add any record in a table that contains the foreign key unless the reference table containing a corresponding primary key		
   2. If any record in referenced table is deleted then all the corresponding records in the referencing table will be deleted for the referential integrity
2. List the integrity constraints.
   1. Set of rules used to maintain quality of information
   2. data insertion and updating as well as other processes have to be performed in such a way that data integrity is not affected.
   3. Used to guard against accidental damage to the database
   4. Integrity constraints
      1. Domain constraint - Data Types (character, varchar...)
      2. Entity Integrity constraint - Primary key value cannot be null
      3. Referential constraint - If a foreign key in Table 1 refers to the Primary Key of table 2, then every value of the foreign key in table 1 must be null or be available in table 2
      4. Key Constraint - Identifies entity within an entity set unqiuely.
3. Define the word “schema”.
   1. A collection of database objects.
      1. includes tables
      2. views
      3. triggers
      4. stored procedures
      5. indexes
4. What is a candidate key? What about a surrogate key?
   1. Candidate Key
      1. column or set of columns that can qualify for candidate key
   2. Surrogate key
      1. Key not derived from columns of a table
      2. Not a natural key
      3. auto generated number
5. What conditions lead to orphan records? (*Think about what happens when we delete from a table that a child table is dependent on because it feautres its Primary keys as foreign keys within the table*)
   1. A record whose foreign key value references a non-existent primary key value
   2. Describe above with tables. It violates referential integrity
6. What are some SQL data types?
   1. Here ![https://www.w3schools.com/sql/sql_datatypes.asp]
   2. String types 	
      1. CHAR
      2. VARCHAR
      3. BINARY
      4. VARBINARY
      5. TINYBLOB
      6. TINYTEXT
      7. TEXT
      8. BLOB
      9. MEDIUMTEXT
      10. LONGTEXT
      11. LONGBLOB
      12. ENUM
      13. SET
   3. Numeric Types
      1. BIT
      2. TINYINT
      3. BOOL
      4. BOOLEAN
      5. SMALLINT
      6. MEDIUMINT
      7. INT
      8. INTEGER
      9. BIGINT
      10. FLOAT
      11. DOUBLE
      12. DOUBLE PERCISION
      13. DECIMAL
      14. DEC
   4. DATE
      1. DATE
      2. DATETIME
      3. TIMESTAMP
      4. TIME
      5. YEAR
7. What is normalization? What are the levels? (0 - 3NF)
8. What are the properties a transaction must follow? (*A.C.I.D*)
   1. A - Atomicity - all changes to the data are performed as if they are single operation. That is, all the changes are performed, or none of them are
      1. Example -- if an app that transfers funds to one account to another. The program must ensure that it is done successfully in one operation
   2. C - Consistency - Data is in a consistent state when a transaction starts and when it ends
      1. Example - in an application that transfers funds from one account to another, the consistency property ensures that the total value of funds in both the accounts is the same at the start and end of each transaction
   3. I - Isolation - The intermediate state of a transaction is invisible to other transaction. So concurrent transaction will appear to be serialized
      1. Example -  in an application that transfers funds from one account to another, the isolation property ensures that another transaction sees the transferred funds in one account or the other, but not in both, nor in neither.
   4. D - Durability - After a transaction successfully completes, changes to data persist and are not undone, even in the event of a system failure.
9. Explain the different isolation levels. What read phenomena do each prevent?
10. What is the difference between joins and set operators?
11. What are the types of joins? Explain the differences.
12. What is a cascade delete?
13. How would you setup a primary key that automatically increments with every INSERT statement?
14. What is the difference between scalar and aggregate functions? Give examples of each
15. 

### JDBC Questions

1. What is JDBC?

2. What are the core interfaces / classes in JDBC?

3. What is a stored procedure and how would you call it in Java?

4. What is the difference between Statement and PreparedStatement?

5. Steps to executing an SQL query using JDBC?

6. How to execute stored procedures using JDBC?

7. Which interface is responsible for transaction management?

   > `Connection` Interface. See this resource here about [JDBC and Transaction management](https://www.javatpoint.com/transaction-management-in-jdbc#:~:text=In JDBC%2C Connection interface provides methods to manage transaction)

### AWS & Cloud Computing Questions

1. what are the benefits of cloud services?
2. What are the 3 models of Cloud computing?
3. What is AWS RDS? What type of service is this? Iaas, Paas, Saas?
4. What is the relationship between a Region and an Availability Zone?
5. What are Security Groups?









## Collections / Generics

42. What are collections in Java?

- A general data structure that contains Objects. Also the name of the API

43. What are the interfaces in the Collections API?

- Iterable, Collection, List, Queue, Set, Map, SortedSet, SortedMap

44. What is the difference between a `Set` and a `List`?

- `Set` does not allow duplicates (its members are unique)

45. What is the difference between a `Array` and an `ArrayList`?

- An array is static and its size cannot be changed, but an ArrayList can grow/shrink

46. What is the difference between `ArrayList` and `Vector`?

- `Vector` is synchronized whereas `ArrayList` is not.

47. What is the difference between `TreeSet` and `HashSet`?

- The two general purpose `Set` implementations are `HashSet` and `TreeSet`. `HashSet` is much faster (constant time versus log time for most operations) but offers no ordering guarantees.

48. What is the difference between HashTable and HashMap?

- a. `Hashtable` is synchronized whereas `Hashmap` is not.

- b. `Hashmap` permits `null` values and the `null` key.

49. Are Maps in the Collections API?

- Yes, but they do not implement `Collection` or `Iterable` interfaces

50. What are generics? What is the diamond operator (`<>`)?

- A way of specifying a type within a data structure - they enforce type safety. `<>` operator lets you infer generic types from the LHS of assignment operation

## Threads

51. What is multi-threading?

- Handling multiple threads / paths of execution in your program.

52. In what ways can you create a thread?

- By extending the Thread Class or by implementing the `Runnable` Interface. You must call Thread's `.start()` method to start it as a new thread of execution.

53. Lifecycle of a thread

- When created, in NEW state.
- When `.start()` is called, it goes to RUNNABLE state.
- When `.run()` is called, goes to RUNNING state.
- If `.sleep()` or `.wait()` is called, will go to WAITING.
- If dependent on another thread to release a lock, it will go to BLOCKED state.
- When finished executing, will be in DEAD state and cannot be restarted.

54. What is deadlock?

- When two or more threads are waiting on locks held by the others, such that no thread can execute

55. What is synchronized keyword?

- Only allowing one thread access to the method or variable at a time - enforces thread-safety

## IO / Serialization

56. How do you serialize / deserialize an object in Java?

- a. Step 1: An object is marked serializable by implementing the `java.io.Serializable` interface, which signifies to the underlying API that the object can be flattened into bytes and subsequently inflated in the future.

- b. Step 2: The next step is to actually persist the object. That is done with the `java.io.ObjectOutputStream` class. That class is a filter stream--it is wrapped around a lower-level byte stream (called a node stream) to handle the serialization protocol for us. Node streams can be used to write to file systems or even across sockets. That means we could easily transfer a flattened object across a network wire and have it be rebuilt on the other side!

- c. To restore the object back, you use `ObjectInputStream.readObject()` method call. The method call reads in the raw bytes that we previously persisted and creates a live object that is an exact replica of the original. Because `readObject()` can read any serializable object, a cast to the correct type is required. With that in mind, the class file must be accessible from the system in which the restoration occurs. In other words, the object's class file and methods are not saved; only the object's state is saved.

57. What is a Marker interface?

- A marker interface is an interface which has no methods at all. Example: `Serializable`, `Remote`, `Cloneable`. Generally, they are used to give additional information about the behavior of a class.

58. What are transient variables?

- Transient variables are those variables which cannot be serialized.

59. Difference between FileReader and BufferedReader?

- `FileReader` is just a `Reader` which reads a file, so it reads characters and uses the platform-default encoding.

- `BufferedReader` reads text from a character-input stream, buffering characters so as to provide for the efficient reading of characters, arrays, and lines (e.g. can read one line at a time).

- So you can wrap a `BufferedReader` around a `FileReader`

## Design patterns

67. What are Singleton / Factory design patterns?

- Singleton - allows for creation of only 1 object. Method for retrieving object returns reference to the same object in memory. Implement via private constructor

- Factory - abstracts away instantiation logic, usually used in conjunction with singleton pattern

## JDBC

68. What is JDBC?

- A Java API used to execute queries on various databases. Uses JDBC drivers to connect with the database

69. What are the core interfaces / classes in JDBC?

- `DriverManager`, `Connection`, `Statement`, `PreparedStatement`, `CallableStatement`, `ResultsSet`

70. What is a stored procedure and how would you call it in Java?

- A stored procedure is an executable block of code that is written in PL/SQL and stored in the Oracle database. A stored procedure is called from a Java class using a CallableStatement object. When the procedure is called, its name and any relevant parameters are sent over the JDBC connection to the DBMS, which executes the procedure and returns the results (if applicable) via the connection.

71. What is the difference between Statement and PreparedStatement?

- PreparedStatements are pre-compiled by the JVM. The database doesn't have to compile the SQL each and every time it is executed. PreparedStatement can be parameterized, which can make the SQL more readable. Furthermore, PreparedStatement will properly escape reserved characters to prevent SQL injection attacks.

72. Steps to executing an SQL query using JDBC?

- 1. Register the driver using `.forName()` (or let `DriverManager` detect and load automatically from classpath)
- 2. Create the connection (`DriverManager.getConnection(url,username,password)`)
- 3. Create a statement for executing the SQL query (`Statement st = conn.createStatement()`);
- 4. Execute the SQL query (`ResultSet rs = st.executeQuery(String sql)`)
- 5. Use `ResultSet` to get values returned (`rs.getInt(1)`, etc)
- 6. Close the connection (`conn.close()`)

73. How to execute stored procedures using JDBC?

- Use the `Callable` statement interface

74. Which interface is responsible for transaction management?

- The `Connection` interface - can `commit`, `rollback`, etc

## JUnit

75. What is JUnit?

- A Java unit testing framework for testing code - use it for TDD

76. What is TDD?

- Test-driven development - write unit tests before application code, then write code to make tests pass. Repeat this process until functionality is complete.

77. What are the annotations in JUnit? Order of execution?

- BeforeClass, AfterClass, Before, After, Test, Ignore

78. Give an example of a test case?

- Adding two numbers, check that the method returns the sum

## Log4j

79. What is an advantage to using a logging library?

- Allows you to set logging thresholds

80. What is log4j?

- Logging library for Java

81. What are the logging levels of log4j?

- TRACE, DEBUG, INFO, WARN, ERROR, FATAL

## Maven

82. What is Maven?

- A build automation and dependcy management tool for Java applications

83. What is the default Maven build lifecycle?

- process resources - copy and process the resources into destination directory
- compile - compile the source code
- process-test-resources - same for test directory
- test-compile - compile the test code
- test - run the test code
- package - combine compiled source code into a .jar or .war file
- install - install package to local repo
- deploy - copy package and install in remote repo

84. Where / when does Maven retrieve dependencies from? Where are they stored locally?

- Maven first looks to see if the dependency is in the local repo under `.m2` directory. If not, it will download the necessary .jar file(s) from the remote central Maven repository into the `.m2` directory

85. What is the POM and what is the pom.xml?

- POM stands for project object model and is the model used by Maven to understand project attributes and dependencies. The pom.xml is the xml document which lists those attributes and dependencies

## Advanced

86. What are functional interfaces?

- Functional interfaces only have one method, and can be used in conjuntion with lambdas

87. What are lambdas?

- Like anonymous functions, they allow implementation of functional interfaces directly without creating a class

88. What is try-with-resources? What interface must the resource implement to use this feature?

- Try-with-resources allows for automatically closing resources in a try/catch block using `try(resource) {...}` syntax. Must implement the `AutoCloseable` interface

89. How to make numbers in your code more readable?

- Use the `_` for numeric literals - must be placed between numbers

90. Which collections cannot hold null values?

- `HashTable`, `TreeSet`, `ArrayDeque`, `PriorityQueue`

91. If 2 interfaces have default methods and you implement both, what happens?

- The code will NOT compile unless you override the method. However, the code WILL compile if one interface is implemented further up in the class hierarchy than the other - in this case, the closest method implementation in the hierarchy will be called

92. If 2 interfaces have same variable names and you implement both, what happens?

- The code will compile unless you make a reference to the variable (this is an ambiguous reference). You must explicitly define the variable by using the interface name: `int a = INTERFACENAME.a;`

93. Why does `HashTable` not take `null` key?

- The hash table hashes the keys given as input, and the `null` value cannot be hashed

94. What new syntax for creating variables was introduced with Java 10?

- The `var` keyword was introduced - with type inference

95. Is there an interactive REPL tool for Java like there is for languages like Python?

- Yes, the `jshell` tool introduced in Java 9

96. What are collection factory methods?

- They allow you to directly populate collections, e.g. `Set.of(1,2,3)`