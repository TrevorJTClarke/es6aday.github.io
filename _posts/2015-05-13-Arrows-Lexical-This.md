---
layout: post-light-feature
title: Arrows and Lexical "this"
description: A study into accessing "this" within the new lexical structure, and arrow functions.
categories: articles
tags: [ES6, blog, Javascript, Arrows, Lexical]
comments: true
date: 2015-05-13
reference: https://babeljs.io/docs/learn-es6/#arrows
fnpreview: "((v, i) => { return v + i })"
---
In trying to understand use cases of "this", I setup the following scenarios:

{% highlight js %}
// Test array
var evens = [2,4,6,8,10]

// Example Expression
var nums = evens.map((v, i) => {
  // here, "this" becomes undefined. There is no lexical parent to tie to.
  console.log(this)
  return v + i
})
  
var parent = {
  name: "parent",
  // new object literal syntax!! :)
  get(){ 
    // here, "this" has a lexical parent to tie to. We can access "this".
    console.log("get()",this)
  },
  getNums( numbers ){
    return numbers.map((v, i) => {
      // here, "this" has the same lexical parent as its containing function.
      console.log("getNums parent",this)
      return v + i
    })
  }
}
// The final result
console.log(nums)
console.log(parent.get())
console.log(parent.getNums( nums ))
{% endhighlight %}

### Findings:

  - "this" is only accessible within a non-arrow function
  - Arrow functions are excellent at being consice, but can get confusing if building larger use cases.
  - Removing "this" from an arrow function can potentially help make scope context less error prone.