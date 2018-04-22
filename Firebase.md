## Documentation Firebase
(First the tuto bellow was often the source of this documentation :https://www.tutorialspoint.com/firebase/firebase_read_data.htm)

### READING/LISTENING:
The function `on` on the cursor given by `.ref()` let you read/listen the database.

!! Be careful of the argument that you give to `ref`. This argument is like the path to the part of the data you need.
Exemple: If you have a database `MyDataBase` with a collection `A` in it, and you want to have a direct acces to `A`, then
your path should be `/MyDataBase/A` which gives you :

`
var ref = firebase.database('/A')
ref.on(MODE, aFunction{})
`

We can mention some of the must current `MODE` / ways of how to listen the database.
They are:

* `value`
* `child_added`
* `child_changed`
* `child_removed`

For more explanaition : https://www.tutorialspoint.com/firebase/firebase_read_data.htm

Warning : Those function DO NOT operate changement on your database, only observe event on it.
