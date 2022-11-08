## Rename a database:
```
USE master;  
GO  
ALTER DATABASE {1} SET SINGLE_USER WITH ROLLBACK IMMEDIATE;
GO
ALTER DATABASE {1} MODIFY NAME = {2};
GO  
ALTER DATABASE {2} SET MULTI_USER;
GO
```


## Check the collation of Databases
`SELECT name, collation_name FROM sys.databases;`

## Check the collation of tables
```
SELECT t.name TableName, c.name ColumnName, collation_name  
FROM sys.columns c  
inner join sys.tables t on c.object_id = t.object_id;  
```