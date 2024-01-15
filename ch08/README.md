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
- https://www.postgresqltutorial.com/postgresql-plpgsql/introduction-to-postgresql-stored-procedures/
- https://www.postgresql.org/docs/current/explicit-locking.html
- https://www.postgresql.org/about/
- https://www.postgresqltutorial.com/

<br />

## Code blocks specific to the chapter

#### Creating the "tickets" table
```
CREATE TABLE tickets(
	id SERIAL PRIMARY KEY,
	event_name VARCHAR(255) NOT NULL,
	ticket_price DECIMAL(10,2) NOT NULL,
	is_booked BOOLEAN NOT NULL DEFAULT FALSE
);
```

#### Checking if the table has been created
```
SELECT * FROM tickets;
```

#### Inserting data into the table
```
INSERT INTO tickets (event_name, ticket_price) VALUES
	('Concert A', 50.00),
	('Concert B', 75.00),
	('Conference X', 100.00);
```

#### Reviewing if the data has been inserted into the table
```
SELECT * FROM tickets;
```

#### Steps for Person A without row-level lock
```
CREATE OR REPLACE FUNCTION update_ticket_price1()
RETURNS VOID AS $$
DECLARE
	price1 DECIMAL(10,2);

BEGIN
	SELECT ticket_price INTO price1 FROM tickets
WHERE id = 3;

PERFORM pg_sleep(30);

price1 := price1 + 10;

UPDATE tickets SET ticket_price = price1 WHERE id=3;
END;
$$ LANGUAGE plpgsql;

SELECT update_ticket_price1();
SELECT * FROM tickets;
```

#### Steps for Person B without row-level lock
```
CREATE OR REPLACE FUNCTION update_ticket_price2()
RETURNS VOID AS $$
DECLARE
	price2 DECIMAL(10,2);

BEGIN
	SELECT ticket_price INTO price2 FROM tickets 
WHERE id = 3;

PERFORM pg_sleep(30);

price2 := price2 + 15;

UPDATE tickets SET ticket_price = price2 WHERE id = 3;
END;
$$ LANGUAGE plpgsql;

SELECT update_ticket_price2();
SELECT * FROM tickets;

```
