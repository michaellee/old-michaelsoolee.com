---
layout: collection
title: 'Functions'
category: javascript
---

Functions are defined as:

```javascript
var sayHello = function(name){
  console.log("Hello " + name);
};
```

## Function Declaration
The syntax for `function declarations` is:

```javascript
function hello(name){
  console.log("Hello " + name);
}
```

A function delcaration doesn't have the ending semi-colon and function declarations could be called above where the function is defined. This is because function declarations _are not part of the regular top-to-bottom flow of control_.

Function declarations are conceptually moved to the top of their scope and is available for use by all the code in the scope.