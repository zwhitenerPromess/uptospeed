## Forms Exercise

Forms are pretty much everywhere on the web and are necessary when getting information from a visitor.

Here is the top level explanation of how a form works:

1. A user visits a page that contains a form.
2. The web browser displays the html containing the form, the user fills out the form and submits the information.
3. The browser sends the submitted form data to the web server.
4. The server side script expecting the post request from the form parses the information and does what it needs to do with it (send an email, save in a database, etc.)\
5. A response page is sent back to the browser.

This process may be a little different if the form is sent through ajax, but that concept will be tackled in the javascript challenges.

Revisiting the contact form:

```html
<form action="/api/call" method="post">

  <label for="name">Full Name</label>
  <input id="name" type="text" name="name" placeholder="Please enter your name" required />
  <label for="email">Email</label>
  <input id="email" type="email" name="email" placeholder="Please enter your email" required />
  <button type="submit">Submit</button>
</form>
```

The labels and inputs guide the user to put in certain types of information. The form tag provides a container for the information that is to be sent to the server. The `action="/api/call"`
attribute means the information in the form is to be sent to that url path where a server side script is waiting to parse the information. The `method="post"` is a request method supported by
the HTTP protocol. The HTTP protocol is an essential concept to understand for web development, but out of scope for this exercise.

For reference, here is a basic Express.js/Node.js (javascript on the server) script to parse the above contact form.

```js

app.post('/api/call', function(request, response) {

  var name = request.body.name; // the name entered in the form
  var email = request.body.email; // the email entered in the form

  /**

  do something with the name and email

  **/

});

```
