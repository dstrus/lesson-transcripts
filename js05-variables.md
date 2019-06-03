Hi, everyone. Welcome to Kenzie Academy. This is Davey Strus.

Ultimately, we want to understand all of the JavaScript that you see here:

```js
function revealTitle() {
  let heading = document.querySelector('h1#album');
  heading.innerHTML = 'Night of the Salamander';
}

let preorder = document.querySelector('p.dark');
preorder.textContent += '!';

function handleSubmit(event) {
  event.preventDefault();
  let form = event.target;
  let email = form.email.value;
  let guests = form.guests.value;

  let list = document.querySelector('#attendees');
  list.innerHTML += `<li><strong>${email}</strong>, plus ${guests}</li>`;

  form.reset();
  form.email.focus();
}

let button = document.querySelector('#reveal');
button.addEventListener('click', revealTitle);

let form = document.querySelector('form');
form.addEventListener('submit', handleSubmit);
```

In fact, we're going to _write_ all of this JavaScript. Right now, we don't really understand any of it, despite having taken our first steps into learning JavaScript.

An awful lot of these lines begin with the word `let`, and it turns out all of those lines are creating **variables**, so it's time to learn about variables.

Go ahead and code along with me in your browser's JavaScript console. If you've closed the console, you can reopen it with **Shift** + **Ctrl** + **J**, or **Option** + **Command** + **J**. And if you already have a bunch of stuff in your console, like I do, you can click the 🚫 button to clear it. There we go.

Now then, let's create a variable. First, the word `let`. Then, a name we want to give to identify our variable. How about `x`? That'll do fine. There are some rules you have to follow when naming a variable. It can only contain letters, numbers, underscores (`_`), and, strangely enough, `$`; and the first character cannot be a number. It cannot start with a number, but it can have a number anywhere else in the name. But no spaces, no dashes, nothing like that. Just letters, numbers, `_`, and `$`.

So, `let` and then our variable name `x`, then an equals sign, then what we want the value of `x` to be. How about `4`?

```js
let x = 4
```

That does exactly what it sounds like. It creates a variable called `x` and gives it the value `4`. Now you'll see that the console says `undefined` after you press **Enter**. Don't worry about that. That doesn't mean that it didn't work. That simply means that the expression `let x = 4` happens to evaluate to... essentially _nothing_. But if we type `x` and hit **Enter**, we'll see that it is `4`. That means that we could use the variable `x` anyplace that we can use the number _literal_ `4`. So:

```js
x + 3
```

`7`!

```js
x + 2 * 3
```

`10`!

```js
(x + 2) * 3
```

`18`! Perfect. How about multiple variables in a single expression? Sure, we can do that. How about...

```js
let y = 3
```

and then...

```js
(x + 2) * y
```

Still `18`. So anyplace that you could use a number literal, you could also use a variable that happens to hold a number. From now on, `x` is always the same thing as just writing `4`. Now that is not the _digit_ `4`, that's the _number_ `4`. So you couldn't say `1x` and expect to get `14`. It replaces the full number `4`. `1x5` is not `145`. It's nothing. It doesn't make any sense in JavaScript. Got it?

We could change the value of one or more of these variables. If we just type...

```js
x = 5
```

(Notice I do not type the word `let` this time.) And if I try some of these again...

```js
x + 3
```

That is now `8`. So I have **reassigned** `x` to a new value. I don't use the word `let` again. If I try...

```js
let x = 6
```

> Uncaught SyntaxError: Identifier 'x' has already been declared

...it will complain at me. "Identifier 'x' has already been declared."

The word `let` **declares** a variable, meaning that it brings it into existance. `x = [some number]` **assigns** the variable&mdash;that is, it gives it a value. When you give it a value for the first time, that's called **initializing** the variable, and we can declare and initialize the variable on the same line by saying `let x = [some number]`. But we could have originally put `let x` on a line by itself. We don't have to set an initial value. We don't have to say `let x = 4` or something; we can just say `let x`, and the variable will come into existance, and we only assign it a value later. Totally valid. You can reassign the variable as many times as you need to. I could say...

```js
x = 7
```

And then `x + 3` is `10`, as we would expect.

So **declare** a variable with `let`; **assign** a variable with `=`; reassign a variable again by using `=` and simply leaving off the word `let`.

Got it?

This is getting a bit busy, so I'm going to go ahead and clear my console again. Now the right side of the equals sign in a variable assignment could be an expression instead of simply a number literal. `x` still exists right now; it's `7`, so I could say...

```js
x = y + 4
```

and, well, `x` happens to be `7` again, because `y` was `3`, right? How about...

```js
x = y + 6
```

And I get `9`. So `x` is now `9`. Ooh, what if I say...

```js
x = x + 1
```

Do you think this works? It gave me `10`. Sure, it just evaluates the right side of the equals sign first. So whatever `x` was at the time is used for the value of `x` on the right side of the equals sign, and then when that's done, it assigns the new value to `x`. `x` now is `10`. This is a pretty common thing to do, in fact, so there's a shorthand for it. `x +=`, and then the value that you want to add to it. So...

```js
x += 2
```

...gives us `12`. And that is the same as writing `x = x + 2`. Exactly the same thing. This may not seem like a big deal, but it's really handy when your variable names get a bit longer than just `x`. It saves you some typing, and you avoid some repetition that sort of clutters things up and makes it a tiny bit harder to read. I'm always interested in making code more readable.

Variables are incredibly useful, because we need to store and reuse values all the time. Don't worry: There's a lot more to programming than just math. In fact, much of the time, we're manipulating _text_, rather than manipulating numbers, and that's what we're going to do next. We're going to learn how to work with text using something called a **string**.

That's next time. Until then, I'm Davey Strus. Haaaappy hacking!
