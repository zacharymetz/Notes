# 5/4/2018

### Adding a new column of inrimenting ints to an existing table

```sql
ALTER TABLE accounts ADD id INT IDENTITY(1,1) 
```


# 5/7/2018

### Updating a table to add unique data from another table 

```sql
Update Client
SET Client.MaritalStatus = Data.[Marital Status]
From Client
INNER JOIN Data ON Client.ClientId = Data.MigrateID

GO
 
```


# 5/14/2018

### Drop a PostgreSQL database if there are active connections to it

```sql
SELECT pg_terminate_backend(pg_stat_activity.pid)
    FROM pg_stat_activity
    WHERE pg_stat_activity.datname = 'target_db'
      AND pid <> pg_backend_pid();
```
Then
```sql
DROP DATABASE target_db
```
