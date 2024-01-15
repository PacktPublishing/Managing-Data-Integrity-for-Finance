# Managing Data Integrity for Finance

<a href="https://www.packtpub.com/product/managing-data-integrity-for-finance/9781837630141"><img src="https://content.packt.com/B19758/cover_image_small.jpg" alt="Book Name" height="120px" align="left" style="margin: 0px 15px; border-color: white; border-style: solid; border-width: 1px;"></a>

**Chapter 8: Using Database Locking Techniques for Financial Transaction Integrity** <br />
This chapter dives deep into how specific SQL and database techniques prevent transaction data integrity issues.

<br />
<br />
<br />
<br />
<br />

## Links and Files

- https://www.postgresql.org/download/
- https://www.postgresql.org/docs/current/explicit-locking.html
- https://www.postgresql.org/about/
- https://www.postgresqltutorial.com/

<br />

## Code blocks specific to the chapter

#### To create the tickets table
```
CREATE TABLE tickets(
	id SERIAL PRIMARY KEY,
	event_name VARCHAR(255) NOT NULL,
	ticket_price DECIMAL(10,2) NOT NULL,
	is_booked BOOLEAN NOT NULL DEFAULT FALSE
);
```

##### To check if the table has been created
```
SELECT * FROM tickets;
```

