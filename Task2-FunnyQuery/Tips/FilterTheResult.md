As we know, to print out the result, we can use `find()` function to do so. However, this command will show out all the data, sometime if we just want to show out the value by indicated the object key, we can setup some conditions as a filter inside `find()` function.

```shell
    db.<table_name>.find({},{condition})
```

**Think About** What is the different between two {} that inside the `find()` function.
<br>

For example, we need to show the two eldest members and sorting the CustomerName as descending order (no _id), so here we can know that:
1. The result should only two data
    To limit the count of our result, we can use `limit()` function
    ```shell
        db.<table_name>.find().limit(number)
    ```
1. Find out the two eldest members 
    Using `sort()` function to sort the Age by descending first
    ```shell
        db.<table_name>.find().sort({Age: -1})
    ```
    
    Then, using `limit()` function to limit the amount of result
    ```shell
        db.<table_name>.find().sort({Age: -1}).limit(2)
    ```
    
1. CustomerName should be descending
    To sort the result, beside using the `sort()` method, we can also set a filter inside `find()` function.
    <br>

    **However**, we have to figure out what elements we need to **sort**, and what elements we need to **filter** first.
    <br>
    
    The most important concept is that, the filter elements will show in the result, however, the sorting elements won't show out. Think about the following two commands:
    ```shell
        db.users.find({},'CustomerName': -1, 'Age': -1).limit(2)
    ```
    
    ```shell
        db.users.find({},'CustomerName': -1).sort({Age: -1}).limit(2)
    ```
    
    Coming back with our task, now we need to **show out** our CustomerName and also show as descending order. So we can
    ```shell
        db.users.find({},'CustomerName': -1).sort({Age: -1}).limit(2)
    ```
    
1. The results don't need to show out the _id
    Finally, we need to filter out the _id from the results, to do so we can
    ```shell
        db.users.find({},'CustomerName': -1, _id: 0).sort({Age: -1}).limit(2)
    ```