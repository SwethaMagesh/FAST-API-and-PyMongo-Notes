# MongoDb
- DB -> Collections -> Documents
- Each doc has an id
- Local or hosted in AWS etc.
- GUI for local -> **MongoDb compass**
- MongoEngine => py library for connecting and typecasting to class

## Mongo cluster and Pymongo
- [Mongo DB](mongodb.com)
- Create cluster in free tier and copy connection string for python linking
- Whitelist IP and create password
- pymongo library
    - `from pymongo import MongoClient`
    - `cluster = MongoClient('connection string')`
    - `db = cluster['dbname']`
    - `collection = db['collectionname']`
    - `collection.insert_one(doc)`
    - `collection.find({"key":"value","key1":"regex"})`
- methods are 
    - insert_one, insert_many
    - find (returns cursor obj, iterate thru it), find_one
    - delete_one, delete_many
    - update_one, update_many
    - count_documents 
    - $set, $inc, $max etc. in update available. 

## Explore more: 
- cursor object
- find_one finds first or only one? are there ordered docs?
- _id in doc (create or random  - which is better)
- capped collections
