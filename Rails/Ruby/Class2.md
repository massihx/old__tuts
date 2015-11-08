# Class 2

## Encapsulation
??

## Visibility
```
def fn1
	...
end

private | protected

def fn2
	...
end

# fn1 is public
# fn2 is private
```
> private methods cannot be called with explicit receiver
> protected: hidden from outside but accessible from other instances of same class

## Inheritance
```
class parent
	...
end

class child < parent
	..
end

```

## Super
> to call the parent method, after being overridden in the child class
> if you call super with no params, it will automatically pass in the arguments that were passed to the child method
```
super(params) # looks for a method by the same name in one of the parent classes, and excute it
```










