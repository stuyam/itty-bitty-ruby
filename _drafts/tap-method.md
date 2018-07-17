---
layout: post
title:  'Tap Method'
jumbo: '.tap()'
---
As of Ruby 1.9 there is a `.tap` method on all objects in Ruby. Tap allows you to _tap_ into an object, do something with that object, and automatically return that object. Here is an example.
```ruby
# before
def new_manager
  user = User.new
  user.role = 'Manage'
  user.save!
  user
end

# using tap
def new_manager
  # this returns the newly created user
  User.new.tap do |u|
    u.role = 'Manager'
    u.save!
  end
end
```

A great use case for the `.tap` method is method chaining with methods that don't return self. Say you have a method on a `CreditCard` object `.pay_balance!` that returns true or false if the payment goes through. You also want to get the `.last4` on the card after that to show in the view. You could do something like this as always.
```ruby
credit_card.pay_balance!
last4 = credit_card.last4
```
With `.tap` you could simply do:
```ruby
last4 = credit_card.tap { |card| card.pay_balance! }.last4

# or more simply
last4 = credit_card.tap(&:pay_balance!).last4
```
