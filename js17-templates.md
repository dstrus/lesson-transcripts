Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

We often need to include the value of a variable within a larger string. So far, we've done that using concatenation&mdash;adding strings together with a `+` operator. That works fine, but it can get a little messy, especially once you start needing to use more than one variable in a single string.

```js
'<p>' + email + '</p>'
```

Here's a perfectly good way to include the value of a variable called `email` inside a longer string containing an HTML paragraph. We have a string literal containing an opening tag, we concatenate a string variable called `email`, and we concatenate another string literal containing the closing tag. We can replace all of this with a single literal, called a **template literal**.

Template literals produce strings, just like regular string literals do.

```js
`<p>${email}</p>`
```

Instead of quotation marks, they begin and end with a backtick. On most keyboards, that's in the upper-left, just under **esc**. What's special about template literals is that we can do something called **interpolation**, which means we can actually embed expressions inside the literal, without concatenation. Just use a `$` followed by a set of curly braces. Inside the curly braces, you can put a variable or any expression, and it will be evaluated and its value included in the resulting string.

```js
'<p>' + email + '</p>'

`<p>${email}</p>`
```

These two literals produce exactly the same string, and personally, I have a terrible time making sure all my quotes are in the right place in that first example. I find the template literal far preferable. Let's use it in our Beasley page.

Let's replace all this concatenation with a single template literal...

```js
function handleSubmit(event) {
  ...
  list.innerHTML += `<p>${email}</p>`;
}
```

...and it works just like what I had there before. Let's try it out. "a@a.com"... boom. Still works.

Now, why don't we add the number of guests? We just need to grab that from the form. Remember our first input had the name `email`. That's why we could do `form.email.value`. We could also use `form.guests.value` to get whatever was typed into the second input.

```js
function handleSubmit(event) {
  ...
  let email = form.email.value;
  let guests = form.guests.value;
  ...
}
```

And then after we print the email, let's add "plus" and then whatever number they put there.

```js
function handleSubmit(event) {
  ...
  list.innerHTML += `<p>${email}, plus ${guests}</p>`;
}
```

Let's give that a shot. Great! But I kind of liked it when the email was in bold, so let's go ahead and wrap that in another `<strong>`, leaving the paragraph tags, just adding the strong tags.

```js
function handleSubmit(event) {
  ...
  list.innerHTML += `<p><strong>${email}</strong>, plus ${guests}</p>`;
}
```

I find it much easier to do this stuff when using a template literal. It's just much tidier than having a bunch of `+` signs and closing quotes all over the place. Let's see if I did it right... very good. And let's make sure I can still add a second one... yep, still works. Each one is in its own paragraph, the email is bold, and print the number of guests alongside it.

So that's the template literal. Pretty handy.

Next time, we'll look at using **lists** in HTML, and we'll add items to a list using JavaScript.

Until then, I'm Davey Strus. Haaaappy hacking!
