Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

We now know how to add brand new content to a page using `document.write()`. Now it's time to learn how to modify _existing_ elements.

First, we need to learn how to grab existing elements from the page, then we need to learn how to change their contents with JavaScript. Ready?

Go ahead and code along with me using the editor on the page, and remember to pause as often as you need to, in order to keep up.

Here's our Beasley the Bard project as we last left it, with plenty of HTML and CSS already there. Let's see if we can grab the `h1` off the page to use in JavaScript.

This is going to require us to work with the DOM, so we'll start with `document`. And this time, what we want is `document.querySelector()`. Notice the capital `S` for `Selector`. This is called **camel case** (because of the hump in the middle), and it's the most common way to have a single name with more than one word in it. You separate multiple words by a capital letter. So the very beginning, the `q` in `querySelector`, is lowercase; and you capitalize each additional word in that name. So lowercase `q`, capital `S`, `querySelector`.

This time, inside the parentheses, we also want a string, but the string this time is a **selector**. That sounds familiar. Remember what a selector is? A selector goes as the beginning of a CSS rule to tell CSS which elements on the page the rule applies to. And they can be as simple as a tag name, like `h1`. Now in JavaScript, the selector needs to be a string, so we'll put `h1` inside quotes.

```js
document.querySelector('h1');
```

And that ought to do it. `querySelector` will grab the first element on the page that matches the selector you give it. There's another version called `querySelectorAll` that finds _all_ elements that match the selector and stores them in a sort of collection, but that's beyond our needs right now, so we're just going to use `querySelector`. And notice that I have a semicolon at the end of the line, as always. Now let's save the result to a variable. I'm going to name the variable `heading`.

```js
let heading = document.querySelector('h1');
```

Now you can name that variable anything you want. You could name it `h1` if you wanted to, but I wanted to make the point that it doesn't _need_ to be named `h1`. That is how you grab an element from the page.

Now we want to know how to modify that element's contents. There's more than one way to do it. One way: Reference that variable where you stored the element, in this case `heading`, and say `.textContent`. Notice the capital `C` in `textContent`.

```js
heading.textContent
```

And then you can _assign_ something to this text content. So an equals sign, and then some string.

```js
heading.textContent = 'Howdy';
```

And look at that: The `h1` changed to "Howdy". Beautiful!

Remember `+=`? We used it with numbers to add something to the value that's already in a variable. For example, `x += 2` means "add 2 to the current value of `x` and save the value back in `x`." Think we could do that with `textContent` as well? Worth a shot!

```js
heading.textContent = 'Howdy';
heading.textContent += ', neighbor!';
```

Look at that! It adds ", neighbor!" to the end of "Howdy", which is what is in `textContent` prior to that line. Neato!

Now I don't really want to call it "Howdy, neighbor!", so let's just change it from its original "Night of the Salamander" to "Plight of the Salamander" just to prove that we have, in fact, changed it with JavaScript.

```js
let heading = document.querySelector('h1');
heading.textContent = 'Plight of the Salamander';
```

There we go. Excellent.

What do you think would happen if we stuck some HTML in that string like we did when we used `document.write()`? Let's just put an `<em>` around "Salamander"...

```js
let heading = document.querySelector('h1');
heading.textContent = 'Plight of the <em>Salamander</em>';
```

Oh no! Look what it did! It actually put `'<em>'` on the page. `textContent` is pure _text_. If you put HTML in there, it will print the HTML as text. It will not interpret it as HTML. So we can't do this. That's a bummer. If only there were some way to do that....

Of course there's a way to do that! Instead of `textContent`, simply use `innerHTML`. Notice `HTML` is all-caps.

```js
let heading = document.querySelector('h1');
heading.textContent = '<em>Flight</em> of the Salamander?';
```

There we go. "Flight" is italicized. The HTML in the string _is_ recognized, and there we have it.

So now we know how to grab elements from the page using `querySelector()`, and we know how to modify the contents of an element with `textContent` and `innerHTML`.

Sometimes you need a selector that's more specific than just "grab the first element of a particular type," so next time, we'll learn how to target elements a little more specifically using some different selector syntax.

Until then, I'm Davey Strus. Haaaappy hacking!
