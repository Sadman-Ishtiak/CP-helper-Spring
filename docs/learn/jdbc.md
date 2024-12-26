# JDBC
JDBC is used to connect java with database as this literally translates to Java Database Connectivity. There are seven(7) steps involved in making a java program to connect with a database using a jdbc. The steps are-

1. Import the packages
2. Load and register the driver
3. Establish the connection
4. Create the statement
5. Execute the query
6. Process results
7. Close the connection

## Import the packages
We need to import the `java.sql` package which is the base package to work with sql. so we import this package to work further.

## Load and register the driver
In Order to work with specific databases we need the drivers of the respective jdbc driver for that database. The driver is usually gives the linking between the `java.sql` with the database itself. for example we use `com.mysql.jdbc` with the help of the jar file or even maven to connect with the mysql driver.

## Establish the connection

In order to establish the connection we need to instanciate interface `connection`

## Create the statement

There are three typer statement

1. Statement
2. Prepared statement
3. Callable statement

## Execute the query
## Process results
## Close the connection


---
## Code Example:
```java
import java.sql.*;

public static void main(){
    Class.forName("com.mysql.jdbc.Driver");
    Connection con = DriverManager.getConnection("url", "username", "pwd");
    Statement st = con.createStatement();
    ResultSet rs = st.executeQuery("select * from student");
    while(rs.Next()) {
        sysout(rs.getInt(1) + " " + rs.getString(2));
    }
    st.close();
    con.close();
}
```

