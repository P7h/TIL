## Hive commands


### List databases
```SQL
SHOW databases;
```

### Exit PSQL console
```SQL
\q
```
Or <kbd>quit;</kbd>
Or <kbd>exit;</kbd>
Or <kbd>Ctrl</kbd> + <kbd>d</kbd>

### Connect to a database
```SQL
USE db_name;
```


### List all tables of a database
```SQL
SHOW tables;
```


### Run a HiveQL statement on command line
```bash
hive -e "show tables"
```


### Run a file containing HiveQL statements from command line
```bash
hive -f hiveql_file.sql
```


### Drop all tables of a Hive database named Hive_DB
```SQL
hive -e 'use Hive_DB;show tables' | xargs -I '{}' hive -e 'use Hive_DB;drop table {}';
```
