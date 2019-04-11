Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

Now that we have a basic understanding of functions, let's put that understanding to good use.

```js
let heading = document.querySelector('#album');
heading.innerHTML = 'Night of the Coriander';

let preorder = document.querySelector('p.dark');
preorder.textContent += '!';
```

The first thing we do in this JavaScript is grab the heading from the page and change its `innerHTML`. What if we did that inside a function? Let's give it a shot.

We'll add a new line at the beginning... and how do we declare a function? The word `function`, followed by what we want to name the function. So what does this function do? Well, it changes the heading, doesn't it? So let's call it `changeHeading`. I always like to make my function names verbs or verb phrases. Very good, then a set of parentheses, a curly brace. We'll need another curly brace after those two lines.

```js
function changeHeading() {
  let heading = document.querySelector('#album');
  heading.innerHTML = 'Night of the Coriander';
}
```

And I always like to indent the contents of the function. So everything between the two curly braces should be indented. This is a pretty much universal convention. Always indent the contents of the function. It makes it much easier to tell where the function begins and ends.

CodePen (the editor on the page) makes this really easy. Just highlight the two lines, and hit **tab**. _Et voilà!_ They're indented now, and we have a function.

Now notice the title is back to "Night of the Salamander", because now the code in the function doesn't ever run. We need to actually invoke the function if we want that to happen, right? So after we declare the function, let's go ahead and invoke it.

```js
function changeHeading() {
  let heading = document.querySelector('#album');
  heading.innerHTML = 'Night of the Coriander';
}

changeHeading();
```

And there we go: "Night of the Coriander". It does the same thing it did before we started, but now it does it all in a function.

Let's make it a little more interesting. Let's pass the new title in as an argument. So we'll change the function to receive an argument inside its parentheses. We'll call that argument. `newTitle`. Now that gives us a new local variable `newTitle` to use inside the function. And instead of setting `innerHTML` to the string `'Night of the Coriander'`, we'll set it to whatever the value of `newTitle` is.

```js
function changeHeading(newTitle) {
  let heading = document.querySelector('#album');
  heading.innerHTML = newTitle;
}

changeHeading();
```

When we invoke the function, we don't pass anything yet as the argument, so we get `undefined`. Swell. But we can put any string we want inside those parentheses, and that will get set to `newTitle` inside the function. So let's set it back to `'Night of the Coriander'`...

```js
function changeHeading(newTitle) {
  let heading = document.querySelector('#album');
  heading.innerHTML = newTitle;
}

changeHeading('Night of the Coriander');
```

...and it worked! Let's fancy this up a little bit. Let's wrap "Coriander" in a new HTML element called `mark`. We haven't used this one before.

```js
changeHeading('Night of the <mark>Coriander</mark>');
```

You can see what it does. It highlights it. Cool! And now we are using a function in our JavaScript. The benefits of having wrapped this in a function may not be obvious at this point. It helps us organize our code, and it actually enables us to do some things that we just plain couldn't do without functions. We'll see an example of that pretty soon. But first, we'll take a little aside to go over some vocabulary. That's next time.

Until then, I'm Davey Strus. Haaaappy hacking!
