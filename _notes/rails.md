---
layout: note 
title: Rails 
lastupdated: 2015-11-02  
---

## Strings

### String interpolation

Let's say you have two variables each with a string assigned to them

```
first_name = "Michael"
last_name = "Lee"
```

You can then use these variables with `#{}` to perform a string interpolation.

```
puts "My name is #{first_name} #{last_name}"
```

### Quotes

Single and double quoted strings are nearly identical except that, in Ruby single-quoted strings don't allow for interpolation.

## Helper modules

Rails handles the inclusion of helper modules automatically. Unlike other modules which you have to explicitly include yourself.

What this means is any helper method is available in all Rails views.

## Arrays

You can split words in a string into an array, using the split method.

```
"pizza hamburger fries".split
# => ["pizza", "hamburger", "fries"]
```

By default split divids a string into an array on whitespace. `split` can also take an argument which will be used to split the string into an array.

```
"pizzashamburgersrice".split('s')
# => ["pizza", "hamburger", "rice"]
```

Arrays have methods such as `.empty?` which returns a boolean whether an array is empty or not. It also has `.include?(12)` which returns a boolean based on whether an array contains a value.

Arrays also has `.sort`, `.reverse`, and `.shuffle` these will change the output but does not change the array itself. To change the array itself, or mutate it, you will want to use the corresponding "bang" methods. For example `.reverse!`.

### push

You can add to an array using the `.push` method which is also equivalent to `<<`

```
a.push(6)
# or
a << 6
```

### join

The opposite of `split` is the `join` method, which allows you to the values of an array and join them together.

```
a = [12,3,55,"hello","world"]
a.join
# => "12355helloworld"
a.join(', ')
# => "12, 3, 55, hello, world"
# Joins with a comma and a space in between each value
```

## Hashes

Hash values can be virtually anything, even other hashes.

`:name` is a symbol. Inside of a hash, `:name` and `name:` are essentially the same.

```
{:name => "Michael"}
{name: "Michael"}
```

## Classes

Everything in Ruby is an object. Classes are used to organize methods and these classes are then instantiated to create objects.

To write your own class, the syntax follows:

```
class Word
  def palindrome?(string)
    string == string.reverse
  end
end
```

We can then use it as follows.

```
w = Word.new
w.palindrome?("hello")
# => false
w.palindrome?("level")
# => true
```

We can have the Word class inherit from String

```
class Word < String
  def palindrome?
    self == self.reverse
  end
end
```

This inheritance now allows for the Word class to ensure it has all of String's methods but also has the palindrome? method as well.

Classes can also be modified by using the same name as an existing class. Here we add the new method `palindrome?` to the existing String class.

```
class String
  def palindrome?
    self == self.reverse
  end
end
```
