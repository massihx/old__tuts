# Methods
```ruby
def method_name
  1 + 1
end
```
## Naming
- The bang methods(! at the end of method name) are called and executed just like any other method. However, by convention, a method with an exclamation point or bang permanently modifies its receiver
- Methods that end with a question mark by convention return boolean
- Methods that end with an equals sign indicate an assignment method. For assignment methods the return value is ignored, the arguments are returned instead

## Operators
| Operator  | Action  |
| :------------: |:---------------|
| +   |add|
| -   |subtract|
| *   |multiply|
| **   |power|
| /   |divide|
| %   |modulud division|
| &   |AND|
| ^   |XOR|
| >>   |right-shift|
| <<   |left-shift, append|
| ==   |equal|
| !=  |not equal|
| ===   |case equality|
| =~   |pattern match|
| !~   |does not match|
| <=>   |spaceship|
| <   |less-than|
| <=   |less-than or equal|
| >   |greater-than|
| >=   |greater-than or equal|

> Unary methods accept zero arguments.
> To define unary methods minus, plus, tilde and not (!) follow the operator with an @ as in +@ or !@:

## Return Value
- By default, a method returns the last expression that was evaluated in the body of the method
```ruby
def method
  a = 1
end

def method
  return 1 + 1
  ...
end
```

## Scope
Instance Method:
```ruby
class C
  def my_method
    # ...
  end
end
```
Class Method: a method that is defined on the class, not an instance of the class
```ruby
class C
  def self.my_method
    # ...
  end
end
```
Adding a method to an object
```ruby
greeting = "Hello"

def greeting.broaden
  self + ", world!"
end

greeting.broaden # returns "Hello, world!"
```

> **self** is a *keyword* referring to the current object under consideration by the compiler.

## Singleton Method
??

## Overriding
When Ruby encounters the *def* keyword, it doesn’t consider it an error if the method already exists: it simply redefines it. This is called **overriding**.

## Arguments
- The argument is a local variable in the method body
- The parentheses around the arguments are optional
```ruby
def add_one(value)
  value + 1
end

def add_one value
  value + 1
end
```

## Default Values
```ruby
def add_values(a, b = 1)
  a + b
end
```
- The default value does not need to appear first, but arguments with defaults must be grouped together

## Array Decomposition
```ruby
def my_method((a, b))
  # we have 2 local variables a and b
end
```

## Array/Hash Argument
- Prefixing an argument with * causes any remaining arguments to be converted to an Array
- The array argument must be the last positional argument, it must appear before any keyword arguments
- a bare * can be used to ignore arguments

```ruby
def gather_arguments(*arguments)
  p arguments
end

gather_arguments 1, 2, 3 # prints [1, 2, 3]


def ignore_arguments(*)
  # ...
end
```

## Keyword Arguments
```ruby
def add_values(first: 1, second: 2)
  first + second
end
```
- When calling a method with keyword arguments the arguments may appear in any order
- If an unknown keyword argument is sent by the caller an ArgumentError is raised.
- When mixing keyword arguments and positional arguments, all positional arguments must appear before any keyword arguments

## Block Argument
??
```ruby
def my_method(&my_block)
  my_block.call(self)
end

def each_item(&block)
  @items.each(&block)
end

def my_method
  yield self
end

```

## Exception Handling
```ruby
def my_method
  begin
    # code that may raise an exception
  rescue
    # handle exception
  end
end

def my_method
  # code that may raise an exception
rescue
  # handle exception
end
```













