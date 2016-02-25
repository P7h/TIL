## Hive commands


### Connect to a database named PGSQL_DB_Name
```SQL
\c PGSQL_DB_Name
```


### Exit PSQL console
```SQL
\q
```
Or <kbd>Ctrl</kbd> + <kbd>d</kbd>


### Time the SQL statement execution in PSQL console
```SQL
\timing
```


### List all tables of a database
```SQL
\d 		# or even \dt
```


### List all tables of a database with additional info of size taken by each table and description, if any
```SQL
\d+ 	# or even \dt+
```


### Describe a table named PGSQL_Table_Name
```SQL
\d PGSQL_Table_Name 	# or even \dt PGSQL_Table_Name
```


### Describe a table named PGSQL_Table_Name with additional info of size taken by each table and description, if any
```SQL
\d+ PGSQL_Table_Name 	# or even \dt+ PGSQL_Table_Name
```
