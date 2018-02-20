---
layout: post
title:  "Pass Rails ENV to Front End"
---
Sometimes you need ENV values from rails in your front end. Maybe `API_BASE_URL` or a `MAPBOX_TOKEN`.
Make an `env.js.erb` file in assets and set it up as follows.
```javascript
var ENV = {
  API_BASE_URL: '<%= ENV['API_BASE_URL'] %>',
  BASE_URL: '<%= ENV['BASE_URL'] %>',
  MAPBOX_TOKEN: '<%= ENV['MAPBOX_TOKEN'] %>',
}
```
Because JS and Ruby are so similar you can access the values the same way you do in Ruby.
```javascript
var token = ENV['MAPBOX_TOKEN'];
```
Note that you need to be careful what values you make available to your front end and make sure you only provide values that can be publicized.
