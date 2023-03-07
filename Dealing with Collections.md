blog> show collections // command used to show the {collections} in the current Database
posts // Response shows all the collections

---

blog> show collections
posts
blog> db.createCollection("users") // command used to Create new Col
{ ok: 1 } // Response confirms that 1 new collection created
blog> show collections
posts
users

---

blog> show collections
posts
users
blog> db.users.drop() // command used to Delete a collection
true // Response confirms the Delete
blog> show collections
posts

---

