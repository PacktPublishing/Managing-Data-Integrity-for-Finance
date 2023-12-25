#### UNIQUE constraint

```
CREATE TABLE Customers (
    CustomerID int,
    Name varchar(100),
    Email varchar(100) UNIQUE
); 

INSERT INTO Customers (CustomerID, Name, Email)
VALUES (1, 'Jane Lat', 'jane@example.com');

INSERT INTO Customers (CustomerID, Name, Email)
VALUES (2, 'Jane Sarah', 'jane@example.com'); 
```
