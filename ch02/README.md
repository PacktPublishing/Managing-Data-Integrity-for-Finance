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

INSERT INTO Transactions (TransactionID, AccountID, TransactionDate,
Amount)
VALUES (101, 1, '2023-01-01', 500.00);
```


#### CHECK constraint

```
CREATE TABLE Accounts (
AccountID int,
CustomerName varchar(100),
Balance decimal(10, 2) CHECK (Balance >= 0)
);

INSERT INTO Accounts (AccountID, CustomerName, Balance)
VALUES (1, 'Jane Doe', -100.00);
```
