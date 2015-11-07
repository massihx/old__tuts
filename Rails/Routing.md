# Routing

```
AppName::Application.routes.draw do
  resources :models # restful routing
end
```

## Custom Routes
```
get '/path' => 'controllerNames#actionName'

```

## Naming routes and linking to them from views
```
get '/path' => 'controllerName#actionName', as: 'path_name'

# in views
<%= link_to "Text", path_name_path %>
```

## Redirection
```
get '/path' => redirect('/another_path')
get '/google' => redirect('http://bing.com/')
```

## Root Route
```
root to: "controller#action"

# in views
<%= link_to "Home Page", root_path %>
```

## Route Parameters
```
get '/path/:param' => 'controller#action'
```

```
get ':name' => 'controller#action', as 'user_page'
