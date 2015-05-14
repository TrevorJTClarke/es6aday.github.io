---
layout: post-light-feature
title: Promises, Part 1
description: Scraping the surface of promises
categories: articles
date: 2015-05-14
reference: http://www.2ality.com/2014/10/es6-promises-api.html, https://github.com/soareschen/es6-promise-debugging
---
A quick look into the Promise setup. This simple example shows how there are many ways to utilize promises.

{% highlight js %}
// declare a function and assign a promise, dont let our data be empty
function asyncFn (name = "George") {
    
    // define something to do
    var resolve = (f => {
        // we know this is Abe now
        console.log(arguments[0])
        return name += " Lincoln"
    })

    // handle some rejection
    var reject = (() => {
        console.log("rejected")
    })
    
    // return a promise
    return new Promise((res, err) => {
        // a dirty way to call the resolve
        res(resolve())
    })
}


asyncFn("Abe").then(res => {
      // This should say Abe Lincoln
      console.log("Resolved:", res)
  }, err => {
      if(err){
          throw new Error(err)
      }
  })
  .catch(err => {
      // an error happened somewhere inside the promise chain
      console.log("ERROR Caught:", err);
  })
{% endhighlight %}

### Findings:

  - 