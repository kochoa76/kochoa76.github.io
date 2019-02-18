---
layout: post
title:      "Database Concepts and Review "
date:       2019-02-18 01:45:10 +0000
permalink:  database_concepts_and_review
---

This last week Flatiron School hosted a few interviews with local Houston and Austin companies looking to fill technical roles.  It was a great opportunity for me to assess my skills to date, brush up on concepts, as well as learn entirely new concepts introduced in these interviews. 

New Concepts I was introduced to: 
1. Transactionality
2. Normalization
2. Document Databases / Tradeoffs between relational databases and non relational databases

**Transactionality**
Transactionality is when you use XML scripts to create, update or delete resources within your database, the changes in the portal database are grouped into transactions. All changes that are part of one transaction are either executed completely or not at all. If an error occurs in making a change to the resources, the resource is not updated and/ or created. 

**Normalization**
Database normalization is process used to organize a database into tables and columns.  A table should only contain data that is specific to the topic you are looking to provide data for. 

Normalization is a way to structure your database so that there isn't any extraneous or unrelated data to the result you're looking for. As a result, normalization is a way to minimize duplicate data, reduce data modification issues, and lastly to simplify queries.

**NoSQL vs SQL **

Relational Databases were introduced in 1970's and provided a structured way to organize relationships between objects. An author has many posts and a post belongs to an author for example. But as Big Data, or data that is too diverse, fast-changing or massive for conventional technologies, became more prevalent, new methods of architecting databases have arisen.

NoSQL databases are designed to take advantage of the cloud computing environment. NoSQL databases are natively able to handle load by spreading data among many servers, making them a natural fit for the cloud computing environment (i.e. AWS, Azure). Part of the reason NoSQL databases can do this is that related data is always stored together, instead of in separate tables. This document data model, used in MongoDB and other NoSQL databases, makes them a natural fit for the cloud computing environment.

The other piece that has created a demand for NoSQL databases is the type of data we're working with nowadays. Social media and multimedia has grown rapidly, which typically leaves data unstructured. As a result, NoSQL developed a way to house and manage unstructured data in an easy way. 

Lastly, agile development methods require a need to be able to make quick changes to the schema, which typically can be tedious and time consuming with SQL databases. 

In response to these issues, NoSQL databases were created such as MongoDB that allows for data to be grouped together more naturally and logically, that loosen the restrictions on database schema. 

One of the most popular ways of storing data is a document data model, where each record and its associated data is thought of as a “document”. 
 
**Advantages to document data model: **
 
1.  Documents are independent units which makes performance better and makes it easier to distribute data across multiple servers while preserving its locality.

2. Application logic is easier to write. You don’t have to translate between objects in your application and SQL queries, you can just turn the object model directly into a document.

3. Unstructured data can be stored easily, since a document contains whatever keys and values the application logic requires. In addition, costly migrations are avoided since the database does not need to know its information schema in advance.

4. Document databases generally have very powerful query engines and indexing features that make it easy and fast to execute many different optimized queries. 






