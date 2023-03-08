**SQL & NoSQL:**

SQL:
--- (Structured Query Language).
--- Its Database contains {Columns or Fields} and {Row or Record}.
--- Example of Sql: MySQL.

NoSQL:
--- (Not Only Structured Query Language).
--- There's different types of NoSQL, Such as the {Document Store}.
--- Example of NoSql: MongoDB.
--- The Documents Store contains {Document} written using JSON
--- The Document does not need to has fixed structure, while this is the case in SQL, means for each {Record} you add, it must contain all the {columns} in the table.

Terms:

- {SQL}: Database, Table, Row, Column, Index
- {MDB}: Database, Collection, Documents, Field, Index

Documents:

A record in MongoDB is a document, a data structure consisting of field and value pairs MongoDB documents are identical to JSON objects and field values may include other documents, arrays or an array of documents.

Advantages of using documents instead of tables:

- Documents are compatible with native data shapes and types in many programming languages.
- Embedded documents and arrays reduce the need for complex joins.
- The non-static schema supports polymorphism fluently.

Aggregation:

- count()
  The count() method is used to retrieve the number of documents that match a given set of query conditions. The syntax for the count() method is as follows: db.collection.count(query, options);

* Here, query is an optional parameter that specifies the query conditions, and options is an optional parameter that specifies additional options such as the maximum number of documents to count or the maximum time to allow for the operation.

- sort()
  The sort() method is used to sort the documents in a collection based on one or more fields. The syntax for the sort() method is as follows: db.collection.find(query, projection).sort(sorting_order);

* Here, query is an optional parameter that specifies the query conditions, projection is an optional parameter that specifies the fields to include or exclude from the results, and sorting_order is a required parameter that specifies the sorting order.

- limit()
  The limit() method is used to limit the number of documents returned by a query. The syntax for the limit() method is as follows: db.collection.find(query).limit(limit);

* Here, query is an optional parameter that specifies the query conditions, and limit is a required parameter that specifies the maximum number of documents to return.

- Add-Feild
  To add a field to a document in MongoDB, you can use the update() method with the $set operator. The syntax for the update() method is as follows: db.collection.update(query, update, options);

* Here, query is a required parameter that specifies the query conditions to select the document(s) to update, update is a required parameter that specifies the modification to apply, and options is an optional parameter that specifies additional options such as whether to create a new document if the query doesn't match any existing documents.
  To add a new field to a document, you can use the $set operator with the new field name and value. For example, to add a new field called "email" with the value "john.doe@example.com" to a document in the "users" collection where the "_id" field is "12345", the following code can be used: db.users.update({_id: "12345"}, {$set: {email: "john.doe@example.com"}});

---

# Relationships:

There are 3 types of relationships to be dealt with:

- 1:1 (one-to-one) relationship,
- 1:m (one-to-group) relationship,
- m:m relationship (group by group).

# There are two ways to apply binding:

1. Embedded

- It is a method of linking the two files to each other by including a (Document) file inside a (Document) file. It is often preferable to use this method if the linking relationship is one-to-one because it helps to retrieve two files with only one query, which contributes to increasing Efficiency of the query process.

2. Using \_id

- The traditional way of joining two files from two different groups and related to each other using a single field.

# One-to-many relationship

Describes a data model that uses embedded documents to describe a one-to-many relationship between connected data.

> There are two ways to apply this link:

- Type 1 (Normalization):
- Type 2 (Deormalization):
