---
layout: post
title:  'Double Negatives'
jumbo: '.blank?'
---
The `unless` keyword can be hard to read. It can set yourself up some weird double negative scenarios.
Instead of
```ruby
unless @user.name.blank?
  # do something
end
```
try
```ruby
if @user.name.present?
  # do something
end
```

If you find yourself using a `bang`! to negate a call with `.blank?` or `.present?` in it, just remove the `bang`! and swap the methods.

In Rails there are the `.blank?` and `.present?` methods to determine if a value is nil, false, or an empty string. Same goes for enumerables like an array with the `.any?` and `.empty?` methods.
