# firebase-javascript-interface@1.1.5

Functions to use firebase cloud firestore database like CRUD (Create Read Update Delete)

## Functions (Now using firebase-admin)

# initialize(serviceAccount)

_To initialize the database with service account json_

Params:

- serviceAccount {object} service account json

# insert(table, value)

_To insert new objects to the db_

_If the collection doesn't exist, it will be created, the Id is generated by firestore_

Params:

- table {string} the collection path ex: "users"
- value {object} the object to save ex: { user: "sito"}

# update(table, key, value)

_To update an element_
Params:

- table {string} the collection path ex: "users"
- key {any} the query to find the element ex: ["id", "equal", "sito"]
- value {object} the object to save ex: { user: "sito"}

_See firestore [queries structure](https://cloud.google.com/firestore/docs/query-data/get-data)_

# getValue(table, rQuery)

_To fetch a single value from db_
Params:

- table {string} the collection path ex: "users"
- rQuery {any} the query to find the element ex: ["id", "equal", "sito"] or [["id", "equal", "sito"],["has", "name"]]

# getTable(table, rQuery, page, count)

_To fetch a entire collection_
Params:

- table {string} the collection path ex: "users"
- rQuery {any} the query to find the element ex: ["id", "equal", "sito"] or [["id", "equal", "sito"],["has", "name"]]
- page {number} to begin at page position
- count {number} count of items to obtain (max: 10000)

# deleteDocuments(table, documents)

_To erase elements from a collection_
Params:

- table {string} the collection path ex: "users"
- documents {string[]} array with the list of ids

# deleteCollection

_To clean a entire collection_
Params:

- table {string} the collection path ex: "users"
