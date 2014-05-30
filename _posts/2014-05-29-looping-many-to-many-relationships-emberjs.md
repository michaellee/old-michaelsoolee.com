---
layout: post
title:  "Looping through many-to-many Relationships in Ember.js"
categories: ember
---

Lately I've been learning how to program with Ember.js &ndash; a MVC Javascript framework. In trying to focus on learning Ember.js alone, I've been relying my data on `FIXTURES`. FIXTURES are a great way to populate some data to be used with your Ember.js application without having to hook up to an API server.

Recently I started a project that dealt with setting up models for many-to-many relationships. Based on <a href="http://emberjs.com/guides/models/defining-models/#toc_many-to-many" target="_blank">Ember.js' documentation</a>, I set up my models and FIXTURES like this:

```javascript
App.Driver = DS.Model.extend({
  name: DS.attr('string'),
  cars: DS.hasMany('car')
});

App.Driver.FIXTURES = [
  {
    id: 1,
    name: "Johnny",
    cars: [1, 3]
  },
  {
    id: 2,
    name: "Sally",
    cars: [1, 2]
  },
  {
    id: 3,
    name: "Carl",
    cars: [2, 3]
  },
  {
    id: 4,
    name: "Kerrigan",
    cars: [1]
  }
];

App.Car = DS.Model.extend({
  name: DS.attr('string'),
  drivers: DS.hasMany('driver')
});

App.Car.FIXTURES = [
  {
    id: 1,
    name: "Station Wagon",
    drivers: [1, 2, 4]
  },
  {
    id: 2,
    name: "Pickup Truck",
    drivers: [2, 3]
  },
  {
    id: 3,
    name: "Electric Coupe",
    drivers: [1, 3]
  }
];
```

```javascript
{% raw %}
<script type="text/x-handlebars" data-template-name="driver">
  <ul>
  {{#each}}
    <li>
      <div class="driver">{{name}}</div>
      <div class="cars">
        {{#each car in cars}}
          {{car.name}}
        {{/each}}
      </div>
    </li>
  {{/each}}
  </ul>
</script>
{% endraw %}
```

You would think this lists out each driver and each of the cars associated to a driver. But it doesn't.

<a href="http://stackoverflow.com/a/23559020/703220" target="_blank">Turns out</a> that when using `FIXTURES` you need to pass a `{ async:true }` flag to the `hasMany` definition to make it an async relationship. According to <a href="http://discuss.emberjs.com/t/what-is-an-async-relationship-async-true-vs-async-false/4107/3" target="_blank">a thread</a> on Ember.js' forums:

> ...when async is true, it will fetch the related entities when you actually request them...

This makes sense because prior to passing the async flag on the `hasMany` definition, I looked at my console and the `Data` tab revealed that the car model had 0 records. Meaning, although I had called a loop to list all the cars attribtued to a driver, the cars weren't being fetched.

So in order to make the inner-loop that's supposed to list the cars for a driver work, we pass the `{ async:true }` flag to `hasMany` in our driver model.

```javascript
App.Driver = DS.Model.extend({
  name: DS.attr('string'),
  cars: DS.hasMany('car', { async:true })
});
```

This now renders a list of drivers with each car that they drive listed below them.