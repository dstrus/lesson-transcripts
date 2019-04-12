Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

Well, we've handled a relatively simple event. Let's try something a little more interesting. Let's try doing something when a form is submitted.

On the surface, this sounds like it ought to be easy enough. Follow the filling the blank formula from last time.

> Listen to [some element]. When [an event] happens, do [a function].

Grab the form with `querySelector()`, call `addEventListener()` on it, and pass the two arguments. First, the type of event&mdash;`'submit'` this time&mdash;and then a function.

```js
let form = document.querySelector('form');
form.addEventListener('submit', handleSubmit);
```

And yes, that formula still works. But the function we use to handle the event has some extra work to do this time. The thing is, the browser already does something when you submit a form, even without your handling it. That's not true of button clicks, unless the button happens to be the submit button in a form. Regular buttons do nothing when clicked, by default. If you want them to do something, you have to handle the event yourself, as we did last time. With a form submission, however, the browser actually makes a new request&mdash;a bit like it does when you browse to a new page. If the HTML doesn't specify otherwise, it requests the page you're already on. So it's a bit like hitting the **refresh** button, except that some form data gets transmitted along with it.

A refresh like that interrupts the execution of our JavaScript. It will start the JavaScript over from the beginning, and any changes we've made to the page's contents will be undone. Let's try it out and see what happens.

First, we'll grab the form from the page. I'll create a variable called `form`. I'll use `querySelector()` with the selector `form`. It's the only form on the page, so that's good enough, to select it by element type.

```js
let form = document.querySelector('form');
form.addEventListener('submit', revealTitle);
```

Then we'll add an event listener to that form, and the event will be... not `'click'` this time, but `'submit'`. And I'm just going to run `revealTitle` again. We'll write our own function later, but for right now, this is good enough for our purposes. Just make sure you don't click the "Reveal Album Title" button before you submit the form, or the title will already be revealed.

The form doesn't fit in the preview at the same time as the album title, so I'm going to click the **`0.5x`** button in the editor, so I can see both. Then it doesn't really matter what I type in here; I just need to submit the form, so I'll go ahead and click the submit button (labeled "RSVP").

Did you see what happened? It happened very quickly. Let me do that one more time. Submit the form; keep your eye on the `h1`... and it _does_ show up, _briefly_, before going back to the button. Because this process of adding the event listener still works for form submission. It does, in fact, run `revealTitle` when we submit the form, but it also refreshes the page very quickly, because it actually submits the form. Because again, the browser already does something by default when we submit a form, in addition to whatever we tell it to do using JavaScript. So while it does change the `h1`, it also submits the form and reloads the page. So what we need to do is prevent that default action from happening. So let's try some things.

First, I'll stop reusing `revealTitle` and write a separate function to run when we submit the form. I'll put it right after `revealTitle`. I'll call it `handleSubmit`, because that's its job.

```js
function handleSubmit() {

}
```

Right now, it doesn't really matter what it does, as long as it does something. We just want to prove that we can make _something_ happen when we submit a form. We don't really care _what_. I'm happy with just writing "It worked" on the page, but where on the page should we write that?

If you look at the HTML, you'll see that I've added a new element after the `h1` and `p` with the class `dark`&mdash;so right inside the gray box, at the bottom. It's a `div`, which is a semantically meaningless container element, with an ID of `attendees`. So one of these days, that `div` is going to contain a list of everyone who is attending the party. But right now, I just want to prove that I can grab it from the page and put _something_ in it. So that's what we'll do in `handleSubmit`.

Someday this is going to be a list of attendees, so I'll call my variable `list`, and I'll grab that attendees `div` from the page with `document.querySelector('#attendees')`. And then I just want to change its contents to say, "It worked!" I'll go ahead and put that in bold, so I'll use `innerHTML`, rather than `textContent`, so I can wrap it in a `strong` element.

```js
function handleSubmit() {
  let list = document.querySelector('#attendees');
  list.innerHTML = '<strong>It worked!</strong>';
}
```

Now before we hook this up to the form, let's make sure this function works when we just run it. So I'm just going to go ahead and run `handleSubmit()`.

```js
handleSubmit();
```

There we go. It worked! Good. I don't actually want to run it here. Instead, I want to run it when I submit the form. So all the way at the bottom, where I have `revealTitle`, I will change it to `handleSubmit`.

```js
form.addEventListener('submit', handleSubmit);
```

Now let's try sunmitting the form. And what do we see? "It worked!" showed up very briefly and then disappeared because, again, the form actually got submitted, and the page refreshed. So that's what we want to prevent. And here things get pretty interesting.

Remember, we're not the ones actually invoking the function that handles the event. The browser invokes it for us after the event occurs, so it's the one effectively putting a pair of parentheses at the end and actually invoking the function. Well, it turns out, it always passes an argument&mdash;it always puts a little something inside those parentheses, whether we ask for it or not. We didn't ask for anything up here...

```js
function handleSubmit() {
  ...
}
```

...when we actually wrote the function. There's nothing inside the parentheses here. It doesn't care. It's going to put something there anyway. So as long as _we_ include it...

```js
function handleSubmit(event) {
  ...
}
```

...we'll be able to use it. And that thing that it passes in is an _event_. It's the event itself, with all kinds of information about the event, including what type of event it was, which element on the page the event happened to, and quite a bit more. So that's going to get passed it automatically, just because this function is handling an event. We'll always receive this event argument, so we should put it inside the parentheses here, so we can actually use it. And one thing we can do with that is call a function called `preventDefault()`.

```js
function handleSubmit(event) {
  event.preventDefault();

  let list = document.querySelector('#attendees');
  list.innerHTML = '<strong>It worked!</strong>';
}
```

So `event.preventDefault()`, camelCase of course, and that does exactly what it sounds like. Because this event that occurred, a form submission, has a default action associated with it, we can prevent that from happening just by doing this. Now let's see what happens.

I submit the form, and it says, "It worked!", and "It worked!" stays around. It doesn't refresh the page afterward, because we prevented that from happening. Pretty cool.

It's very easy to forget to do this and to start banging your head, because your form event handler isn't working. Just remember, if you see it work very briefly, and then the page refreshes, it's because you forgot to `preventDefault()`.

So now that we know basically how to handle form events, let's see if we can make it a little more useful by actually using the data that's typed into the form.

But that's next time. For now, I'm Davey Strus. Haaaappy hacking!
