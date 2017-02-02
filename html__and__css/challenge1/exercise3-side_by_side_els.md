## Side by Side Elements Exercise

Exercises are small challenges or tidbits of information to get familiar with important concepts. Exercises don't need to
be uploaded to github, however, you can if you want to. Go to [codepen](codepen.io) to try out some of the exercises.

Exercise 2 talked a little bit about the display property and how block elements take up a lot of width. This presents a problem
of trying to juggle using block elements with declarative sizing, but not having the benefit of displaying multiple elements side
by side like inline elements.

`display: inline-block` is the best of both worlds. First try laying out a bunch of divs normally:

```html
<div></div>
<div></div>
<div></div>
<div></div>
<div></div>
<div></div>
<div></div>
```

```css
div {
  width: 14%;
  height: 400px;
  background: skyblue;
}
```

Notice how the divs just lay down vertically. Now make them inline-block:

```css
div {
  width: 14%;
  height: 400px;
  background: skyblue;
  display: inline-block;
}
```

The elements flow just how we need them to. This isn't the only way to make block elements flow like this. You could use the float property, flexbox, or tables.
Check out this [article](http://blog.karenmenezes.com/2014/apr/13/floats-inline-block-or-display-table-or-flexbox/#wrapper) for the advantages/disadvantages of
using each method and then try them for yourself.
