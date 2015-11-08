# Models - Best Practices

## Create Models
```
rails g model <modelName> <field:type> <field:type>
```
it creates a migration file db/migrate/*.rb

## Model Class
```

```

## Migration Class
```
class name < ActiveRecord::Migration
    def change
        create_table :nameS do |t|
            t.integer :table_id
            t.string :name
        end
        add_index :nameS, :id # adding a foreign_key index
    end
end
```

## Named Scope

```
# in model
class ModelName < ActiveRecord::Base
	scope :name, query|value
	scope :name, where(field: value)
	scope :name, where("field < 10")
	scope :name, order("field desc").limit(3)
end

# in controller
...
@name = ModelName.scope_name
@name = ModelName.scope_name.limit(5)
@name = ModelName.scope_name1.scope_name2

```

## Callbacks
```
before_save :method_name

def method_name
    ...
    if field1 > 10 # reading variables doesn't need 'self'
        self.field2 = true # setting attributes needs 'self'
    end
    ... 
end
```
> if callback returns false, the action will halt/stop

### List of Callbacks
- before_validation
- after_validation
- before_save
- after_save
- before_create
- after_create
- before_update
- after_update
- before_destroy
- after_destroy

### Common Callbacks
- after_create :send_welcome_email
- before_save :encrypt_password
- before_destroy :set_deleted_flag

## Relationships

### has_one
    





