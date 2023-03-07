test> show dbs // command used to show all the Databases
admin 40.00 KiB
config 84.00 KiB
local 88.00 KiB
lwn> use blog // command used to Create/Select Database
switched to db blog // Response confirm the create of the db
blog> db // command used to show the current db you in
blog
blog> use admin // command used to Switch from {blog} to {admin} db

---

admin> show dbs
admin 40.00 KiB
blog 8.00 KiB
config 96.00 KiB
local 88.00 KiB
admin> use blog
switched to db
blog> db.dropDatabase() // command used to Delete current Database
{ ok: 1, dropped: 'blog' } // Response confirming the Delete
blog> show dbs
admin 40.00 KiB
config 96.00 KiB
local 88.00

---
