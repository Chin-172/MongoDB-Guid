# Task 2 - Funny Querry

Hi, noivce! Congratulations! You completed your first task, but here is no way to stop it! We received the second task immediately. This time we will insert a new data and also using some query commands to list out the data we want to show.

**NOTE** Before we continue, we clean up our CLI first. Use command `cls` to do so.

|  Customer ID	|   Customer Name	|  Age	|   Address 	|   Phone Number	|
|---	|---	|---	|---	|---	|
| C0001	|   Jally	|   19	|  Flat A , 25/F, Acacia Building, 150 KennedyRoad, Wai Chai, HK 	|   +852 2222 3333	|
| C0002	|   Kenny	|   32	|  Rm 02, 12/F, Boilly Building, 128 Queen's Road, Central, HK  	| +852 1111 2222  	|
| C0003 	|   Tony	|   25	|  Flat A, 12/F, Kowloon Government Offices, 405 Nathan Road, Yau Ma Tei, Kowloon, HK 	|   +852 3333 5555	|
| C0004 	|   Candy	|   21	| 	|   +852 6666 2255	|
| C0005 	|   Tommy	|   21	| Flat C, 21/F, HappySunny Building, 89 Sanny Road, Fake Address, Null Country	|   +852 6666 2255	|

Step 1: Insert Candy's & Tommy's data
<br>

Step 2: List out the data by sorting Address descending
<br>

Step 3: Find out the two older members and show out with name only (no _id)
<br>

db.users.find({}).sort({Address: -1})

db.users.find({}, {CustomerName: -1, _id: 0}).sort({Age: -1}).limit(2)