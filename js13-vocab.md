Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

We've been throwing around some pretty fancy words, and at times, we've been at a loss, because we just didn't know the lingo to describe the situation we were in. Let's fix some of that. Let's learn some vocabulary.

We'll start with **syntax**. There's a good word! You'll hear it thrown around quite a bit in the context of programming, but what does it mean?

All languages have syntax&mdash;even languages like English. In the case of spoken and written languages like English, syntax refers to the rules for how words and phrases should be arranged to form sentences. Syntax makes the difference between random assortments of words and sentences that actually make sense.

The same applies to programming languages like JavaScript. There are rules for the order in which things must appear&mdash;what goes where, to form lines of code that the computer can actually understand. The computer has to be able to parse the code, just as we parse words and phrases to make sense of them.

> The conductor enjoyed very hot coffee.

There's a perfectly good English sentence. Our brain parses this very quickly and finds that it makes sense. You've probably forgotten how to diagram sentences, but your brain is basically doing the same work&mdash;recognizing a noun here, an adjective there, and so on.

> Very conductor coffee the enjoyed hot.

Right away, we encounter a syntax error. "Very conductor." Those words don't make sense in that order.

Very conductor. Much coffee. Wow.

```js
let salePrice = 1.99;
```

Similarly, JavaScript sees a line of code like this and knows just what to do with it. The thing following the word `let` must be an identifier. Yep, `salePrice` is a valid identifier. Ah, an equals sign followed by a number. "Very good, your excellency. I'll get right on that."

```js
1.99 let salePrice =;
```

This is how Yoda might write a line of code. Unfortunately, JavaScript is pretty strict when it comes to syntax. You have to obey the rules. Sorry, Yoda.

So that's **syntax**. Get it? Good.

Let's talk about **identifiers**. I've thrown that word around quite a bit. Identifiers are the names we assign to things&mdash;variable names, function names. Those are identifiers. You'll see that word show up in error messages sometimes. Try to declare the same variable twice, and you'll see a syntax error: `Identifier has already been taken`.

So those are **identifiers**.

Let's talk about **keywords**. Keywords are words that have a special meaning in JavaScript and are thus unavailable for us to use as identifiers. We can't use them as variable names or function names, because they already mean something else. For example, `function` is a reserved keyword. We can't use `function` as the name of a variable or function, because JavaScript already has big plans for that word. Another example: `return`. That word should only turn up when you're returning a value from a function. You can't use `return` as a variable name or a function name.

There are a bunch of reserved keywords in JavaScript. Some of them actually have special meaning in the language, and others are just words that the languages designers once _thought_ would _one day_ have a special meaning, and now we're just sort of stuck with them. Eh, that's how it goes.

You can find a [list of all the reserved keywords](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Keywords) on the [Mozilla Developer Network](https://developer.mozilla.org/) site, aka MDN, which you can find at `developer.mozilla.org`. MDN happens to be a fantastic resource for learning more about HTML, CSS, and JavaScript, so definitely check it out.

You don't need to memorize all these keywords right now. You'll learn more of them as you get to know the language better, and if you try to use one inappropriately, you'll be greeted with an error message.

Moving on to **declaration**. We've used this word a few times, in the context of both variables and functions. We _declare_ a variable or function when we bring it into existance. We can declare variables with the word `let` followed by an identifier. We can declare functions with the word `function` followed by an identifier, some parentheses, and curly braces. These are both forms of declaration.

```js
function doSomething() { }
```

Before this line, `doSomething` didn't mean anything in JavaScript, but now I've declared it.

So what is **assignment**? That's what we've been doing with equals signs: _assigning_ a value to a variable. Sometimes we perform declaration and assignment on a single line. Nothing wrong with that. And the first time you assign a value to a variable, that's called **initialization**&mdash;assigning a variable's value for the first time.

OK, feel better? Has your mind been expanded? Very good. Armed with our new vocabulary, let's venture onward toward **events** in JavaScript.

That's next time. Until then, I'm Davey Strus. Haaaappy hacking!
