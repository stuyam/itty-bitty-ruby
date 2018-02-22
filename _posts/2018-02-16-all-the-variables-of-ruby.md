---
layout: post
title:  "All the Variables of Ruby"
---
In ruby there are *six* different types of variables. Some very obscure and rarely used, but interesting to know.

### Local Variable
Used in the scope of a method or other local usage.
```ruby
name = 'stuart'
```

### Constant
Usually used as a value that it set once to set a default or reusable value. They use all caps as a convention.
```ruby
class Person
  TYPES = [:admin, :user].freeze
  # hint use the freeze method to make constants immutable
end
```

### Instance Variable
Saves a values to the instance of a class.
```ruby
def name=(name)
  @name = name
end
```

### Class Variable
Saves a value to the class itself. Works almost like a class constant.
```ruby
def self.count_plus_one
  @@count += 1
end
```

### Global Variable
A variable that can be accessed anywhere from within the program. Admittedly I have never seen these used. Perhaps it makes more sense to make a class, nevertheless it's worth mentioning.
```ruby
$access_me_anywhere = 42
```
