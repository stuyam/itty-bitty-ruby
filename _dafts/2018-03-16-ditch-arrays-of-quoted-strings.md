---
layout: post
title:  "Ditch Arrays of Quoted Strings"
---
This is a common things you see in Ruby.
```ruby
array = ['This', 'Is', 'An', 'Array']
```
A simpler and more concise way to write this would be.
```ruby
array = %w(This Is An Array)
```
It will be converted to the same as the first example, but with a simpler syntax. I also find that it is easier to read and easier to edit in the future.

***
Using an uppercase `%W` is like using double quoted strings than you can string interpolate in.
```ruby
name = 'Alyssa'
# array = ["#{name}able", "Stuartable", "Christianable", "Johnable"]
array = %W(#{name}able Stuartable Christianable Johnable)
# both return ['Alyssaable', 'Stuartable', 'Christianable', 'Johnable']
```
The same is true for lowercase vs. uppercase `%i` vs `%I` for creating arrays of symbols.
```ruby
var = 'wow'
array1 = %i(wow this is cool)
array2 = %I(#{var} this is cool)
# both return [:wow, :this, :is, :cool]
```
