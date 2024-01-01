# Managing Data Integrity for Finance

**Chapter 9: Using Managed Ledger Databases for Finance Data Integrity** <br />
This chapter teachers the reader how to use managed ledger databases to enforce data integrity in financial systems and applications.

<br />
<br />
<br />
<br />
<br />

## Links and Files
<br />

## Code blocks specific to the chapter
#### Generating a document
```
INSERT INTO "myCustomers" `{"CustomerName":"John Ryan","CustomerId":"S0001", "CustomerAddress": "55 Prairie, Lincoln Drive 20502", "Loans":{"Student":10000}}`;
```

<br />

#### Viewing the data in the table
```
SELECT * FROM myCustomers;
```
<br />

#### Adding records to the table
```
INSERT INTO "myCustomers" `{"CustomerName":"Jack Kane","CustomerId":"S0002", "CustomerAddress": "77 Shawn St, Bradley Drive 20206", "Loans":{"Car":45000}}`;
INSERT INTO "myCustomers" `{"CustomerName":"Winnie Li","CustomerId":"S0003", "CustomerAddress": "86 Wonder Road, Sunrise Drive 20238", "Loans":{"Home":35000}}`;
```

<br />
#### To obtain the block address of the document
```
SELECT m.metadata.CustomerId, m.blockAddress
FROM _ql_committed_myCustomers AS m
WHERE m.data.CustomerId = 'S0001'
```
<br />
