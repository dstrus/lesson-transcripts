Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

We know how to make something happen when a form is submitted now, but that's of limited use, because we don't yet know how to access the _data_ from the form. Time to fix that.

To get the data from the form, we need to have the form. So we need to be able to get to that form from inside the `handleSubmit` function.

```js
function revealTitle() {
  let heading = document.querySelector('#album');
  heading.innerHTML = 'Night of the Salamander';
}

function handleSubmit(event) {
  event.preventDefault();

  let list = document.querySelector('#attendees');
  list.innerHTML = '<strong>It worked!</strong>';
}

let preorder = document.querySelector('p.dark');
preorder.textContent += '!';

let button = document.querySelector('#reveal');
```

"No problem," you may be thinking. This `form` variable should still be in scope inside this function, because it is global, and it's declared before the function is invoked. That's true. That variable _will_ still be in scope... but that's cheating. Why is it cheating? Well, we could use this same function to handle more than one event. We could have two forms on the page and reuse the same function to handle them both, and in that case, this `form` variable might be pointing at the wrong form. To be sure we've got the right form, the one that was actually submitted, we should get it from this `event` object that is passed in as an argument.

The `event` object has a property called `target` (`event.target`), and the target is the thing that the event happened to. If you click a button, the event target is the button. If you move your mouse over a paragraph, the event target is the paragraph. If you submit a form, the event target is the form. So we can create a new variable, local to this function, and set it to `event.target`.

```js
function handleSubmit(event) {
  event.preventDefault();
  let form = event.target;

  let list = document.querySelector('#attendees');
  list.innerHTML = '<strong>It worked!</strong>';
}
```

And now we have the form. Notice I did reuse the variable name `form`. That's totally fine. We've done it before, right? Now we just have two different variables that happen to share the same name in two different scopes. This `form` variable will go away as soon as we hit the closing curly brace.

Once you have the form, there are several ways of getting the data out of it. The easiest is to give each input a name. If you flip over to the HTML, you'll see that I've taken the liberty of doing just that,

```html
<form>
  <input name="email" placeholder="Email" type="email">
  <input name="guests" placeholder="# of guests" type="number">
  <button>RSVP</button>
</form>
```

The first input now has a `name` attribute with a value of `email`. The second input has a `name` attribute with a value of `guests`. Now these are _named_ inputs, and we can access them using their names, `email` and `guests`, respectively.

So I have `form`. Now `form.email` will get me that email input. It does not get me the value that is typed into the input; it gets me the actual `input` element itself. If I want to get the value that is typed in there, I need to say `form.email.value`. So now I can save that to a variable, and it will get me whatever is typed in there.

```js
function handleSubmit(event) {
  event.preventDefault();
  let form = event.target;

  let email = form.email.value;

  let list = document.querySelector('#attendees');
  list.innerHTML = '<strong>It worked!</strong>';
}
```

And then I can do something with it. Instead of printing out "It worked!", I could print out the email. So let's make this opening `<strong>` tag a string, concatenate that `email` variable, and then concatenate a separate string with the closing `</strong>` tag.

```js
function handleSubmit(event) {
  ...
  list.innerHTML = '<strong>' + email +'</strong>';
}
```

Let's see what this does. Type something into the email field, "a@a.com", submit the form, <em>et voilà</em>! "a@a.com" shows up. Excellent. That's how you get the data out of a form that has been submitted. It's as easy as that.

Now what if we type in a different email and submit the form again? How about "b@a.com"? That replaces it. "b@a.com" is here now _instead_ of "a@a.com". It would be nice if they were both there. It would be nice if we could keep a running list. We could try that.

What if our `innerHTML` had a `+=` instead of just an `=`?

```js
function handleSubmit(event) {
  ...
  list.innerHTML += '<strong>' + email +'</strong>';
}
```

Then we would be _appending_ this, instead of _replacing_ it. Let's try that. So, it's blank again, because we made a change to our code. Let's try "a@a.com", submit. Let's try "b@a.com", submit. And they're both there. Now, they're right next to each other, which is unfortunate; but they're both there, by golly, and that's something.

What if we replace the `<strong>` elements with `<p>` elements?

```js
function handleSubmit(event) {
  ...
  list.innerHTML += '<p>' + email +'</p>';
}
```

Resubmit, and now they're in separate paragraphs. Excellent.

Next time, we'll keep working with form data, but we'll also learn a new trick for dealing with strings called **template literals**. Get excited!

Until then, I'm Davey Strus. Haaaappy hacking!
