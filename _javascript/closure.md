---
layout: collection
title: "Closure"
category: javascript
---

Closures have been one of those concepts in Javascript that I honestly had a hard time wrpaping my mind around. I think I've finally got a handle on what exactly a closure does.

First here is an example of a closure:

```javascript
function sayMyName(firstName){
  return function(lastName){
    return firstName + " " + lastName;
  };
}

var sayMyNameSayMyName = sayMyName("Michael");
console.log(sayMyNameSayMyName("Lee"));

// -> Michael Lee
```

As you can see in the function above, a local variable isn't needed. In closures, the `function` keyword "freezes" the code in its body. What this allows you to do is then later, restore that code to be used with another variable as a parameter. In the example above, the `lastName` variable.
