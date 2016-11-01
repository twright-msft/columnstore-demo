# columnstore-demo
This is a simple Java-based command line application that shows how to use a clustered columnstore index to improve performance.

The application does the following:
* The application uses the Microsoft JDBC connector to connect to SQL Server.
* Then it runs a simple query to get and display the version information.
* Next it runs queries to create an 'Example' database and a Orders table.
* A query is then run to generate some demo data in the Orders table.
* The application then runs a query to sum up the Price column in the Orders table.
* The elapsed time to run the query is shown.
* Then a clustered columnstore index is created.
* Lastly, the same query is run to sum the Price column in the Orders table.
* The elapsed time is shown for the query after the clustered columnstore index is added.
* The performance improvement from adding the columnstore index is shown.

To run this application you need to have the following installed:
* [Java](https://java.com/en/download/help/index_installing.xml)
* [Microsoft JDBC Driver](https://www.microsoft.com/en-us/download/details.aspx?id=11774)
* A SQL Server instance running somwhere that you can connect to.

:exclamation:##Before you run this application, change the connectionUrl information: server name, port, default database, user, password##

### After making changes to the .java file, recompile with this command:
`javac columnstoreDemo.java`

### To run this application from the directory where the project is cloned:
`java -cp .:/<location of JDBC driver jar> columnstoreDemo`

### Example:
`java -cp .:/Users/travis/Projects/sqljdbc42.jar columnstoreDemo`