To create a table, there is no any directly way to generate a table, however, we can via insert something to table to generate the table at the same time.

```shell
    db.<table_name>.insertOne({object})
```

For example, we want to generate a table called users, and insert one object to it. 
<br>
Object Content: {name: "Novice", Age: 20, Todo: "learning"}

```shell
    db.users.insertOne({name: "Novice", Age: 20, Todo: "learning"})
```