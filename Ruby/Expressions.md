# Expressions

## IF
```ruby
if true than
  ...
end

if true
  ...
end

if true
  ...
else
  ...
end

if condition
  ...
elseif condition
  ...
else
  ...
end

# if assignment
def var =
  if condition
    "string"
  else
    "another string"
  end

```

## Ternary If
```ruby
def var = condition ? true : false
```

## UNLESS
unless = if not
```ruby
unless true
  ...
else
  ...
end
```
> Do not use *elseif* with *unless*

## IF && UNLESS Modifier
```ruby
a = 1 if b == 2
a += 1 unless a == 0
```

## CASE
```ruby
case condition
  when pattern
    ...
  when another_pattern then
    ...
  when pattern1, pattern2
  else
    ...
  end

case
  when a == 1
    ...
  when b == 1
    ...
  else
    ...
  end
```

## WHILE
```ruby
while condition do # do is optional
  ...
end
```
> use *break* to end the loop prematurely
> The result of a while loop is *nil* unless *break* is used to supply a value.

## UNTIL
The until loop executes while a condition is false
```ruby
until condition do
  ...
end
```
> the result of an until loop is *nil* unless *break* is used.

## FOR
```ruby
for value in array do
  ...
end
```

## WHILE && UNLESS Modifier
```ruby
a += 1 while a < 10
a -= 1 untill a < 10

begin
  a +=1
end while a < 10
```
> rescue, ensure

## BREAK
**break** is used to leave a block early
```ruby
values.each do |value|
  break if value.even?
  ...
end

while true
  a += 1
  break if a < 10
end

def result = array.each do |value|
  break value * 2 if value.even?
end
```

## NEXT
**next** is used to skip the rest of the *current* iteration
```ruby
def var = array.map do |value|
  next if value.even?
  value * 2
end

def var = array.map do |value|
  next value if value.even?
  value * 2
end
```

## REDO
**redo** is used to redo the *current* iteration
```ruby
while true
  ...
  redo if condition
  ...
end
```
