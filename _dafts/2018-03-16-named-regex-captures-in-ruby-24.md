---
layout: post
title:  "Named Regex Captures in Ruby 2.4"
---
As of **Ruby 2.4** you can now name your regex captures, rather than just using numbers. Name the capture with `?<name>` at the beginning of the capture group. Then you can access it with the `.values_at` methods using a list of symbols.
```ruby
pattern = /(?<year>\d{4})-(?<month>\d{2})-(?<day>\d{2})/
pattern.match('2018-02-16').values_at(:year, :month) # => ['2018', '02']
```
Giving things names makes is easier to come back to, read, and understand.
