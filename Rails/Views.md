# Views

**Evaluate**
```
<% row = TableName.find(id) %>
```

**Evaluate & Print result**
```
<h1><%= row.key %></h1>
```

**Yield**
```
<%= yield %>
```

**Linking**
```
<%= link_to name, link %>
<%= link_to row.parent.name, parent_path(row.parent) %>

<%= link_to text_to_show, model_instance %>
```
*  Find options we can use with link_to

**Loop, each**
```
Model.all.each do |instance_name|

<% Model.all.each do |model_name| %>
  <%= model_name.key %>
  ...
<% end %>
```
```
Model -> Class
Model.all -> Array of hashes
instance_name -> single hash (row)
```
**Handle empty models**
```
<% models_name = Model.all %>
<% models_name.each do |model_name %>
  ...
<% end %>
<% if models_name.size == 0 %>
  <p> no result </p>
<% end %>
```

**Edit & Delete**
```
<%= link_to "Edit", edit_model_path(model_name) %>
<%= link_to "Delete", model_name, method: :delete %>
```
