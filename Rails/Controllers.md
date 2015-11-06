# Controllers

```
class ModelsNameController < ApplicationController
  ...
end
```
## ACTIONS
```
def index     # list all records
def show      # display a single record
def new       # display a new record form
def edit      # display an edit record form
def create    # create a new record
def update    # Update a record
def destroy   # Delete a record
```

## Action Examples
```
def show
  @record = ModelName.find(:id)
end
```
corespond to: views/modelName/show.html.erb
```
<%= @record.name %>
```

```
def edit
  @record = ModelName.find(params[:id])
end
```

**@** : to grand views access to variables (Instance Variable)

## Render a different view
```
def show
  @record = ...
  render action: 'viewName'
```

## Accepting Parameter
```
params = {hash}
```
```
def show
  @record = Model.find(params[:id])
end
```
## Parameters
we are required to use **Strong Parameters**
```
require(:param)
permit(:param)
```
```
@record = ModelName.create(params.require(:param_key_level_1) permit(:param_key_level_2))
@record = ModelName.create(params.require(:param_key_level_1) permit([:param_key_level_2, :param_key_level_2]))
```

## Before Action
```
before_action :check_auth
before_action :method_name, only: [:edit, :update, :destroy]

def method_name
  @record = ModelName.find(params[:id])
end

def check_auth
  if session[:user_id] != @record.user_id
    flash ...
    redirect ...
  end
end

def edit

end

def update

end

def destroy

end
```
