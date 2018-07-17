---
layout: post
title:  'Keyword Arguments'
jumbo: 'keywords:'
---
In Ruby 1.9 and below you would probably do something like this if you wanted an options hash in a method.
```ruby
def update(options = {})
  force = options.fetch(:force, false)
  run_some_thing! if force
end

update(force: true)
```

As of Ruby 2.0 and above you can simplify this process.
```ruby
def update(force: false)
  run_some_thing! if force
end

update(force: true)
```

In addition to that, as of Ruby 2.1 you can add required keyword arguments if you don't want optional values.
```ruby
def update(force:)
  run_some_thing! if force
end

update(force: true)
```

Using this pattern has a few benefits. The first being self documenting code. What would it mean if you didn't use an options hash / keyword arguments and you called `update(true)`? You would have to go into the method to see that it does a force.

Another benefit is the future proofing. If you had the method `update_with_force(true)` maybe it is clearer what the argument does. But say in a year from now you want to add another argument to set some property and you want it required? With keyword arguments that might looks something like this.

```ruby
def update(property:, force: false)
  self.name = property
  run_some_thing! if force
end
```

As you can see another benefit is order doesn't matter so when you add more arguments you can put them in any order you prefer.
