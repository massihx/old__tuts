# Assignment

## Local Variable Scope
```ruby
a = 5
```
- A block creates a new scope
- All variables created inside a block, do not leak to the surrounding scope
- Variables defined in an outer scope, appear in inner scope

## Instance Variables
- Instance variables are shared across all methods for the same object
- It must start with **@**
- An uninitialized instance variable has a value of *nil*
```ruby
@instance_variable = 5
```

## Class Variables
- Class variables are shared between a class, its subclasses and its instances
- A class variable must start with **@@**
- Accessing an *uninitialized* class variable will raise a *NameError* exception.
```ruby
@@class_variable = 5
```

## Class variables VS Instance variables
TODO

## Global Variables
- Global variables are accessible everywhere
- They must start with **$**
- An uninitialized global variable has a value of *nil*.

```ruby
$global_variable = 5
```

## Assignment Methods ??
```ruby
def value=(value)
  @value = value
end

value = 2
```
## Abbreviated Assignment
```ruby
a = 1
a += 2
a ||= 0 # makes the assignment if the value was nil or false
a &&= 1 # makes the assignment if the value was not nil or false
```

## Implicit Array Assignment
```ruby
a = 1, 2, 3 # [1,2,3]
a = *[1, 2, 3] # [1,2,3]
a = 1, *[2, 3] # [1,2,3]
```
## Multiple Assignment
```ruby
a, b = 1, 2 # a:1, b:2
a, b = 1, 2, 3 # a:1, b:2
a, *b = 1, 2, 3 # a:1, b:[2,3]
*a, b = 1, 2, 3 # a:[1,2], b:3
```
## Array Decomposition
```ruby
(a, b) = [1, 2] # a:1, b:2
a, (b, c) = 1, [2, 3] # a:1, b:2, c:3
a, (b, *c), *d = 1, [2, 3, 4], 5, 6 # a:1, b:2, c:[3,4], d:[5,6]
```
