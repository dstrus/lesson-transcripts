Hey, everyone. Welcome to Kenzie Academy. This is Davey Strus.

Now that we have our JavaScript console open, with **Option** + **Command** + **J** or **Shift** + **Ctrl** + **J**, it's time to start actually trying out some JavaScript. So let's do it!

Here's about the simplest JavaScript I can think of. Let's just type `4`, and hit **Enter**.

```js
4
```

And it returns... `4`. That's what happens when it **evaluates** this line of JavaScript. The answer is `4`. OK, seems intuitive enough. Think we can do actual arithmetic? Let's try it.

```js
4 + 3
```

And it gives us `7`. Yep, totally valid line of JavaScript.

By the way, I put spaces around the `+` sign for the sake of readability. The spaces are optional.

How about multiplication?

```js
4 * 3
```

Notice that is an asterisk (`*`), not an `x`, for _times_. And we get `12`. Division? That would be a forward slash (`/`). So how about...

```js
9 / 3
```

And we get `3`. Sure enough, the basic arithmetic operations work.

When we write something like `4`, all by itself, that's just a number. It's what we call a number **literal**. That's _literal_ as opposed to _variable_. We'll talk about variables in a bit. A number literal is just raw, numerical data.

```js
4 + 3
```

Here we have two number literals with a little something in between. That little something is an **operator**. `+`, `-`, `*` for multiplication, `/` for division&mdash;they're all operators. And there are many others. This whole thing, `4 + 3`, is an **expression**. We'll talk more about expressions when we have something to compare them to, but an expression is something that can be evaluated to give us some value, some _answer_. The expression `4 + 3` evaluates to `7`.

Let's try a more interesting expression. How about...

```js
4 + 2 * 3
```

Now we have three number literals and two operators. What do you think the answer is going to be? Let's hit enter... and it's `10`. Were you expecting `18`? After all, `4 + 2` is `6`, and `6 * 3` is `18`. Ah yes, but `4` plus the result of `2 * 3` (which is `6`) is `10`. So we have an issue with the order of operations, and it works the same way in JavaScript that it works in, well... _math_.

You may remember a mnemonic device from school:

> **P**lease **E**xcuse **M**y **D**ear **A**unt **S**ally.

Or maybe the slightly less common:

>**Please** **E**xonerate **M**y **D**astardly **A**ardvark **S**tuart.

But whichever one you remember, it's a useful mnemonic device for:

> **P**arentheses, **E**xponents, **M**ultiplication, **D**ivision, **A**ddition, **S**ubtraction

Those things are evaluated in that order, so multiplication comes _before_ addition. If we want to get `18`, however, we can use parentheses. We can use them in JavaScript just like we would in regular old math.

```js
(4 + 2) * 3
```

`(4 + 2) * 3` is `18`. `(4 + 2)` is almost treated as a separate expression inside the parentheses. That's evaluated, and then the result is multiplied times `3` to get `18`.

There are a lot more operations in JavaScript than just these, but as long as you're dealing with basic arithmetic, you can follow the same rules that you would when doing math outside of JavaScript. Just remember the old mnemonic device:

> **P**lease **E**radicate **M**y **D**eadly **A**ntlion **S**election.

So now we know about number literals, operators, and expressions, and we're familiar with the basic order or operations. Next, we need to learn about variables.

Until then, I'm Davey Strus. Haaaappy hacking!
