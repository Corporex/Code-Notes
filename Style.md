#Style

### a. Working with focus styles
- The pseudo code `focus` only matchend when an element has __focus__:
```
:focus {
//Use the "outline " property to change the appeareance of the focus ring
outline: 1 pc dotted #fff; 
}
```

__NOTE__: This is a __MAJOR__ _anti-pattern_
- Without a focus indicator, a user does not know which keyboard element to interact with.

```
:focus {
outline: 0; 
}
```
Alternatives are:
1) __Give your element the same hover focussed styles__
```
button:hover,
button: focus {
background: #e91e63;
color: #fff;
text-decoration: underline;
}
```
2) __Use a specific focus pseudo class in CSS__ 
(to get a consistent indicator across browsers)
```
button: focus {
outline: 0;
box-shadow: 0 0 8px 3 px;
rgba (255, 255, 255, 0.8);
}
```

3) Delete default focus indicator, use focus style
```
.radio:focus {
outline: 0;
}

.radio:focus::before {
box-shadow: 0 o 1px 2 px #5b9dd9;
}
```
- Leave the default focus ring in place.
- If you want to change, use the :focus pseudo class to create your own styled focus indicator.
- [Exercice](https://github.com/udacity/ud891)

#### Resources 
- [WebAim-2.4.7 checklist](https://webaim.org/standards/wcag/checklist#sc2.4.7).
- [:focus](https://developer.mozilla.org/en-US/docs/Web/CSS/:focus)
- [outline](https://developer.mozilla.org/en-US/docs/Web/CSS/outline)
- [:hover-pseudo-class](https://developer.mozilla.org/en-US/docs/Web/CSS/:hover)
- [::before-pseudo-element](https://developer.mozilla.org/en-US/docs/Web/CSS/::before)
- [video- Styling for focus :focus pseudo selector](https://youtu.be/ZooEnrj8aMc).


Input Modality
Styling with Aria
Responsive design for multiple-devices
Mobile Screen Readers
Seque to Color & Contrast
Contrast Requierements

 

- [video_ Styling native/non-native buttons](https://youtu.be/bfPGicTGBTI).

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
  - You can use [High Contrast chrome extension](https://chrome.google.com/webstore/detail/high-contrast/djcfdncoelnlbldjfhinnjlhdjlikmph?hl=en) and check how your UI appear for high contrast users.
  