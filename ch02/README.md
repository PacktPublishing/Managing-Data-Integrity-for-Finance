#### NOT NULL constraint

```
CREATE TABLE Accounts (
AccountID int,
CustomerName varchar(100) NOT NULL,
Balance decimal(10, 2)
);

INSERT INTO Accounts (AccountID, Balance)
VALUES (1, 100.00);
```


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


#### FOREIGN KEY constraint

```
CREATE TABLE Accounts (
    AccountID int PRIMARY KEY,
    CustomerName varchar(100),
    Balance decimal(10, 2)
);

CREATE TABLE Transactions (
    TransactionID int PRIMARY KEY,
    AccountID int,
    TransactionDate date,
    Amount decimal(10, 2),
    FOREIGN KEY (AccountID) REFERENCES Accounts(AccountID)
);
```
