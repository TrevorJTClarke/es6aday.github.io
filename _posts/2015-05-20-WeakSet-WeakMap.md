---
layout: post-light-feature
title: WeakSet, WeakMap
description: Associate data with objects without having to worry about memory leaks.
categories: articles
tags: [ES6, blog, Javascript, Maps, JS Map, Array vs Map]
comments: true
date: 2015-05-19
reference: http://www.2ality.com/2015/01/es6-maps-sets.html
fnpreview: "let wm = new WeakMap()"
---

With WeakMap, the API is similar except you cannot iterate on data inside, and all data must be arbitrary. WeakMap is best suited for private methods where you know both the WeakMap and Keys.

{% highlight js %}
// Creates a WeakMap
let m = new WeakMap()


{% endhighlight %}


### For WeakMap, here are the available methods: 

* set - method to add data to a Map with its key name and value
* get - method to retrieve data from a Map by its key name
* delete - removes data by key
* has - method to access data inside a Map from its key name, returns boolean

##### *NOTE:* If WeakMap had the method **clear** for example, it would be a security risk. See [TC39 Resolution](https://github.com/rwaldron/tc39-notes/blob/master/es6/2014-11/nov-19.md#412-should-weakmapweakset-have-a-clear-method-markm)

### Findings:

* 

### References:

* [2ality](http://www.2ality.com/2015/01/es6-maps-sets.html)