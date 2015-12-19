# URL Schema #
An explanation of the URL schema in use by restful-sqlite. All results are returned in JSON format.

| **URL** | **GET method** | **POST method** | **PUT method** | **DELETE method** |
|:--------|:---------------|:----------------|:---------------|:------------------|
| /       | Lists all databases in defined data directory | Not implemented | Not implemented | Not implemented   |
| /`database`/ | List all tables in `database` | Not implemented | Not implemented | Not implemented   |
| /`database`/`table`/ | `SELECT * FROM table` | `INSERT`        | Not implemented | `DROP TABLE`      |
| /`database`/`table`/`id` | `SELECT * WHERE ROWID=id` See [ROWID](http://www.sqlite.org/autoinc.html) | `UPDATE`        | `REPLACE`      | `DELETE`          |