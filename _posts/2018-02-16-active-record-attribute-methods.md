---
layout: post
title:  "Active Record Attribute Methods"
---
You know these two getter and setter methods that are created when you add a column to a model. Take `name` for example.
```ruby
person.name # nil
person.name = 'stuart'
```
But here is a list of lesser known methods that are automatically created for attributes that you might find useful.
```ruby
person.name?         # Boolean: calls .present? on the attribute (aka. nil, false, or '')
person.name_was      # when updating a record it will return the previously set value
person.name_changed? # Boolean: if the value has changed
person.name_change   # Array: index 0 is the old value, index 1 is the new value
person.restore_name! # set the value back to what it initially set to
```
Want to see a list of all available methods created for each attribute? Run this with your model name and an attribute to find out!
```ruby
# rails c
Person.new.methods.select {|e| e =~ /first_name/}
```
