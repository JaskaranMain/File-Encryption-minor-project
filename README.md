# File-Encryption-minor-project



<h2>DB:</h2> 
<h3>MyConnection:</h3>
Here Java code defines a class called MyConnection inside a package named db. The class manages a database connection using JDBC to a MySQL database located at "jdbc:mysql://localhost:3306/SecureHide?useSSL=false". It provides methods to establish a connection and close the connection.

Key points of the code:

1- The class has a private static Connection object named connection to store the database connection.

2- It has constant fields URL, USER, and PASSWORD containing the database connection details.

3- It uses a Logger object to record logs for connection-related events.

4- The private constructor prevents instantiation of the class.

5- The getConnection() method checks if a connection already exists. If not, it establishes a new connection using the DriverManager class and logs an info message if successful.

6- If an exception occurs during connection setup, it logs an error and throws a RuntimeException.

7- The closeConnection() method checks if the connection is not null, closes the connection, logs a message, and sets the connection to null.

<hr>

<h2>DAO package:</h2> 
<h3>userDAO:</h3>
this defines a method isExist that checks if a given email address exists in a database table named 'users'. Here's a breakdown of the code:

Key points of the code:

1- The method takes an email address as a parameter and returns a boolean value (true if the email exists in the database, false if it doesn't).

2- It establishes a connection to the database using a method called MyConnection.getConnection().

3- It prepares a SQL statement to select all email addresses from the 'users' table.

4- It executes the SQL query and retrieves the result set.

5- It iterates through the result set, checking each email address against the input email.

6- If a match is found, the method returns true, indicating that the email exists in the database.

7- If no match is found during the iteration, the method returns false, indicating that the email does not exist in the database.

8- If an SQL exception occurs during the process, it is caught, the exception is printed, and the method returns false.
