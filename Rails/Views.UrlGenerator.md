# URL Generator

```
<%= link_to text_to_show, code %>
```

```
| Action  | Code  | URL |
| :------------ |:---------------| :-----|
| List all records  | records_path            | /records          |
| New record form   | new_record_path         | /records/new      |
| Show a record     | record                  | /records/:id      |
| Edit a record     | edit_record_path(record)| /records/:id/edit |
| Delete a record   | record, method: :delete | /records/:id      |
```
