---
layout: post
title:  "Give Arbitrary Numbers Names"
---
It's common to see a like this this.
```ruby
date += 60*60*24
```
I can mostly figure out that is happening, it's adding 24 hours to the date. But why not make it more readable? Here are some examples.
```ruby
hours_24 = 60*60*24
date += hours_24
```
The next example pulls a date range out as a constant that can be reused and only needs to be created once.
```ruby
LABOR_DAY_TO_MEMORIAL_DAY = Date.parse('2018-05-25')..Date.parse('2018-09-03')

def night_in_summer_season? night
  LABOR_DAY_TO_MEMORIAL_DAY.include?(night)
end
```
That way you or someone else doesn't need to lookup the dates every time they come back to this code.
