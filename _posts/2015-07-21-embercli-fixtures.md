---
layout: post
title: "How ember-cli handles fixtures"
category: 'work'
---

I've been really digging how ember-cli structures an ember.js project. One of the things I ran across yesterday was how ember-cli handles fixtures. Instead of the [traditional way of setting up fixtures](http://guides.emberjs.com/v1.11.0/models/the-fixture-adapter/), ember-cli sets up what they call a `http-mock`. What this does is first install an express server and then sets up an API located at `baseurl:4200/api/`.

This is useful since your application will eventually be hooked up to an API, it allows you to setup your routes to perform HTTP requests via the API. I'm assuming the ember.js team is also pushing for this, as the documentation on fixtures has been absent from their documentation since version 1.12.0 and up.

To generate a http-mock, you can execute this command using the ember command-line tool, `ember generate http-mock route-name`. From there you can setup fixture data using the files located at *server/mocks/route-name.js*. The routes could also be accessed via the browser but navigating to http://localhost:4200/api/route-name.

Documentation on http-mock could be [found on the ember-cli page](http://www.ember-cli.com/user-guide/#mocks-and-fixtures) but I found the documentation to be sparse. Doing a Google search yielded better explanation about this feature.