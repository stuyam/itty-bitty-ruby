---
layout: post
title:  "Include vs. Extend"
---
I always get confused as to when to use `include` and when to use `extend` to add a modules methods to a class or instance of a class. Here is how I remember it now.

I will use this module as an example throughout:
```ruby
module Menu
  def items
    [:apps, :drinks, :salads]
  end
end
```

### Include
Include **only** adds methods to an instance of that class.
```ruby
class Food
  include Menu
end

food = Food.new
food.items #[:apps, :drinks, :salads]
```

### Extend
Extend **always** adds the modules methods to the current class or instance. If it's on a class it will add class methods, if it's on an instance of a class it will add instance methods.
```ruby
class Food
  extend Menu
end

Food.items #[:apps, :drinks, :salads]

food = Food.new
food.extend(Menu) #adds module to instance of food
food.items #[:apps, :drinks, :salads]
```
