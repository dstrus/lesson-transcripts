Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

So far, all the JavaScript we've written has run as soon as the page loads. That makes some of these changes seem kind of pointless, because we could've just made those changes in the HTML. It's more interesting when the code runs in response to something else happening. Maybe someone clicked a button. Maybe they submitted a form. Maybe they hit a certain key on the keyboard. Wouldn't it be great if we could run some code in response to that sort of thing? Well, I wouldn't be suggesting it if we couldn't. We can! Enter: **Events**.

Here's the idea. We can ask the browser to invoke a function when something occurs. We tell the browser to _listen_ for that thing&mdash;that event&mdash; to occur. Events include things like clicks with a mouse, taps on a mobile device, keypresses on a keyboard, movement of a mouse, the submission of a form. All of these things are events, and we want to _handle_ them. What we're about to do is called **event handling**.

We need to tell the browser three things to set this up:

1. First, where to listen for that event. That is, what object on the page the event will happen _to_&mdash;a particular button, a form, a paragraph.
2. Second, what kind of event to listen for&mdash;a click, a mousemove, a keypress, that sort of thing.
3. And third, what function to invoke when that event finally occurs.

I said awhile back that there are certain things that we just can't do without functions. Handling events is one of those things. The only thing we can tell the browser to do in response to an event is to invoke a function.

In essence, we need to fill in these blanks:

> Listen to ____. When ____ happens, do ____.

That first blank is something that an even can happen to, often an element on the page, like an `h1`, `p`, `form`, or `button`. It's not enough to say "listen for a _click_"; you have to say _where_ to listen for a click. In most cases, you don't want to manually handle every click on an entire page, but you might interested in the click of a particular button, or a particular paragraph on the page. This is where you tell it _which_ button, or _which_ paragraph.

The second blank is the _type of event_ we're waiting on&mdash;click, submit, mousemove, stuff like that. We don't tell it to wait for just _anything_ to happen. We tell it to wait for something _specific_ to happen.

The third blank is what to do when the event occurs&mdash;what _function_ to invoke. For example...

> Listen to `myButton`. When `click` happens to that button, do the function `turnHeadingBlue`.

Naturally, the actual syntax isn't in such plain English, but the blanks are the same. First, you need to find the element. `querySelector` will do nicely for that.

```js
let myButton = document.querySelector('button');
```

Then, just like we say `document.querySelector()`, we say _that element_, effectively filling in the first blank, `.addEventListener()`.

```js
let myButton = document.querySelector('button');
myButton.addEventListener();
```

Because that's what we're doing, technically. We're adding something called an **event listener** to that element. `addEventListener` is a function, so we'll put a set of parentheses, and it takes two arguments. Want to guess what they are? They're the other two blanks! The first argument is what type of event we're listening for, as a string. For example, the string `'click'`.

```js
let myButton = document.querySelector('button');
myButton.addEventListener('click');
```

The second argument is the function we want to invoke when the event occurs. Just type the name of that function as the second argument.

```js
let myButton = document.querySelector('button');
myButton.addEventListener('click', turnHeadingBlue);
```

Notice I _don't_ include a set of parentheses after the function name. We're not invoking the function right now. We're asking the browser to invoke it for us later, after an event occurs. So the argument is the function itself, as though the function were just another variable. Now let's try it for real.

```js
function changeHeading(newTitle) {
  let heading = document.querySelector('#album');
  heading.innerHTML = newTitle;
}

changeHeading('Night of the <mark>Coriander</mark>');

let preorder = document.querySelector('p.dark');
preorder.textContent += '!';
```

Right now, `changeHeading()` runs as soon as the page loads. What if we didn't do that? What if we made it run in response to some event? Let's just get rid of the line where we invoke the function, and I'm going to take this opportunity to change its behavior so that it just uses a title that we hardcode in here, instead of passing in the new title as an argument.

```js
function changeHeading() {
  let heading = document.querySelector('#album');
  heading.innerHTML = 'Night of the Salamander';
}

let preorder = document.querySelector('p.dark');
preorder.textContent += '!';
```

OK, very good. Now what event should we listen for? Ooh, look at that! There's a button on the page now. As soon as we stopped calling `changeHeading()` first thing, we saw that in the HTML, the `h1` actually contains a `button` now, and it has an ID of `reveal`.

```html
<h1 id="album">
  <button id="reveal">Reveal Album Title</button>
</h1>
```

So what if clicking this button revealed the album title? We haven't made a major change to how `changeHeading()` works. It still grabs the heading from the page and then changes its `innerHTML`, but now what that's _effectively_ doing is revealing the title, not just changing the heading. So I'm going to rename the function `revealTitle()`. Do you understand why? Right now, when the page first loads, we don't see the title. We see that button instead. And as soon as we call or invoke this function, we'll see the title. So effectively, what that function is doing is revealing the title, so I wanted to update the name to reflect that. It's good to have names that accurately reflect what a function does.

So if we want this to run when that button is clicked, what can we do? First, we need to grab that button from the page.

```js
let button = document.querySelector('#reveal');
```

It had an ID of `reveal`, so that ought to work. Then, we need to fill in the blanks, right? First blank: What element the event happens to. That's `button`. Then, `.addEventListener()`. Then, the first argument to `addEventListener` is the second blank&mdash;the event we're waiting for, as a string. We're waiting for a click, so `'click'`. Then the second argument: What function we want to run when that click occurs, and that is the function `revealTitle`.

```js
let button = document.querySelector('#reveal');
button.addEventListener('click', revealTitle);
```

And I don't put a set of opening and closing parentheses after `revealTitle`. Of course, I want the closing parenthesis for `addEventListener`. And there we go. Let's see if it works.

Click the button, and there's the title. Voilà! That's a little more interesting than just having it change the title as soon as the page loads. We never even saw the old title before. Now, when we first load the page, we see a button. Click it to reveal. Very good.

JavaScript gets a whole lot more interesting with events. Next time, we're going to look at events some more. This time, we're going to see how to handle a form submission event.

That's next time. Until then, I'm Davey Strus. Haaaappy hacking!
