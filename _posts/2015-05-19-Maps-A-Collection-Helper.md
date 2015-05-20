---
layout: post-light-feature
title: Maps, A Collection Helper
description: Think of Map as a magicians hat. You can put anything you want in it, and you can access items by a simple key.
categories: articles
tags: [ES6, blog, Javascript, Maps, JS Map, Array vs Map]
comments: true
date: 2015-05-19
reference: http://www.2ality.com/2015/01/es6-maps-sets.html
fnpreview: "let map = new Map()"
---

Take a look at the dynamics of Map:

{% highlight js %}
// Creates a Map
let m = new Map()

// Add things into the Map, anything you want
m.add("hello", "hey you")

// Strange thing, need to find a good use case for this
m.add({}, "Object as a key") 

// Could be a nice default value
m.add(NaN, "default")
{% endhighlight %}

Another great thing to note, chaining methods:

{% highlight js %}
let d = new Map()

d.add("hello", "hey you")
 .delete("hello")

console.log(d.has("hello")) // false
{% endhighlight %}


Map methods are very similar to Set, only the structure of storing/retrieving items is different.

### Here are the methods: 

* set - method to add data to a Map with its key name and value
* get - method to retrieve data from a Map by its key name
* clear - removes all data within the Map
* delete - removes data by key
* has - method to access data inside a Map from its key name, returns boolean
* keys - returns all keys available inside the Map
* size - the amount of the items within the Map, similar to *Array.length*
* values - returns all values available inside the Map
* entries - returns an Array of key/value pairs of any items defined in the Map
* forEach - iteration similar to *Array.forEach*

### Findings:

* Since Map handles collection data, Map can be used extensively for functions that need more flexibility in data stored.
* Map could be used for a config contract, the interface makes this a prime candidate for a better data object.

### References:

* [2ality](http://www.2ality.com/2015/01/es6-maps-sets.html)