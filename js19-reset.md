Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

Right now, after we add an attendee, if we want to add a second one, we have to manually click back up here ourselves, highlight what's already there, backspace over it like some kind of animal. We don't want to do that to the nice people who use our form.

There are two parts to solving this. First, let's clear out the data that's in the form. All of this happens after we pull the existing data out of the form, so I'll just do it at the very end of our `handleSubmit` function. Now that I've done what I needed to do with the data, I can safely blow that data away. That's called **resetting** a form, and it's easy. Since we already have the form in a variable called `form`, it's as simple as `form.reset()`. Now `reset` isn't a piece of data, it's a function. It _does_ something, right? It clears out the data. So we'll need a set of parentheses there to invoke that function.

```js
function handleSubmit(event) {
  ...
  form.reset();
}
```

And that's all there is to clearing out the data in the form. So let's try it again. `a@a.com`, `2` guests... ooh, look at that! It cleared out as soon as I submitted the form, but my data still made it down here, so it didn't blow it away too early. Outstanding.

Now the other issue is that I want my cursor to go back to the email field, because I want to be able to add multiple attendees fairly quickly. So for that, I need to grab the email input again. We grabbed the _data_ out of the input up here with `form.email.value`. Remember, it wasn't just `form.email`; `form.email` grabs the actual `<input>`, because there's more you can do with the input than just read its value. For example, put the cursor back in it. So for that, all we do it `form.email.focus()`.

```js
function handleSubmit(event) {
  ...
  form.reset();
  form.email.focus();
}
```

And again, a set of parentheses, because this is performing an action, rather than retrieving or setting some data. It's putting the cursor back in that field. That is called **focusing** a field. A field that has the cursor is said to have **focus**. As you might guess, the opposite of focus is **blur**. If you want to make sure the focus is _not_ on a particular field, you can blur that field, but **focus** is what we want right now. Let's give this a shot.

Add another attendee with some guests, and not only did the form clear out, but my cursor went right back inside that email field. Outstanding. Nice improvement to the usability of the form.

I think we've added all the behavior we need to add with JavaScript. Nice work! But that list could look a little better, couldn't it? Let's learn some new CSS tricks to tidy that up.

That's next time. Until then, I'm Davey Strus. Haaaappy hacking!
