# css3-mixins-tricks
Tips &amp; Tricks, A bunch of tips and tricks I've learned and found very helpful.


## Best Practice

It's important when building a web page to avoid unecessary element, to remind this there is some tricky way using css3.
In the sample below we will display a counter within a badge 
See sample below:

#bad practice

## HTML

```html
<div class="dropdown" is-open="notification.isOpen"> 
    <span></span>
    <button data-count="{{notification.count}}" class="dropdown-toggle icon alert-btn"></button> 
    <div class="dropdown-menu" ng-click="$event.stopPropagation();"> 
        <!-- Drop down list content -->
    </div> 
</div>
```

## CSS



#good practice

#HTML


#CSS

```css
  .alert-btn:after { 
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

