# Classes

- Every class is also a module
- Classes cannot be mixed-in to anothe module or class.
- Class can be used as a namespace

```ruby
class Name
  # ...
end
```

## Inheritance
```ruby
class Child < Parent
  # ...
end
```

- Dafault *superclass* is **Object**
- **BasicObject** is designed as a *blank class* and includes a minimum of built-in methods.
- Any method defined on a class is callable from its subclass

## Redefining methods in subclass
```ruby
class A
  def x
    1
  end
end

class B < A
  def x
    2
  end
end

B.new.x # => 2
```

## Super
- When used without any arguments **super** uses the arguments given to the subclass
- To send no arguments to the superclass method use **super()**

```ruby
class A
  def x
    1
  end
end

class B < A
  def x
    2 + super
  end
end

B.new.x # => 3
```
## Singleton Class ??
singleton, metaclass, eigenclass
It is a class that holds methods for only that instance.

```ruby
class C
  # ...
end

class << C
  # self is the singleton class here
end
```

```ruby
class C
  class << self
    # ...
  end
end
```

















