# css3-mixins-tricks
Tips &amp; Tricks, A bunch of tips and tricks I've learned and found very helpful.

## Css3 Best Practice

It's important when building a web page to avoid unecessary element, to remind this there is some tricky way using css3.
In the sample below we will display a counter within a badge.

-
**Note:** 
*The content property is used with the :before and :after pseudo-elements, to insert generated content.*
*The attr() CSS function is used to retrieve the value of an attribute of the selected element and use it in the style sheet. It can be used on pseudo-elements too and, in this case, the value of the attribute on the pseudo-element's originated element is returned.The attr() function can be used with any CSS property.*

See sample below:

#bad practice

**Example:**

![Alt text](/screenshots/sample.jpg?raw=true "Example")

**HTML:**

```html
<a href="#">Inbox <span class="badge">42</span></a>

<button class="btn btn-primary" type="button">
  Messages <span class="badge">4</span>
</button>
```

**CSS:**

#good practice

**HTML:**

```html
<a href="#" data-count="4">Inbox <span class="badge">42</span></a>

<button data-count="4" class="btn btn-primary" type="button"></button>
```

**CSS:**

```css
  .btn:after { 
    position: absolute; 
    z-index: 1; 
    top: 2px; 
    right: 5px; 
    content: attr(data-count); 
    display: block; 
    width: 13px; 
    height: 13px; 
    border: 1px solid #FFF; 
    border-radius: 13px; 
    background-color: #C30019; 
    font-weight: bold; 
    white-space: normal; 
    color: #FFF; 
    text-align: center; 
    font-size: 9px; 
  } 
```

