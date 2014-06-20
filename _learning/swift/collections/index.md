---
layout: post
title:  "Swift: Collections"
---

## Arrays
Arrays can only store values of the same type. In order to tell the type it is allowed to store use the syntax `SomeType[]`

var shoppingList: String[] = ["Eggs", "Milk"]

If an array is initialized with the same type, it is inferred of that type without telling what type it can store.

var shoppingList = ["Eggs", "Milk"]

### Array Methods, Properties and Subscripts

shoppingList.count // Returns the read-only count property
shoppingList.isEmpty

### Adding New Items
shoppingList.append("Chocolate")
shoppingList += "Chocolate"
shoppingList += ["Chocolate", "Strawberries", "Bread"]

### Adding with Subscript Syntax
var firstItem = shoppingList[0]

shoppingList[0] = "Six eggs" // Replaces first item in list

shoppingList[4...6] = ["Bananas", "Ice Cream"]

shoppingList.insert("Maple Syrup", atIndex: 0)

shoppingList.removeAtIndex(0) // Will return removed item and array is updated so that item at position 1 is now at position 0

shoppingList.removeLast()
