# JavaScript-[Intro-JS](-Intro-to-JavaScript) :scream_cat: 
_Source: Intro to JavaScript - Udacity Front End Web Development Nanodegree_

### Table Of Contents:
- __a. What is JavaScript?__
- __b. The JavaScript Console__
- __c. Developer Tools on Different Browsers__
- __d- Console.log__

### a. What is JavaScript?
- __HTML__ and __CSS__ are `markup languages`, that _describe and define elements within a document_. 
- __JavaScript__ is a `programming language`, used to _communicate instructions to a machine_ to:
    1) _control the behavior of a machine_ 
    2) _express algorithms_.

### b. The JavaScript Console
The __JavaScript Console__ is a development tools to `iterate`, `debug` and `profile` JavaScript code directly into the web browser.
```
"Diana"
alert("Hello "Diana"! How are you?!");
```
This creates a _JavaScript alert box_ in the web browser, on the current web page.

### c. Developer Tools on Different Browsers
Every modern web browser includes its own set of developer tools:

#### 1 [Google Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools/)
- The Chrome DevTools are a set of web authoring and debugging tools built into Google Chrome. 
- Use the DevTools to `iterate`, `debug` and `profile` a site. 
- __Open Chrome DevTools:__
  1) `right-click` on any page element, select `Inspect`. 
  2) open the `Chrome settings menu` in the top-right corner of your browser window and select `More Tools > Developer Tools`. 
  3) Use shortcuts: `Command + Option + i` (Mac) OR `Ctrl + Shift + i`/ `F12` (Windows/Linux).

#### 2 [Mozilla Firefox](https://developer.mozilla.org/en-US/docs/Tools)
- Firefox Developer Tools allow to examine, edit, and debug HTML, CSS, and JavaScript on the desktop and on mobile. 
- Download a version of Firefox called `Firefox Developer Edition` tailored for developers, featuring the latest Firefox features and experimental developer tools. 
- __Open Firefox Developer Tools:__
  1) `right-click` on any page element, select `Inspect`. 
  2) open the `Firefox settings menu` in the top-right corner of your browser window and select `Developer`. 
  3) Use shortcuts: `Command + Option + i` (Mac) OR `Ctrl + Shift + i`/ `F12` (Windows/Linux).

#### 3 Internet Explorer
- The features vary between versions, but starting at Internet Explorer 8 remain pretty consistent.
- [Internet Explorer 8](https://msdn.microsoft.com/en-us/library/dd565628.aspx)
- [Internet Explorer 9](https://docs.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/samples/gg589512(v=vs.85))
- [Internet Explorer 10](https://docs.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673549(v=vs.85))
- [Internet Explorer 11](https://docs.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/dev-guides/bg182636(v=vs.85))
- __Open Internet Explorer Developer Tools:__`F12`

#### 4 [Microsoft Edge]( https://docs.microsoft.com/en-gb/microsoft-edge/devtools-guide)
- __Microsoft Edge__ introduces improvements to the F12 developer tools in Internet Explorer. 
- The new tools are built in `TypeScript`, and are always running, so no reloads are required. 
- F12 developer tools documentation available on [GitHub](https://github.com/MicrosoftDocs/edge-developer). 
- __Open Microsoft Edge Developer Tools:__`F12`

#### 5 [Safari Web Inspector](https://developer.apple.com/safari/tools/)
For any Mac users, Safari includes Web Inspector, a powerful tool that makes it easy to modify, debug, and optimize a website for peak performance and compatibility on both platforms. 
- __Safari's Web Development Tools:__
  1) Enable the Develop menu in `Safari’s Advanced preferences`. Then  `right-click` on any page element, select `Inspect Element`. 
  2) Use shortcuts: `Command + Option + i` (Mac).

#### 6 [Opera Dragonfly](https://www.opera.com/dragonfly/)
- Fast, lean and powerful, Opera comes pre-packed with a fully-featured suite of developer tools. 
- Opera Dragonfly is designed to make your job easier. 
- __Open Opera Dragonfly:__
  1) `right-click` on any page element, select `Inspect Element`. 
  2) Use shortcuts: `Command + Option + i` (Mac) OR `Ctrl + Shift + i`/ `F12` (Windows/Linux).

### d. Console.log
`console.log` is used to display content to the JavaScript console. 
__Perform the log action on the debugging console:__
- Run the following code in the console:
```
console.log("hiya friend!");
```
- __Prints:__ "hiya friend!"
- The __message logged__ is "hiya friend!". 
- hiya friend! is a `string` (=a _sequence of characters_).

- Write a block of JavaScript code that __`loops`__ through the numbers 0 through 9 and prints them out to the console:
```
for (var i = 0; i < 10; i++) {
  console.log(i);
}
```
- __Prints:__ 
"0
1
2
3
4
5
6
7
8
9"
- This means: any code written inside the __curly brackets__ `{...}` will be repeated 10 times. 
-  In this case, `console.log` is printing out the value of `i` each time the loop runs.

__How to use the console as a sandbox to test a new line of JavaScript in the browser?__
- Open [this site](https://daringfireball.net/projects/markdown/) in Dev Tools.
- Paste the following code: `document.getElementsByTagName("h1")[0].style.color = "#ff0000";`
- __What happened when you ran that line of code in the JavaScript console?__
- The heading changed to RED.
- Styling elements on the page is great, can also be don by modifying the CSS. 

__What makes JavaScript so special in this case?__ 
- Refresh the page, then paste this line of code in the JavaScript console.
`document.body.addEventListener('click', function () {
     var myParent = document.getElementById("Banner"); 
     var myImage = document.createElement("img");
     myImage.src = 'https://thecatapi.com/api/images/get?format=src&type=gif';
     myParent.appendChild(myImage);
     myImage.style.marginLeft = "160px";
});`
- When you click, an image (cat gif)is added to the webpage 🐱! An image is added to the page.

#### Resources 
- [Chrome Dev Tools Keyboard Shortcuts](https://developers.google.com/web/tools/chrome-devtools/shortcuts)
- [Google Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools/)
- [Mozilla Firefox](https://developer.mozilla.org/en-US/docs/Tools)
- [Internet Explorer 8](https://msdn.microsoft.com/en-us/library/dd565628.aspx)
- [Internet Explorer 9](https://docs.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/samples/gg589512(v=vs.85))
- [Internet Explorer 10](https://docs.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673549(v=vs.85))
- [Internet Explorer 11](https://docs.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/dev-guides/bg182636(v=vs.85))
- [Microsoft Edge]( https://docs.microsoft.com/en-gb/microsoft-edge/devtools-guide)
- [Safari Web Inspector](https://developer.apple.com/safari/tools/)
- [Opera Dragonfly](https://www.opera.com/dragonfly/)
