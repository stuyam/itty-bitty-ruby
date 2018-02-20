---
layout: post
title:  "Rails String Inflections"
---
Here is a quick cheat sheet of the Rails string inflector methods. There are more but these are all the methods that end in _ize_ which are the string transformers.

### Camelize
```ruby
'stuart_yamartino'.camelize # => 'StuartYamartino'
'stuart_yamartino'.camelize(:lower) # => 'stuartYamartino'
'account/profile_controller'.camelize # => 'Account::ProfileController'
```
### Constantize
```ruby
'Module'.constantize # => Module (note it returns an actual constant)
```
### Dasherize
```ruby
'stuart_yamartino'.dasherize # => 'stuart-yamartino'
```
### Demodulize + Deconstantize
```ruby
'Account::ProfileController'.demodulize # => 'ProfileController'
'Account::ProfileController'.deconstantize # => 'Account'
```
### Humanize + Titleize
```ruby
'tacos_for_breakfast'.humanize # => 'Tacos for breakfast'
'tacos_for_breakfast'.titleize # => 'Tacos For Breakfast'
```
### Parameterize
```ruby
'This is for a url.'.parameterize # => 'this-is-for-a-url'
```
### Pluralize + Singularize
```ruby
'taco'.pluralize # => 'tacos'
'octopus'.pluralize # => 'octopi'

'tacos'.signularize # => 'taco'
'octopi'.singularize # => 'octopus'
```
### Tableize
Get the corresponding table name for a model.
```ruby
'AdminUser'.tableize # => 'admin_users'
```
