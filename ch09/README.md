# Managing Data Integrity for Finance

<a href="https://www.packtpub.com/product/managing-data-integrity-for-finance/9781837630141"><img src="https://content.packt.com/B19758/cover_image_small.jpg" alt="Book Name" height="120px" align="left" style="margin: 0px 15px; border-color: white; border-style: solid; border-width: 1px;"></a>

**Chapter 9: Using Managed Ledger Databases for Finance Data Integrity** <br />
This chapter teaches you how to use managed ledger databases to enforce data integrity in financial systems and applications.

<br />
<br />
<br />
<br />
<br />

## Links and Files
- https://www.youtube.com/watch?v=a9__D53WsUs
- https://aws.amazon.com/qldb/customers/
- https://en.wikipedia.org/wiki/Merkle_tree
- https://aws.amazon.com/
- https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html
- https://aws.amazon.com/blogs/opensource/announcing-partiql-one-query-language-for-all-your-data/
- https://docs.aws.amazon.com/qldb/latest/developerguide/working.redaction.html
- https://docs.aws.amazon.com/qldb/latest/developerguide/what-is.overview.html
- https://docs.aws.amazon.com/cost-management/latest/userguide/what-is-costmanagement.html
- https://docs.aws.amazon.com/qldb/latest/developerguide/what-is.html
- https://docs.aws.amazon.com/qldb/latest/developerguide/what-is.relational-ledger.html
- https://docs.aws.amazon.com/qldb/latest/developerguide/qldb-glossary.html
- https://docs.aws.amazon.com/qldb/latest/developerguide/verification.html
- https://docs.aws.amazon.com/qldb/latest/developerguide/working.history.html
- https://docs.aws.amazon.com/qldb/latest/developerguide/working.optimize.html
- https://aws.amazon.com/qldb/pricing/
<br />

## Versions of the tools used
- A web browser
- Any text editor (such as Notepad or Sublime Text)

## Code blocks specific to the chapter
#### Generating a document
<pre>
INSERT INTO "myCustomers" `{"CustomerName":<b>"John Ryan"</b>,"CustomerId":"S0001", "CustomerAddress": "55 Prairie, Lincoln Drive 20502", "Loans":{"Student":10000}}`;
</pre>



#### Viewing the data in the table
```
SELECT * FROM myCustomers;
```


#### Adding records to the table
```
INSERT INTO "myCustomers" `{"CustomerName":"Jack Kane","CustomerId":"S0002", "CustomerAddress": "77 Shawn St, Bradley Drive 20206", "Loans":{"Car":45000}}`;
INSERT INTO "myCustomers" `{"CustomerName":"Winnie Li","CustomerId":"S0003", "CustomerAddress": "86 Wonder Road, Sunrise Drive 20238", "Loans":{"Home":35000}}`;
```



#### To obtain the block address of the document

```
SELECT m.metadata.CustomerId, m.blockAddress
FROM _ql_committed_myCustomers AS m
WHERE m.data.CustomerId = 'S0001'
```


#### Updating the transaction
```
UPDATE myCustomers AS m
SET m.Loans.Car = 5000
WHERE m.CustomerId = 'S0001'
```



#### Deleting records from the ledger
```
DELETE FROM myCustomers;
```


#### Working with history and data (history)
```
SELECT * FROM history(myCustomers);
```
#### Working with history and data (data)
```
SELECT data FROM history(myCustomers);
```

#### Inserting the initial records again
```
INSERT INTO "myCustomers" `{"CustomerName":"John Ryan","CustomerId":"S0001", "CustomerAddress": "55 Prairie, Lincoln Drive 20502", "Loans":{"Student":10000,"Car":5000}}`;
INSERT INTO "myCustomers" `{"CustomerName":"Jack Kane","CustomerId":"S0002", "CustomerAddress": "77 Shawn St, Bradley Drive 20206", "Loans":{"Car":45000}}`;
INSERT INTO "myCustomers" `{"CustomerName":"Winnie Li","CustomerId":"S0003", "CustomerAddress": "86 Wonder Road, Sunrise Drive 20238", "Loans":{"Home":350000}}`;
```
