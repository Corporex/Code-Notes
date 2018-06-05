# Callback, Promises & Async

__Callback__ = `the default JS technique for Asynchronous work`: 
- Passes a `function`() into another function 
- Calls the `call back`() function at some time later, when some conditions have been met.
EXAMPLE:
```
function loadImage(scr, parent, callback) {
 var img = document.createElement('img');
 img.src = src;
 img.onload = callback;
 parent.appendChild(img);
};
```
__NOTE:__Althoug a `callback() function` works fine, it is not a solution for everything:

Remaining questions are:
1) __How to handle errors?__


# Promises 
__Course Stages:__
1. Wrapping.
2. Thening.
3. Catching.
4. Chaining.

__States:__
1. Fulfilled (Resolved). => The action related to the promise succeeded.
2. Rejected. => The action related to the promise failed.
3. Pending. => Promise has not yet fulfilled or rejected.
4. Settled. => Promise has either fulfilled or rejected.

 # Async/Await
 ![Async](https://github.com/dianavile/Code-Notes/blob/master/img/Async.png)
 
# Resources:
- [Getting to know asynchronous JavaScript: Callbacks, Promises and Async/Await](https://medium.com/codebuddies/getting-to-know-asynchronous-javascript-callbacks-promises-and-async-await-17e0673281ee)
- [JavaScript Promises](https://davidwalsh.name/promises)
- [Google Developers- JavaScript Promises: an Introduction](https://developers.google.com/web/fundamentals/primers/promises)
- [JavaScript Promises for Dummies](https://scotch.io/tutorials/javascript-promises-for-dummies)
- [Asynchronous vs synchronous execution, what does it really mean?](https://stackoverflow.com/questions/748175/asynchronous-vs-synchronous-execution-what-does-it-really-mean)
