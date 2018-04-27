# mysql-sql-cheatsheet

Collection of some mysql SQL queries i commonly used 

# Show

# Show databases in a mysql server

```sql
show databases;
```

# Show tables in a database

```sql
use mysql;
show tables;
```

# Show the structure of a table

```sql
desc purchase_order;
```

# Show index listing of a table

```sql
show index from product;
```

# Display a table select query nicely

```sql
select * from purchase_order\G;
```

# Create

### Create index

```sql
create index idx_item_activity_id on vendor (item_activity_id);
```

# Update

### Change a field data type in a table

```sql
alter table purchase_order modify status varchar(255);
```

### Update table1 from table2 based on joining

```sql
update purchase_order_line inner join purchase_order on purchase_order_line.purchase_order_id = purchase_order.id set purchase_order_line.created_at = purchase_order.created_at;
```

# Delete

### Delete an index from a table

```
alter table product drop index idx_type;
```


