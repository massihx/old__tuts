# Modules

- Modules are used for namespacing and mix-in functionalities
- A module may be reopened any number of times to add, change or remove
- It is best to only reopen classes you own


```ruby
module Name
  # ...
end
```

## Nesting
```ruby
module Outer
  module Inner
    # ...
  end
end

module Outer::Inner::GrandChild
  # ...
end
```

## Scope
**self**
- It refers to the object that defines the current scope
- It will change when entering a different method or when defining a new module

**Constants**
```ruby
module A
  x = 1

  module B
    # has access to 'x'
  end
end

module A
  x = 1
end
module A::B
  # doesn't have access to 'x'
end
```

## Methods
- A method on a module is called a 'class method'
- Class Methods can be called directly

## Visibility
- **Public:** default, may be called from any other object
- **Private:** can't be called with a receiver
- **Protected:** sender must be a subclass of receiver or receiver must be a subclass of sender























