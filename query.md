Tutte le risorse con isActive a true

Query:  {isActive: true}
Result: 51 records

Tutte le risorse con Age > 26
Query:  {age: {$gt: 26}}
Result: 54 records

Tutte le risorse con Age > 26 e Age <= 30
Query:  {$and: [{age: {$gt: 26}}, {age: {$lte: 30}}]}
Result: 19 records

Tutte le risorse con Eyes brown o blue
Query:  {$or: [{eyeColor: {$eq: "blue"}}, {eyeColor: {$eq: "brown"}}]}
Result: 66 records

Tutte le risorse con Eyes diverso da green
Query:  {eyeColor: {$ne: "green"}}
Result: 66 records

Tutte le risorse con Eyes diverso da green e diverso da blue
Query:  {$and: [{eyeColor: {$ne: "green"}}, {eyeColor: {$ne: "blue"}}]}
Result: 35 records

Tutte le risorse con company uguale a FITCORE, restituire solo l'email
Query:  db.collection("M6W2D1").find({company: "FITCORE"}).project({email:1})
Result: 1 record