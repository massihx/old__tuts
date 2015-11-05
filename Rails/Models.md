#Models
> app/models/modelNameS.rb

> table: lowercase, plural
> model: upercase, singular

```
class TableName < ActiveRecord::Base
    ...
end
```

## Validation
```
validates_presence_of :key
validates_numericality_of :key
validates_uniqueness_of :key
validates_confirmation_of :key //password
validates_acceptance_of :key //checkbox
validates_length_of :key, minimum: number
validates_format_of :key, with: /regex/i
validates_inclusion_of :key, in: 21..99 //between 2 values
validates_exclusion_of :key, in: 0...21, message: "msg"
```
```
validates :key, presence: true
validates :key, length: {minimum: number}
```
```
validates :key,
presence: true,
length: {minimum: number}
```
```
presence: true
uniqueness: true
numericality: true
length: {minimum: 0, maximum: 100}
format: {with: /regex/}
acceptance: true
confirmation: true
```
```
## Relationships - mapping
> has_many: tableName (lowercase, plural)
> belongs_to :tableName (lowercase, singular)

```
t1 = ParentTable.find(id)
t2 = ChildTable.create(key: value, foreignKey: t1)
```
```
t1.childTableS // array
t1.childTableS.count
```
```
t2.parentName
t2.parentName.key
```
