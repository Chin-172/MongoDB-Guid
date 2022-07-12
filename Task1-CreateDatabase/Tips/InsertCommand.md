As we mentioned as before, we can insert an object to generate the table inside your DB, however, what about if we want to insert many objects as once?

```shell
    db.<table_name>.insertMany([{Object1},{Object2},{Object3},...])
```

For example, we want to insert the objects to the table called chess, such as:
object 1: {name: "King", amount: 1, movingRange: "12346789", movingSteps: 1}
object 2: {name: "Rook", amount: 2, movingRange: "2468", movingSteps: 99}
object 3: {name: "Bishop" amount: 2, movingRange: "1379", movingSteps: 99}

```shell
    db.chess.insertMany([{name: "King", amount: 1, movingRange: "12346789", movingSteps: 1}, {name: "Rook", amount: 2, movingRange: "2468", movingSteps: 99}, {name: "Bishop" amount: 2, movingRange: "1379", movingSteps: 99}])
```