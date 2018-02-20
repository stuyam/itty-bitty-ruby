---
layout: post
title:  "Safe Method Chaining"
---
Ever do something like this?
```ruby
def street_name
  if user && user.address
    user.address.street
  end
end
```

Well as of Ruby 2.3 you can use the new safe method chaining syntax to prevent you from calling an undefined method on nil. Just add a `&` after each object you are unsure of if it will be nil or not.
```ruby
def street_name
  user&.address&.street
end
```
If either `user` or `address` is `nil` it will stop calling methods and just return nil. This has been a similar feature in Rails for a long time using the `try` method.
```ruby
def street_name
  user.try(:address, :street)
end
```
