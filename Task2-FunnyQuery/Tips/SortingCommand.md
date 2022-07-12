In order to sort our result, we need to use `sort()`. To specify sorting order 1 and -1 are used. 1 is used for ascending order while -1 is used for descending order.

```shell
    db.users.find().sort({object_key: 1/-1})
```

For example, to descending the Address, we have to 
```shell
    db.users.find().sort({Address: -1})
```

However, if we want to sort the Address in asscending order, we can
```shell
    db.users.find().sort({Address: 1})
```