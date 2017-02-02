## Display and Layout Exercise

Exercises are small challenges or tidbits of information to get familiar with important concepts. Exercises don't need to
be uploaded to github, however, you can if you want to. Go to [codepen](codepen.io) to try out some of the exercises.

Knowing how to display html elements is really important when trying to build layouts. Before trying to explain the benefits and quirks myself, there
is a really good article that will serve as a good introduction: [learn css layout - the display property](http://learnlayout.com/display.html).

tldr; There are a ton of display properties, some you'll use often, some you'll probably never touch. They're still good to know, along with the default
display properties on elements. For example - p, header tags, lists, divs, etc. are display block by default and as a result of this they take up as much
horizontal space as their parent element will allow.

```html
<div class="parent">
  <div class="child">
  </div>
  <a href="#">Click me</a>
</div>
```

```css
.parent {
  width: 500px;
  margin: 0 auto;
  padding: 100px 0; /* to give the div some height */
  background: blue;
}
.child {
  padding: 100px 0; /* to give the div some height */
  background: black;
}
a {
  color: white;
}
```

How wide will the child div be? How about the anchor tag? The reason the child div is just as wide as the parent element is because it is a block element and the
reason the anchor tag doesn't follow suit is because it is an inline element, meaning it only takes up as much horizontal space as the content it holds. Inline elements also
won't interrupt flow. You can put three inline elements next to each other and they'll lie along the same line. But when you go to assign a height or width to an inline element
you'll run into a problem - it doesn't work. That's where `display: inline-block` comes into play. Open up codepen and copy the code above. Mess around with the display, width, etc.
of elements and see what happens. 
