# SQL
sql queries

<h2>Create Table</h2>

```sql
CREATE TABLE cities (
    id SERIAL PRIMARY KEY
    country_id INTEGER REFERENCES country(id),
    name VARCHAR(50),
    population INTEGER,
    aria BIGINT
);
```


<h2>Insert Data</h2>

```sql
INSERT INTO cities(name, country, population, area)
VALUES ('Dehli', 'India', 2546000, 6125),
       ('Shanghai', 'China', 22125000, 4015),
       ('Sao Paulo', 'Brazil', 20935000, 3043);
    
```

<h2>Calculated Column</h2>

```sql
SELECT name, population/area  
AS populationDensity 
FROM cities 
ORDER BY populationDensity DESC;
```

<h2>String Functions </h2>


```sql
SELECT name, 
CONCAT(name, ', ', country) AS location, 
LENGTH( name ) AS name_length,
UPPER(name) AS upper_name 
FROM cities;
```

<h2> Update query </h2>

```sql 
UPDATE cities
SET population = 39505000
WHERE name = 'Tokyo';
```


<h2> Delete query </h2>

```sql
DELETE FROM cities
Where name = 'Tokyo';
```
<h2>SQL information</h2>
<p>
Foreign key constraint checks every foreign key ids existence.
we can set foreign key to null if null: true attribute exist.
</p>

<p>
ON DELETE <br>
RESTRICT ( default ): Throw an error on delete. <br> 
NO ACTION: Throw an error on delete. <br>
CASCADE: Delete related data too!<br>
SET NULL: Set the foreign key to NULL.<br>
SET DEFAULT: Set the foreign key to a provided default value.<br>
</p>
JOINS <br>
<br>
<br>

<img src="./0001.jpg">
