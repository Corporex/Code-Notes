# Accessibility
_Source: Accesibility - Udacity Front End Web Development Nanodegree_

### Table Of Contents:
* [A11y Overview](#1-a11y-overview)
* [FOCUS](#2-focus)
* [Semantics Basics](#3-semantics-basics)
* [Navigating Content](#4-navigating-content)
* [ARIA](#5-aria)
* [Style](#6-style)

## 1. A11y Overview
__GOALS:__
- a. __Accessibility__: What is accessibility?
- b. __User experience:__ Explore diversity of user experience with web and apps.
- c. __Screen readers:__ How to use screen readers practically?
- d. __Inclusive webexperiences:__ How to build webexperiences for all users?

### a. __DEFINITION__: What is accessibility?
- `Good accessibility`("a11y"):`_to ensure all users can access the content in web and apps_`.
- Site _**content**_ needs to be `available` to everyone.
- Site _**functionality**_ needs to be `operable` to everyone.
__`Acessibility`__= to make sure "content" and "websites" created are `usable` to people with _various imparements or abilities._
- __Note:__ 
- `"a11y"` is a shorten word for `"accessibility"`(=there's 11 letters between the "A" and "Y" in the word "Accessibility"). 
- `"i18n"`is a shorten word for `"internationalization"`.
- `" l10n"`is a shorten word for `"localization"`.

### b. __USER EXPERIENCE:__ _Explore diversity of user experience with web and apps_
- Consider accessibility (`"a11y"`) from the start of your process, as it `affects all users`:

1) __Users with `_disabilities_`:__ (issues due to `human disability`.) 
- a. `Vision impairment`
  - __vision disability:__ (_blind or have significant difficulty seeing even with glasses_)
  - __refractive error:__ (_a visual impairment which may be corrected with glasses if mild enough_)
  - __color vision deficiency:__(_difficulty to distinguish colors_)
- b. `Hearing impairment`  
  - __hearing disability:__(_deaf or have significant difficulty hearing even with hearing devices_)
- c. `Cognitive impairment`
  - __cognitive disability:__ (_difficulty remembering, concentrating, or making decisions_)
- d. `Motor impairment`
  - __physical disability:__ (_part of the body does not work optimal_)
- __Note:__ These impairments can be `Temporary`, `Permanent`, or `Situational`.)  

2) __Users `_without disabilities_`:__ (issues due to `bad design`) 
- __unresponsive design__ 
- __lack of__ `color contrast` 
- __lack of__ `keyboard navigation`
- __lack of__ `visual or sound alternative`
- __lack of__ `zoom-in option`
- __lack of__ `minimal design`(_to minimize distraction_)

#### Sources:
  - [Disability Compendium](https://disabilitycompendium.org/)
  - ["The Perception of Color"](https://www.ncbi.nlm.nih.gov/books/NBK11538/)
  - ["Prevalence of Refractive Error in the United States, 1999-2004"](https://jamanetwork.com/journals/jamaophthalmology/fullarticle/420707)

### c. SCREEN READERS/VIEWERS 
A __Screen viewer__ = `software that allows blind people to hear the information displayed on a screen, via text-to-speach-syntiziser.`

- __How to use a Screenreader?__
- Enable `ChromeVox Lite` via the "Enable ChromeVox Lite" button or press `TAB` once.
- The controls for ChromeVox Lite will appear once it is enabled:
- `"Voice"` drop-down: to choose alternate voices
- `"Speech rate"` drop-down: to make speech faster or slower
- `"Navigate"`buttons: to move ChromeVox's focus to non-focusable items on the page (e.g. Headers)
- `"Volume control"`: to fine-tune ChromeVox's volume. 

#### Sources:
  - **[Screen Reader example](http://udacity.github.io/ud891/lesson1-overview/06-experiencing-screen-reader/)**
  - [Chromevox extension](https://chrome.google.com/webstore/detail/chromevox/kgejglhpjiefppelpmljglcjbhoiplfn?hl=en)
  - [Chromevox extension shortcuts](http://www.chromevox.com/keyboard_shortcuts.html)

### d. Web Content Accessibility Guidelines: 
_Web Content Accessibility Guidelines_ make your website and app 
- __"POUR"__ (4 core principles):
- `Percievable`: to make sure ALL users can "percieve" content. (_Is the content "visual, audio, text, keyboard, touch!- ready?_)
- `Operable`: to make sure users can "work" with the content. (_Can users use your components and navigate the content?_) 
- `Understandable`: to make sure users "understand" the content & the interface. (_Can users understand your content?_) 
- `Robust`: to make sure ALL users (_Is the content "robust" enought be be consumed by a wide variety of ages?_)
- __Note:__ Although the below guidelines are a great resource, what actually matters is `"the users experience"`.

#### Sources:
  - [WCAG](https://www.w3.org/TR/WCAG20/) (_Web Content Accessibility Guidelines 2.0_)
  - [Web Aim Checklist WCAG 2.0](https://webaim.org/standards/wcag/checklist): checklist to _`ensure web meet WCAG guidelines`_.

## 2. FOCUS
__GOALS:__
- a. __FOCUS (MANAGEMENT):__ What is focus (management)? 
- b. __DOM ORDER__  
- c. __TABINDEX ATTRIBUTE__ 
- d. __SKIP LINKS__ 
- e. __MANAGE FOCUS__ 
- f. __KEYBOARD DESIGN PATTERNS__ 
- g. __OFF-SCREEN CONTENT__
- h. __MODALS & KEYBOARD TRAPS__

### a. __DEFINITION__:  focus (management)
__FOCUS__= `the location on a page that receives input from the keyboard`. It shows _where keyboard events go in a page_.
- An __HTML user interface(UI)__ consists of _multiple interactive widgets_ (__input__, __buttons__ & __select__ elements), 
- Such as:`form controls`, `scrollable regions`, `links`, `dialog boxes`, `browser tabs`, that form a `hierarchy` of `automatic tab order + built-in keyboard event handling`. They are __implicitely focussable__.
- Yet, __NOT all elements are focussable__. Examples are `header`, `paragraphs`and `images`. 

__FOCUS MANAGEMENT__= Move focus around the page using your [keyboard](https://www.w3.org/TR/html5/editing.html#focus-management) to interact with the interface.
- __TAB ORDER__:  _key input_ is channeled from the system, through a hierarchy of interactive widgets, to the "active(= focused) widget:
- ```TAB```: move focus forward
- ```SHIFT  TAB```: move focus backwards
- ```Arrow keys```: to navigate inside a component
```
Don't add focus to any content a user can Not interact with.
```
#### Sources:
- [Focus Management](https://www.w3.org/TR/html5/editing.html#focus-management)
- Exception: [add focus to non-interactionable content](https://www.youtube.com/watch?time_continue=155&v=ifW_oy9hajU)

### b. DOM ORDER
The DOM order matters for FOCUS MANAGEMENT: `element.tabIndex;`
```
Tab order = same as DOM order, even if  `visual` order is changed (with CSS).
Changing the  `visual` order can cause confusion among `screen readers` and `keyboard users`, who depend on keyboard navigation. 
```
- Work with native elements is good practice for __FOCUS behaviour__, because they are automatically be inserted into the __TAB ORDER__, based on their __DOM POSITION__.
```
<button> I should </button>
<button> Be Focussed </button>
<button> Last! </button>
```
- If Visual order is changed (with CSS), it can cause confusion:
```
<button style= "float: right;"> 
I should </button>
<button> Be Focussed </button>
<button> Last! </button>
```
- To prevent confusion, the __Reading__ and __navigation order__ (code order) SHOULD BE _logical_ and _intuïtive_.

#### Sources: 
- [WebAIM checklist items](http://webaim.org/standards/wcag/checklist#sc1.3.2)

### c. TABINDEX ATTRIBUTE
- Control __FOCUS BEHAVIOUR__ with __TABINDEX ATTRIBUTE__. 
- To get tabindex value of an element: `element.tabIndex;`
- __NOTE:__ `ONLY NEEDED` for `Interactional elements` (__input__, __buttons__ & __select__ elements)
- __NOT__ for `non-interactional elements` (__HTML-tags__, such as: _headers, paragraphs or images_)
 
- These elements should have __FOCUS__:
  - `Header links`
  - `Call to Action button`
  - `Search Input`
  - `Form Elements`
  - `Footer Links`
- The elements should __NOT have FOCUS__:
  - `Header`
  - `Block of text (paragraph)`
  - `Image`
  
##### 1) __tabindex = "-1"__
_ [.] __NOT__ in tab order.
- [.] focus programmatically by `focus()`
- [.] Used for __Off screen content, that appear in response to a user event()__ (ex. modals).
```
HTML: <dialog id="modal" tabindex="-1"></dialog>
JS: document.querySelector(´#modal´).focus()
```
##### 2) __tabindex = "0"__
- [.] to insert __Unfocusable element__ in tab order.
- [.] focus programmatically by `focus()`
- [.] So, `keyboard events` get directed to it.
```
HTML: <div id="dropdown" tabindex="0">Settings</div>
JS: document.querySelector(´#modal´).focus()
```
##### 3) __tabindex > 0__ 
- [.] Jump to the (__IN__) front of the tab order.
- [.] If multiple elements, `lowest value`= first (in tab order).
- [.] This practice is discouraged and seen as an __anti-pattern!__

- __NOTE__: never remove the `focus indicator` from an _interactive element_ unless you're going to replace it. 
- Otherwise a keyboard user might not know which element is focused!

#### Sources: 
- [tabindex on MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/tabindex)
- [focus navigation and tabindex attribute](https://www.w3.org/TR/html5/editing.html#sequential-focus-navigation-and-the-tabindex-attribute)

### d. SKIP LINKS
- Allow `screen reader, keyboard, and switch devices users` to __navigate__ towards main pagecontent.
- It bypasses all the following elements before the main content: `navigation bar`, `sublists`, `sitebars`, `hamburger menus`.
- Skip links makes all links __hidden until focus().__
```
<!--html code-->
<a href="#main-content" class="skip-link">Skip to main content</a>
<nav>
.
.
.
</nav>
<main id="main-content" tabindex="-1">
.
.
.
</main>
```
```
/*CSS code*/
.skip-link {
  position: absolute;
  top: -40px;
  left: 0;
  background: red;
  color: white;
  padding: 8px;
  z-index: 100;
  }
.skip-link:focus {
  top: 0;
  }
  ```
#### Sources: 
- [skip links](https://webaim.org/techniques/skipnav/)
- [Focus Start point](https://developers.google.com/web/updates/2016/03/focus-start-point?hl=en)
- **[Alternate way to skip to main content.](https://webaim.org/techniques/skipnav/#headings)**

### e. MANAGE FOCUS
- To manage `Focus in Complex Components`, use the [WAI-Aria guidelines](https://www.w3.org/TR/wai-aria-practices-1.1/).
-  The __ARIA Authoring Practices__ ("_ARIA Design Patterns doc_") provides guidance in selecting which `keyboard interaction` is appropriate for complex component ("actions", such as `drop down menu`, `tree view component`. 
 
### f. KEYBOARD DESIGN PATTERNS 
- Use `keyboard design patterns` to implement __focus inside of a component__.
- EXAMPLE: __Radio pattern__`Implement Keyboard Event Listeners`
- Use __ROVING FOCUS__( `"roving tabindex"`) to make changes in: `radiogroup.js`file.
 - __first radio button__: 
 1. tabindex="0" 
 2. checked 
 3. focus()
```
<li tabindex="0" checked> //set tab index to 0 on the currently active item
<li tabindex="-1"> //set tab index to -1 for all children
<li tabindex="-1">
<li tabindex="-1">
<li tabindex="-1">
```
- The component uses a `keyboard event listener` to know which keyboard the user pressed.
- to know on which component to set next tabindex to 0
- when moving to the next element => first element: 
1. tabindex="-1" 
2. remove checked 
3. unfocus :: 
```
<li tabindex="-1"> //change tabindex to -1, remove checked
<li tabindex="0"> checked //add focus(), later remove focus() and add checked
<li tabindex="-1">
<li tabindex="-1">
<li tabindex="-1">
```
Next element: 1. tabindex="0" / 2. checked / 3. focus()
  - If  __last__ element `tab` move to __first__ element.
  - If  __first__ element `shift` + `tab` move to __last__ element.

#### Sources: 
- [ARIA Authoring Best Practices 1.0 (Radio Button)](https://www.w3.org/TR/wai-aria-practices/#radiobutton)
- [ARIA Authoring Best Practices 1.1 (Radio Group)](https://www.w3.org/TR/wai-aria-practices-1.1/#radiobutton)
- [Example](https://www.w3.org/TR/wai-aria-practices-1.1/examples/radio/radio-1/radio-1.html)
- [ARIA- Design Patterns and Widgets](https://www.w3.org/TR/wai-aria-practices/#aria_ex)
- [Video](https://www.youtube.com/watch?v=uCIC2LNt0bk)

### g. OFF-SCREEN CONTENT
- A drawer panel can lead __focus__ to `visually disappear`. 
- Overcome it by setting `display: none;` or `visibility: hidden;`

####__How to check if `OFF-SCREEN CONTENT` is `ACCESSIBLE`?__
1) __Track focus:__ to find `missing focus`, type into console: `document.activeElement;`
    - this gives a reference to the current focussed item
2) Use the __Chrome Accessibility Developer Tools Extension__ to quickly find __accessibility issues__ in your page:
    - to add an `Accessibility Properties panel` to __Elements__ inspector
    - to add an `Accessibility option` to __audits__ panel. 
#### Sources: 
- [document.activeElement](https://developer.mozilla.org/en-US/docs/Web/API/DocumentOrShadowRoot/activeElement)
- [Chrome Accessibility Developer Tools Extension](https://chrome.google.com/webstore/detail/accessibility-developer-t/fpkknkljclfencbdbgkenhalefipecmb?hl=en)

### h. KEYBOARD TRAP & MODAL
-  __KEYBOARD TRAP:__ keyboard focus is `locked or trapped at one particular page element`. 
- The user __CAN NOT__ `navigate` to and from all navigable page elements, using only a keyboard.
- Prevent a `permanent keyboard trap`.

__EXCEPTION:__ use a `temporary keyboard trap` for a __MODAL__
- Use __WebAim__ in `Modals` to _trap keyboard focus inside the modal_ until modal is closed.
- It => return focus to `last focused element` before modal open.
__HTML__:
```
<button class="modal toggle"> Open Modal </button>

<div class="modal">
  <h1> Join our newsletter </h1>
  <p> short description about the newsletter & why to join? 
  </p>
  <div class="field">
  <label for="fullname"> Full Name </label>
  <input id="fullname" type= "text">
</div>
 <div class="field">
  <label for="email"> E-mail address </label>
  <input id="email" type= "text">
</div>
<button id="signup"> Sign me up!</button>
</div>

<div class="modal overlay"></div>
```
__JAVASCRIPT__:
```
//hold previosly focussed element
let focusedElementBeforeModal;

//find the modal and its overlay
const modal document.querySelector(´modal´);
const modalOverlay document.querySelector(´modalOverlay´);

//add EventListener "click" on ModalToggle to openModal
let modalToggle document.querySelector(´modalToggle´);
modalToggle.addEventListener(´click´, openModal);

//create function openModal
function openModal(){
//save current focus
focusedElementBeforeModal= document.activeElement;

//Listen for and trap the keyword
modal.addEventListener(´keydown´, trapTabKey);

//Listen to indicators to close the modal
modalOverlay.addEventListener(´click´, closeModal);
//Sign-up button
let signupBtn.addEventListener(´click´, closeModal);

//Find all focusable children
const focusableElementString = ´a[href], area[href],
input:not([disabled]), select:not([disabled]),
textarea:not([disabled]), button:not([disabled]), iframe, object,
embed, [tabindex=´0´]), [contenteditable]´;

let focusableElements = 
modal.querySelectorAll(´focusableElementString´);

//Convert Nodelist to Array
focusableElements= Array.prototype.slice.call(focusableElements);

//Figure out first and last element in group of focusableElements
let firstTabStop = focusableElements[0];
let secondTabStop = focusableElements[focusableElements.length -1];

//Show the modal and overlay
modal.style.display = ´block´;
modalOverlay.style.display = ´block´;

//Focus firstTabStop
firstTabStop.focus();

function TapKeyPress()
//Check for TapKeyPress
if (e.keyCode === 9) {

//shift + TAB
if (e.shiftKey) {
if document.activeElement=== firstTabStop) {
e.preventDefault();
lastTabStop.focus();
}
//TAB
} else {
if document.activeElement=== lastTabStop) {
e.preventDefault();
firstTabStop.focus();
    }
  }
}

//Escape
if (e.keyCode ===27) {
closeModal();
    }
  }
}

function closeModal(){
//Hide the Modal and Overlay
modal.style.display = ´none´;
modalOverlay.style.display = ´none´;
  
//Set focus back to element before modalOpen
focusedElementBeforeModal.focus();
}
```
#### Sources: 
- [WebAIM checklist items](http://webaim.org/standards/wcag/checklist#sc2.1.2)
- [dialog](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dialog)
- [Example](https://github.com/udacity/ud891/tree/gh-pages/lesson2-focus/07-modals-and-keyboard-traps)

##3. Semantics Basics

### a. Affordances
- Definition: the qualities or properties of an object that define its possible uses or make clear how it can or should be used.
- [WebAim](https://www.w3.org/TR/UNDERSTANDING-WCAG20/ensure-compat-rsv.html)
- Screen reader can provide info for elements' **Name(label) Role State Value.**
- Browser takes DOM tree (natively semantic elements or othered with ARIA)  ==modify it to==> Accessibility tree( containing all information for screen reader Name Role State Value).

### b. Labeling, Naming, and Alternative text
- [WebAim](https://webaim.org/standards/wcag/checklist#g1.1)
- Element could have a visual label (name) like for radio button or text alternative like in case of images.
- There are 2 ways of labeling form inputs.
```
<label>
  <input type="radio">
  Check me
</label>
```
```
<input type="radio" id="radio-button">
<label for="radio-button">Check me</label>
```
 - Using these labeling allow user to toggle the input element by also clicking the label.
 - alt text: 1. An alternative to the image if not loaded.
             2. describe what the image about for screen reader.
             3. For logos you can assign the company name for alt attribute.
             4. For search icon you can leave alt with no value. This will skip it from accessibility tree.
             5. Any image that is meant for decoration should have an empty alt.
             
             
## 4. Navigating Content
- Screen Reader can make you navigate through headings, links, form controls, and landmarks.
- It is important to use meaningful headings and links names.
- Also use a good heading structure from h1 to h6 (for long complex content).
- descriptive link text example: 
instead of using "learn more" links text use :learn more about bla bla".
- [link Anti-patterns video](https://youtu.be/SiblO4dfYBg)
- Landmarks: you can navigate by landmarks
`<header>`
`<nav>`
`<main>`
`<section>`
`<article>`
`<aside>`
`<footer>`

## 5. ARIA
- **WAI-ARIA**: Web Accessibility Initiative - Accessible Rich Internet Application.
- ARIA attributes need to have explicit values (can't be empty values).

- What ARIA can do and what can not do:
  - Can:
  
  :white_check_mark: modify Accessibility tree.
  
  - Can Not:
  
  :x: modify element behaviour.
  
  :x: modify element appearance.
  
  :x: add focus.
  
  :x: add event handling.
  
- ARIA give a semantic meaning to non semantic elements.
- ARIA can also give a new semantic meaning to a native semantic element.
  - Example:
  ```
  <button role="switch" aria-checked="true" class="toggle">
    Enable
  </button>
  ```
- ARIA can express UI patterns which doesn't exist in HTML.
  - Example: `tree widget`

- ARIA can add labels which is only accessible to assestive technology.

- ARIA can provide semantic Relationship.

- ARIA can provide live updates (aria-live).

- the [video](https://youtu.be/7vz1aakYHtw?t=50s) explains that.

### a. Role

- Definition: Short hand for a particular UI pattern.

- make sure that the role attribute is in the same element as tabindex attribute.

```
<div tabindex="0" role="checkbox" aria-checked="true" class="checkbox" checked>check me</div>
```

### b. ARIA labelling

- **aria-label** _attribute_
  - Can be used for element that has only a visual appearance.
  - override any other labelling such as `<label>`, or text content (like that for a button) except **aria-labelledby** _attribute_.
  - have the label clicking behaviour like `<label>` 
  
- **aria-labelledby** _attribute_
  - Overcome all other labelling methods.
  - refers to another element (which label it) by using a value corresponds to the id of the labelling element.
  - can take more than one element id (multiple labels) .
  - can refer to elements that are hidden for assestive technologies ( hidden for example).
  - Don't have the label clicking behaviour like `<label>` and `aria-label`.
  
### c. Landmarks and ARIA roles
- Landmarks may not have support in browsers' old versions. So we need to use role attribute with them.
  -Examples: 
  ```
  <header role="banner">
  <nav role="navigation">
  <main role="main">
  <aside role="complementary">
  <footer role="contentinfo">
  <dialog role="dialog">
  ```
  
### d. ARIA realtionships  
- **ARIA relationship attributes**
  - They take a reference to one or more elements on the page to make a link between them.
  - The difference is: 1. _What link means_.
                       2. _How represented to users_.
          
- Attributes: 
  - `aria-labelledby`
  - `aria-describedby`
  - `aria-owns`
  - `aria-activedescendant`
  - `aria-posinset`
  - `aria-setsize`
    
- [Video](https://youtu.be/e1ZmfmnB6v8?t=40s) explains it.
- [Collection of relationship attr](https://www.w3.org/TR/wai-aria-1.1/#attrs_relationships)


### e. Visible and Hidden content
- For the seek of fine tuning the experience of users using assistive tech.
- To ensure that certain parts of the DOM is either: 
  - hidden to assistive tech.
  Or
  - Only visible to assistive tech.
- Hidden:

  1. 
  ```
  <button style="visibility: hidden;">
  <div style="display: none;">
  <span hidden>
  ```
  2. `aria-hidden="true"`
  
- Only visible to assistive tech:
  1. element positioned absolute far off the screen. `position: absolute; left: -1000;`
  2. `aria-label`
  3. `aria-labelledby` or `aria-describedby` reference a hidden element.


### f. ARIA live
- for in time alerts to user.
- `aria-live="polite"`  : important but not urgent alert.
- `aria-live="assertive"` : important and urgent alert.

### g. ARIA relevant
- These attributes work with `aria-live`:

  - `aria-atomic` : when true assistive tech will present the entire region as a whole.
  - `aria-relevant` :indicates which type of changes should be presented to the user.
    `aria-relevant="additions"` ==> means any element added to live region is presented.
    `aria-relevant="text"` ==> means that any text content added to any descendant element is presented.
    `aria-relevant="removals"` ==> means that removal of any text or element within the live region is presented.
    `aria-relevant="all"` ==> means that additions or removals of text is presented.
    `aria-relevant="additions text"` (default).
  -  `aria-busy`
 
## 6. Style
### a. Focus style
- [WebAim](https://webaim.org/standards/wcag/checklist#sc2.4.7).
- [video shows different styling for focus using :focus pseudo selector](https://youtu.be/ZooEnrj8aMc).
- [video shows different styling reaction between native and non native buttons](https://youtu.be/bfPGicTGBTI).
- Styling with ARIA ==> using ARIA attribute as an attribute selector. This made a good verification that I set the aria state properly.
- Responsive website:
  - [WebAim](https://webaim.org/standards/wcag/checklist#sc1.4.4).
  - meta viewport tag: `<meta name="viewport" content="width=device-width, initial-scale=1">`
  - In meta viewport tag: don't use `user-scalable=no` ==> prevent user from zooming the screen.
  - Use relative CSS units.
  - Use appropriate size touch targets.Minimum touch target size is 48 px.
  - If the touch target(like icons) is smaller, add padding to it.
  - To avoid overlapping make sure to leave margin around touch target with minimum 32px.
- Color Contrast:
  - [WebAim Minimum](https://webaim.org/standards/wcag/checklist#sc1.4.3).
  -It states that: Body text (less than 18.66px) ==> Contrast ratio minimum `4.5:1`
                   Large Text (more than 18.66px) or (24px) ==> Contrast ratio minimum `3:1`
                   
  - [WebAim Enhanced](https://webaim.org/standards/wcag/checklist#sc1.4.6).
   -It states that: Body text (less than 18.66px) ==> Contrast ratio minimum `7:1`
                    Large Text (more than 18.66px) or (24px) ==> Contrast ratio minimum `4.5:1`
 - You can use {Chrome Accessibility Extension}(https://chrome.google.com/webstore/detail/accessibility-developer-t/fpkknkljclfencbdbgkenhalefipecmb?hl=en) to make Accessibility Audit to check contrast ratios and see recommendations and try them live at Dev tools.
- 1 of 20 men and 1 in 200 women suffer from some sort of color blindness.
  - Don't convey info with color alone.
  - You can use color together with text, underline, audio, and aria-live.
  - [WebAim](https://webaim.org/standards/wcag/checklist#sc1.4.1).
  - You can use [Nocoffee chrome extension](https://chrome.google.com/webstore/detail/nocoffee/jjeeggmbnhckmgdhmgdckeigabjfbddl?hl=en-US) to experience color blindness vision and enhance use of color to convey info.
  - Use [High Contrast chrome extension](https://chrome.google.com/webstore/detail/high-contrast/djcfdncoelnlbldjfhinnjlhdjlikmph?hl=en) and check how your UI appear for high contrast users.
