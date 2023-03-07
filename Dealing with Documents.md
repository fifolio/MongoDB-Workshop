blog> show collections
posts
users
blog> db.users.find({}) // show all the data inside a collection
[
{
_id: ObjectId("6407705c0e58f1b2e073a291"),
name: 'ahmed',
age: '9'
},
{ _id: ObjectId("6407708c0e58f1b2e073a292"), name: 'Jad', age: '12' },
{
_id: ObjectId("640770970e58f1b2e073a293"),
name: 'omar',
age: '23'
}
]
blog> db.users.find({age: "12"}) // find and show specific data from collection
[
{ _id: ObjectId("6407708c0e58f1b2e073a292"), name: 'Jad', age: '12' }
]

---

blog> show collections
posts
users
blog> db.users.find().pretty() // used to make the response look sorted
[
{
_id: ObjectId("6407705c0e58f1b2e073a291"),
name: 'ahmed',
age: '9'
},
{ _id: ObjectId("6407708c0e58f1b2e073a292"), name: 'Jad', age: '12' },
{
_id: ObjectId("640770970e58f1b2e073a293"),
name: 'omar',
age: '23'
}
]

---

blog> show collections
posts
users
blog> db.users.find()
[
{
_id: ObjectId("6407705c0e58f1b2e073a291"),
name: 'ahmed',
age: '9'
},
{ _id: ObjectId("6407708c0e58f1b2e073a292"), name: 'Jad', age: '12' },
{
_id: ObjectId("640770970e58f1b2e073a293"),
name: 'omar',
age: '23'
}
]
blog> db.users.insertOne({name: "Firas", age: 23}) // Add new Document to the collection
{
acknowledged: true, // Response confirms the Addition
insertedId: ObjectId("640772d90e58f1b2e073a294")
}
blog> db.users.find() // Show the Documents in the Collection
[
{
_id: ObjectId("6407705c0e58f1b2e073a291"),
name: 'ahmed',
age: '9'
},
{ _id: ObjectId("6407708c0e58f1b2e073a292"), name: 'Jad', age: '12' },
{
_id: ObjectId("640770970e58f1b2e073a293"),
name: 'omar',
age: '23'
},
{ _id: ObjectId("640772d90e58f1b2e073a294"), name: 'Firas', age: 23 }
]

---

blog> db.users.find()
[
{
_id: ObjectId("6407705c0e58f1b2e073a291"),
name: 'ahmed',
age: '9'
},
{ _id: ObjectId("6407708c0e58f1b2e073a292"), name: 'Jad', age: '12' },
{
_id: ObjectId("640770970e58f1b2e073a293"),
name: 'omar',
age: '23'
},
{ _id: ObjectId("640772d90e58f1b2e073a294"), name: 'Firas', age: 23 }
]
blog> db.users.insertMany([ // Used to add Many Documents to the Collection
... {name: "criss", age: 32}
... , {name: "Elian", age: 42},
... { name: "Jaddian", age: 25}
... ])
{
acknowledged: true,
insertedIds: {
'0': ObjectId("640774300e58f1b2e073a295"),
'1': ObjectId("640774300e58f1b2e073a296"),
'2': ObjectId("640774300e58f1b2e073a297")
}
}
blog> db.users.find()
[
{
_id: ObjectId("6407705c0e58f1b2e073a291"),
name: 'ahmed',
age: '9'
},
{ _id: ObjectId("6407708c0e58f1b2e073a292"), name: 'Jad', age: '12' },
{
_id: ObjectId("640770970e58f1b2e073a293"),
name: 'omar',
age: '23'
},
{ _id: ObjectId("640772d90e58f1b2e073a294"), name: 'Firas', age: 23 },
{ _id: ObjectId("640774300e58f1b2e073a295"), name: 'criss', age: 32 },
{ _id: ObjectId("640774300e58f1b2e073a296"), name: 'Elian', age: 42 },
{
_id: ObjectId("640774300e58f1b2e073a297"),
name: 'Jaddian',
age: 25
}
]
