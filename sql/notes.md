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
