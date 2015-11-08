# Class

```
class Name
	def initialize(first, last = nil)
		@first = first
		@last = last
	end
	def format
		[@last, @first].compact.join(', ')
	end
end

# using class
def n = Name.new('fname', 'lname')
puts n.format

```

## Getter and Setter
```
attr_accessor :var1, :var2
# =
def var1 = (value)
	@var1 = value
end
def var1
	@var1
end
# same with var2
```

## Read-only attribures - private
```
attr_reader :attribute
```

## Re-opening Classes
> only re-open classes that you yourself own.

## Self
```
	...
	def initialize(name)
		self.name = name
	end
	...
```














