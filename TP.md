# MongoDB Cheat Sheet (de ton TP)
## Mongo Shell 
"C:\Program Files\MongoDB\Server\4.2\bin\mongo.exe"

## Command lines
```
show dbs
```
```
use shop
```
```
db.products.insertOne({name:"Book", price : 9.99})
```
db.products.find() db.products.find().pretty()
```
db.products.updateOne({name:"iPhone"},{$set:{ price : 1119.99}})
```
db.products.find({price {$gt :4}})
```
db.products.insertOne({name:"iPhone XS", price : 19.99, details:{ram:"3gb", battery:"2500mAh"}})
```
db.products.find({"details.ram":"3gb"}).pretty()
```
db.products.insertOne({name:"iPhone 11", price : 1200.99, details:{ram:"4gb",
battery: »2500mAh"},tags:["mobile","apple","toto"]})
```
db.products.updateOne({name:"iPhone 11 » },{$addToSet:{tags:"ordi"}})
```
```
db.products.updateOne({tags:"ok"},{$set:{tags.$:"FRANCE"}})
```

