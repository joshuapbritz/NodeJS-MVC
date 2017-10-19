# NodeJS-MVC

This is a boiler plate stater project for NodeJS that tries to implement an MVC (Model View Controller) type of structure. 

## Start up
First you will need to clone the project onto you pc and cd into the directory.

Once you have the project on your computer, run 
```
npm install
```
---
When the packages have been installed, run
```
npm start
```
this will start the server at http://localhost:4500
# What's included
This project includes 
* A File based, database engine
* A paginator
---
## The database
This database include in this project is very simple.
To use it, require it in your file:
```
var database = require('./database/dbo');
```
and connect to a collection
```
var db = database.connectTo('collection-name');
```
now you can use the built in methods to get, save, and delete data
```
db.find()
//Return all records

db.find(v => v.name === 'John')
//Return all records that have the name John

db.findOne(v => v.name === 'John')
//Return the first record with the name John

db.findId(1)
//Return the first with an id of one

db.create({name: 'Jane})
//Creates a record with the name Jane (Id is automatically added)

db.delete(1)
//Delete the record that has the id of one
```
