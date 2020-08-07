## SQL Staments:

`CREATE TABLE <name> (
    <columnName> <dataType> (<size>) <option>,
);`

`INSERT INTO <tableName> (<column list>) VALUES (<value list>) ;`

`SELECT <column list> FROM  <table name> WHERE <conditions> AND <condtions> ORDER BY ... ;`

`WHERE name LIKE %searchTerm%`: find column that contains the search term (`ILIKE`: case insensitive)

## Knex methods:

`.toQuery()`: modify the complete query code
