# notes-careertrack-13.md
### Mongo Aggregations
* behaviour acts like a pipe
* the pipeline has different stages and each stage transforms the data, some stages produce new documents and/or filter out documents.
* db.collection.aggregate() is the method. 

| findAndModify | Update |
| ------------- | ---------------- |
db.collection.findOneAndUpdate() | |
db.collection.findAndModify() |  db.collection.updateOne()
| |db.collection.updateMany()<br>
| | db.collection.update()<br>| | Bulk.find.update()<br>
| | Bulk.find.updateOne()<br>
| | Bulk.find.upsert()<br>
* example $match(first filter and must be the first) => $sort(can filter if preceded by $project, $unwind, or $group) => $group(preceded by $sort) => $first
* if aggregation requires subset of data $match => $limit => $skip used at the beginning to limit data.
* aggregation provides alternative to map-reduce function. 
* 
#### Aggregations by Example
* MongoDB aggregation is a tool which is a set of functions with the purpose of manipulating data coming from the MongoDB query.
* one function <i>aggregate</i> accepts and array then transforms the data according to what defined transformations. (Matching, group, sum, min max avg, etc)
* $gte: (greater than)
* $lt: (less than)
total: adds ($sum:) total of groups with same ID
* $avg: average
* $min: minimum
* $max: maximum 

