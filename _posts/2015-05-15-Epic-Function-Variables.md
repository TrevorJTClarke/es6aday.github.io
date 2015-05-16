---
layout: post-light-feature
title: "Epic Function Variables: Spread"
description: This probably just made things more awesome. I'm tired of implied "arguments" and the rigidity of variables passed into functions.
categories: articles
date: 2015-05-15
reference: https://babeljs.io/docs/learn-es6/#default-rest-spread
fnpreview: "fn(...[2,3,4])"
---

Functions with spread variables, there are so many use cases where this could be helpful.

{% highlight js %}
// setup the function as if you have 3 set variables
function getSpread(x, y, z) {
    // just add
    return x + y + z;
}
// Pass each elem of array as argument
var s = getSpread(...[2,3,4])
// returns 9
console.log("Spread", s)
{% endhighlight %}


### Findings:

* I have used rigid variables for many purposes, but the flexibility given here means I can pass in an Array rather than an Object or single variable. Only problem here is having to account for a missing/undefined item.

Example: 

{% highlight js %}
// Before:
var options = {
  name: "Example Options Object",
  left: true,
  totalRecords: 43
};

// Now:             x                     y   z
var options = ["Example Options Object",true,43]
// Inside the function, each item becomes its own variable 
// Instead of accessing from an array by: arrayData[0]
//    -> access by y = true
{% endhighlight %}


### References:

* [Babeljs](https://babeljs.io/docs/learn-es6/#default-rest-spread)