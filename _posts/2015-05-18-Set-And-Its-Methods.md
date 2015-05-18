---
layout: post-light-feature
title: Set, and Its Methods
description: Very similar to the native Array, Set has significantly more support for helpful methods.
categories: articles
tags: [ES6, blog, Javascript, Sets, JS Set, Array vs Set]
comments: true
date: 2015-05-18
reference: https://babeljs.io/docs/learn-es6/#default-rest-spread
fnpreview: "var s = new Set()"
---

There are quite a few methods available, making it easy to access/store data in a Set, with the flexibility of handling multiple types of data.

{% highlight js %}
// Creates a Set
var s = new Set()

// Add things into the Set, anything you want
s.add("hello") // Strings
 .add({"data": "hiii data"}) // Objects
 .add(["First", "Second"]) // Arrays

// The "size" is similar to Array.length
s.size === 3

// Easily access/change the data from a key
s.has("hello") === true
s.delete("hello")
s.has("hello") === false

// get all the keys/values of the Set
console.log(s.keys())
console.log(s.values())
{% endhighlight %}



### Here are the methods: 

* add - method to add data to a Set with its key name, similar to *Array.push*
* clear - removes all data within the Set
* delete - removes data by key
* has - method to access data inside a Set from its key name
* keys - returns all keys available inside the Set
* size - the amount of the items within the Set, similar to *Array.length*
* values - returns all values available inside the Set
* entries - returns an Array of key/value pairs of any items defined in the Set
* forEach - iteration similar to *Array.forEach*

### Findings:

* Set has  a lot of power with the methods provided
* It functions like a well defined Array with extra alias methods
* Could be useful for handling user data, or any data contract

### References:

* [Babeljs](https://babeljs.io/docs/learn-es6/#default-rest-spread)