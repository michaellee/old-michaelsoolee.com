---
layout: post
title:  "Swift: Operators"
---

## Increment and Decrement Operators
A value can be incremented or decremented with ++ or --. Either in the front of the value or after.

```javascript
var i = 0
i++
// i is now 1
```

The increment and decrement operators not only update the value but also returns a value.

```javascript
var i = 0
var j = i++
// i is 1 and j is 0
```

This is because when if ++ is after a value, it returns first then increments

```javascript
var i = 0
var j = ++i
// i and j are both 1
```

It is recommended that unless you need the specific behaviour of i++, you should use ++i and --i in all cases, since they have the typical behaviour of modifying and returning the result.

## Ternary Conditional Operator
Syntax for ternary operators:

```javascript
question ? answer1 : answer2
```

If `question` is true return answer1 else return answer2

## Ranged Operators

### Closed Range Operator
`(a...b)` defines a range from a to b and includes a and b.

### Half-Closed Range Operator
`(a..b)` defines a range from a to b but doesn't include b.