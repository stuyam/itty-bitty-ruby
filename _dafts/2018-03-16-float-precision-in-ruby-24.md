---
layout: post
title:  'Float Precision in Ruby 2.4'
jumbo: '.floor(2)'
---
As of **Ruby 2.4** you can now set a precision for floats with the `#round`, `#ceil`, `#floor`, and `#truncate` methods.
```ruby
8.55.ceil(1) # => 8.6
8.55.floor(1) # => 8.5
8.55.round(2) # => 8.55
8.555.truncate(1) # => 8.55
```
You can do the same on Integers to coerce them to floats with N number of decimals.
```ruby
12.ceil(1) # => 12.0
12.floor(2) # => 12.00
```
