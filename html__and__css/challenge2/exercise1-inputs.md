## HTML Inputs Exercise

Inputs provide a medium for users to give custom information to an application. Think about a typical contact form that you might see on a local business's
website. The contact forms purpose is to get inquiry information from the visitor of their website. This form provides a means of communication from the user to
the websites server. The inputs are the elements that actually collect the information.

The contact form may look something like this:

```html
<form action="/api/call">

  <label for="name">Full Name</label>
  <input id="name" type="text" name="name" placeholder="Please enter your name" required />
  <label for="email">Email</label>
  <input id="email" type="email" name="email" placeholder="Please enter your email" required />
  <button type="submit">Submit</button>
</form>
```

Pretty simple stuff. This form just grabs the name and email from whoever is filling out the form and sends the information to the "/api/call" url endpoint. But don't worry about
how a form works for right now, that will be covered in future exercises and the upcoming challenge. Notice all of the different attributes on the input tags, especially the type
tag. The type tag specifies what kind of information the input should expect. The first input tag is expecting some string of text while the second input tag is expecting an email.
There are loads of "types" that input tags can accept. Check out the [w3schools tutorial on input tags here](http://www.w3schools.com/tags/tag_input.asp). Open a new pen on codepen
and try out some of the input types and see how they change based off the type.

Note that some browsers interpret input types differently, so that's something to keep in mind to avoid bugs. For example, the "datetime-local" type works great in Chrome, but in Firefox
not so much.
