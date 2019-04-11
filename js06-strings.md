Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

Let's talk about text! I will once again be working in the JavaScript console in my web browser. You should do the same. Go ahead and open your console up if it's not already, and follow along. Feel free to pause the video as often as you need to, to keep up.

We've dealt with numbers. We know we can assign numbers to variables...

```js
let x = 4
```

And `x` is indeed `4`. Number literal, `4`, on the right side of the `=`. A variable that we're declaring, `x`, on the left. And from then on, that variable holds the number `4`.

Data in JavaScript has a data _type_. The data type of `x` is `number`. Straightforward enough. But we need to deal with _text_ data, and just as we can have _number literals_, we can have _string literals_. The data type for text is called `string`.

Unlike numbers, we can't just start writing text and have it work.

```js
Howdy, neighbor
```

It doesn't know where the string begins and ends. It's going to think that `Howdy` is the name of a variable. That's what it's going to think if it just sees `Howdy`. We need to tell it where the string literal begins and ends, and we do that with **quotation marks**. And we can use single quotes:

```js
'Howdy, neighbor'
```

...or we can use double quotes:

```js
"Howdy!"
```
The only difference between the two can be illustrated by a string that contains either an apostrophe or a quotation mark. If a string has an apostrophe in it...

```js
'Don't look!'
```

...and you used single quotes for your string, when it sees that apostrophe, it's going to think that's the end of the string. So you have to tell it, "No, I really want the apostrophe character here." So you **escape** that character using a backslash (`\`).

```js
'Don\'t look'
```

A backslash before the apostrophe lets it know this is not the end of the string; I actually want an apostrophe in the middle of this text.

If you're using double quotes, you have to do the same thing if a string contains double quotes in the middle. You have to put a backslash before that double quote, or it will think this is the end of the string.

```js
"It was 6\" from the wall."
```

I would encourage you not to mix single quotes and double quotes. Just pick a style, and stick with it. The JavaScript community seems to single single quotes a little more commonly than double quotes, so I'm going to use single quotes in all of my examples. You'll notice the output in the console always uses double quotes. That's fine. It makes no difference. The quotes aren't actually part of the string. They are simply how it notes the beginning and end of the string. The actual string is the text that appears in between.

So what can we do with this? Well, we can save a string to a variable.

```js
let greeting = 'Howdy'
```

Cool. All right, what can we do with it now that we have a variable? With numbers, we could do math. We can't exactly do math with a string, but let's try anyway.

```js
let name = neighbor
```

Let's see what happens. Try...

```js
greeting + name
```

...and I get `'Howdyneighbor'`. It smashes the two strings together, in the order that I placed them. Now this isn't really _addition_. This is something called **concatenation**. When you smash two strings together, you are **concatenating** those strings. Let's try this again.

```js
let firstname = 'Davey'
```

I'm going to put `'Davey'`, because that's my first name. Feel free to use your own.

```js
let lastname = 'Strus'
```

Try smashing them together. Ooh, what if we smash them together and save the result in a variable?

```js
let fullname = firstname + lastname
```

Can I do that? Let's check what `fullname` is... and, sure enough, it's `'DaveyStrus'`. I wish there were a space between the two, but I didn't put a space in either one of those strings, and I didn't put a space in between them, so there's no space there. It only does exactly what you tell it to do. We told it to smash the two string, `firstname` and `lastname` together, and it did exactly that. How should it know you wanted a space in between? But hey, how about `' '`? Quote-space-quote? Is that a valid string? Sure it is! It's a string containing just a space. So what if I said...

```js
fullname = firstname + ' ' + lastname.
```

(Notice I left the `let` out, because it's already been declared.)

Holy smokes, it worked! It put the space there: `'Davey Strus'`. Wonderful. So that's string concatenation. Can I _multiply_ a string by a string?

```js
firstname * lastname
```

No, that doesn't make any sense, and it gives us this special value: `NaN`, which means "not a number". `firstname * lastname` isn't a number. It's not _anything_. So that's no good. How about...

```js
firstname * 3
```

Also `NaN`. OK, so we can't multiply strings. Fair enough. How about adding a string to a number?

```js
firstname + 6
```

Oh, it's the string `'Davey6'`. That's interesting. So, again, it doesn't actually perform _addition_. It does _concatenation_. It will just turn the number into a string, so instead of adding `firstname` to `6`, it added `firstname` to the _string_ `'6'`. It just assumed you meant the string `'6'`, not the number, because the number doesn't make any sense. So it automatically converts the number `6` into the string `'6'` and smashes the two strings together. Interesting.

So this is a very brief overview of how strings work in JavaScript, but we'd like to do more things with them. We'd like to be able to use this stuff to actually manipulate a web page, not just work inside the browser console. So that's what we'll do next. We'll actually start to use JavaScript to manipulate a web page.

Until then, I'm Davey Strus. Haaaappy hacking!
