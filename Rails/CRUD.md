#CRUD

##Hash
```
variable = {key: value}
variable = var[:key] || var.key
```

puts?

##CRUD:
### Read
```
TableName.find(id)

TableName.find(id1, id2, id3) // returns an array of rows
```
```
TableName.first
TableName.last
TableName.all
TableName.count
TableName.order(:key)
TableName.limit(number)
TableName.where(key: value)
```
chaining
```
TableName.where(key: value).order(key).limit(number)
```

### Create
```
t = TableName.new
t.key = value
t.save
```
```
t = TableName.new(hash)
t.save
```
```
TableName.create(hash)
```

### Update
```
t = Table.find(id)
t.key = value
t.save
```
```
t = TableName.find(id)
t.attributes = hash
t.save
```
```
t = TableName.find(id)
t.update(hash)
```
### Delete
```
t = Table.find(id)
t.destroy
```
```
TableName.find(id).destroy
```
```
TableName.destroy_all
```
