# Managing Data Integrity for Finance

<a href="https://www.packtpub.com/product/managing-data-integrity-for-finance/9781837630141"><img src="https://content.packt.com/B19758/cover_image_small.jpg" alt="Book Name" height="120px" align="left" style="margin: 0px 15px; border-color: white; border-style: solid; border-width: 1px;"></a>

**Chapter 2: Avoiding Common Data Integrity Issues and Challenges in Finance Teams** <br />
This chapter dives deep into the data integrity issues and challenges faced by different finance teams.

<br />
<br />
<br />
<br />
<br />

## Implementing preventative measures and constraints when using databases such as PostgreSQL
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


#### DOMAIN constraint

```
CREATE TABLE Accounts (
    AccountID int,
    CustomerName varchar(100),
    Balance decimal(10, 2),
    Type varchar(20) CHECK (Type IN ('Savings', 'Checking', 'Credit',
'Loan'))
);

INSERT INTO Accounts (AccountID, CustomerName, Balance, Type)
VALUES (1, 'Jane Doe', 1000.00, 'Investment');
```
