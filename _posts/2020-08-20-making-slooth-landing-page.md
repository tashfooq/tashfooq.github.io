---
title: Making Slooth Landing Page
date: 2020-06-23
categories:
- Bootstrap
- HTML
- CSS
---
### Slooth
It's an app I'm currently working on where customer can order farm fresh products straight to their doorstep. In the process of making the landing page for the app I learned some cool bootstrap and CSS tricks.

<!-- more -->

### Resize the line break 
I typically use the ```<br>``` tag for line breaks and adjust the height with
```css
 {
  line-height: 150%;
}  
```
However this needs to be applied to the parent so the entire paragrap would have a larger line-height.
The solution was to
```css
br {
    content: "";
    margin: 2em;
    display: block;
    font-size: 24%;
}
```

### Ordering columns in bootstrap when page shrinks 
In Bootstrap 4 one can simply assign ordering classes to columns
```html
order-first
order-second
order-last
order-0
order-1
```