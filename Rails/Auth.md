# Auth

```
if session[:user_id] != @record.user_id
  flash[:notice] = "sorry, you don't have access to this page"
  redirect_to(another_path)
  # or
  redirect_to(another_path, notice: "sorry, you don't have access to this page")
end
```

**session** a per user hash
**flash[:notice]** to send messages to the user
**redirect_to <path>** to redirect the request


## flash
```
# in view
<% if flash[:notice] %
  <div> <%= flash[:notice] %> </div>
<% end %>
<%= yield %>
```
