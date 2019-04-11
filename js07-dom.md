Hey, everyone. Welcome to Kenzie Academy. This is Davey Strus.

We want to actually manipulate web pages with JavaScript. It's time to start talking about the **DOM**, or **Document Object Model**. When the browser looks at our HTML, it builds this model out of it, representing every element and every piece of text as a sort of _object_ that can be manipulated with JavaScript. This is the DOM.

We've seen that we can make up variables with names that we choose, but there's a variable that JavaScript sets for us called `document`, and we can use that to access the DOM.

Let's go ahead and play around with the DOM a little bit. Use the editor on this page to code along with me, and remember to pause as often as you need to, to keep up.

We'll start by typing `document`.

```js
document.write()
```

`document.write` and then a pair of parentheses. Inside the parentheses, we can put any string.

![linear gradient](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/codepen-error.png)

Notice that it freaks out a little bit that I have an "unterminated string constant" . That simply means I haven't put the closing quote yet. If you pause a little too long as you're typing the string, the editor on the page will get a little alarmed. Not to worry. Just go ahead and put that closing quote. Now since we're actually writing inside a JavaScript document here, we're going to start putting semicolons at the end of each line of code. There are some exceptions. You don't put a semicolon after absolutely everything, but we'll talk about those exceptions as we come to them. And you can choose to leave semicolons out altogether, but I'm going to go ahead and use them in my example code.

```js
document.write('Greetings');
```

And notice that "Greetings" shows up on the page. We actually wrote to the web page using JavaScript. Cool! Now I said you could put _any_ string inside the parentheses. I used a string _literal_, but does that mean I could have used a string _variable_? Let's go ahead and create a variable on the line above `document.write`, and use that variable in place of the literal.

```js
let name = 'Davey';
document.write(name);
```

Sure enough. "Davey" shows up on the page. So you can use a variable; you can use a literal; you can use a combination of the two, by using string concatenation. You can do the concatenation right inside the parentheses.

```js
let name = 'Davey';
document.write('Greetings, ' + name);
```

Wonderful! So you can put an _expression_ inside the parentheses. That's totally fine. Let's put some punctuation at the end there.

```js
let name = 'Davey';
document.write('Greetings, ' + name + '!');
```

So I put another string containing only an exclamation point, and that works totally fine.

How about numbers? It's not much fun if you can't put numbers in there. So let's try it.

```js
document.write(4);
```

There we go. "4" is on the page. Now what about an expression involving a number?

```js
document.write(4 + 3);
```

Yep, totally fine. Could I put a set of parentheses inside the parentheses?

```js
document.write((4 + 2) * 3);
```

There we go! "18". Totally works. Yep.

I said it needed to be a string inside the parentheses. Turns out, what's happening is that it's evaluating the expression inside the parentheses to get `18`, and then it's converting the result to a string. All of this is happening behind the scenes, so we don't necessarily need to know that that's what's happening, but it's not bad to know that that's what's happening. For our purposes, it's enough to know that you can in fact put numbers and mathematical expressions inside the parentheses of `document.write()`, and the result will end up on the page.

Let's see what happens if we have `document.write()` on the page more than once.

```js
document.write((4 + 2) * 3);
document.write(17);
```

Oh, great: "1817". One thousand eight hundred seventeen. No, it just wrote the `18` and then immediately afterward wrote the `17`. It didn't put a space between them. It didn't put them on separate lines or anything like that, so they just look smashed together. Huh. What can we do about this?

Well, it turns out you can give `document.write()` a string containing HTML, and that totally works. So see the difference between `document.write('Hello')` and `document.write('<h1>Hello</h1>')`. It prints the second example out as an `h1`. Cool!

Let's try putting our numbers inside paragraph tags.

```js
document.write('<h1>Hello</h1>');
document.write('<p>' + 18 + '</p>');
document.write('<p>' + 17 + '</p>');
```

Now the "18" and "17" are on separate lines, underneath "Hello". Great. Now, I suppose I could have just put `17` inside the same set of quotation marks as the paragraph tags...


```js
document.write('<p>17</p>');
```

...and then we just have the string `'<p>17</p>'`, but I wanted to make the point that even if you had the _number_ `17`, you could still concatenate it with the opening and closing tag strings, and it would work. Now they're not all smashed together. They're all in separate elements on the page, which makes it much more readable. Good to know.

So now we know how to write brand new HTML onto the page. But how do we modify HTML that's _already_ on the page? How do we modify _existing_ elements? You guessed it: That's next time!

Until then, I'm Davey Strus. Haaaappy hacking!
