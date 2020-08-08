## General:
* `express.json()` parse the req body to json if the `content-type` is set to `application/json`
* `now() - '3 days'::INTERVAL` generate a valid datetime that's 3 days before right now
* `String''s value`: escape single quote
* `knex({client:' ', connection:' ')`: knex instance
* `knexInstance()`: promise-like obj

## SQL Statements:

`CREATE TABLE <name> (
    <columnName> <dataType> (<size>) <option>,
);`

`INSERT INTO <tableName> (<column list>) VALUES (<value list>) ;`

`SELECT <column list> FROM  <table name> WHERE <conditions> AND <condtions> ORDER BY ... ;`

`WHERE name LIKE %searchTerm%`: find column that contains the search term (`ILIKE`: case insensitive)

## Knex methods:

`.toQuery()`: modify the complete query code
`.whereNotNull`: filter results
`.count()`
`.where()`
`.raw()`: pass in raw SQL statement as a string (use `??` to identify user input, known as 'prepared statement')

## Migration:
**Usage**: make copies of the db, add new features to the app, revert changes to the tables etc (steps)

* `postgrator-config.js`: `{"migrationDirectory": '', "driver":'', "connectionString":''}`

## Testing:
* `.toLocaleString()`: for both expected and actual
* `this.retries()`: specify how many times to attempt the test before counting it as a failure

