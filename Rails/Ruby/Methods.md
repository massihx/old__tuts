# Methods

## Optional Arguments
```
def fn(name, age=nil)
	...
end
```


## Exceptions
```
raise AuthorizationException.new

begin
	# call the method
rescue AuthorizationException
	warn "you are not authorized to access this list"
end


## Splat Argument
> passing multiple strings instead of array
```
def fn(name, *array)
	...
end

fn('name', 'arr1', 'arr2')
```
