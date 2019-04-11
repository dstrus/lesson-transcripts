Hey, everyone. Welcome to Kenzie Academy. This is Davey Strus.

Let's talk about **functions**! Functions give us a great way to organize our code and ultimately serve as the main building blocks of our programs. You can think of them like little factories. They take some raw materials in, they do some work, and then they produce something of value in the end. So we're going to learn how to make functions of our own.

Go ahead and code along with me using the editor on this page, and remember to pause as often as you need to.

There's more than one way to create a function. We're going to learn one of them right now. It's called a **function declaration**, and it has a very specific **syntax**. (There's that word again. We'd better learn what that means before too long.)

You begin a function declaration by writing the word `function`. Simple enough. Now, `function` is a **reserved keyword**, which means we cannot name variables `function`. It means something very special. After the word `function`, we put a space, and then the name that we want to give our function. It's an identifier, just like a variable name. So we can choose anything that follows those rules for how we name identifiers. Let's call ours `timesThree`. Notice I'm using camelCase: Lowercase `t` to start, capital `T` for the word `Three`. Uppercase and lowercase letters are treated differently in JavaScript. We cannot refer to this function later as `timesthree` with two lowercase `t`s. That capital `T` in the middle is part of the name, and it must be there anytime we refer to this function later.

So, the word `function`, a space, the name we want to give the function (the name of the identifier), followed by a set of parentheses. After the parentheses, we'll put another space and a set of curly braces (`{ }`). Curly braces probably aren't a key you're used to if you have done any coding before, but we use them all the time in coding. That is **Shift** + **[**. Square bracket is found right above the apostrophe/quotation mark key. Apply **Shift** to that, and you get a curly brace. So, left curly brace (`{`) to start, and a right curly brace (`}`) to end. And everything in between is considered the _body_ of the functions. That's where we do the actual work.

```
function timesThree() {

}
```

So this is a complete function declaration, but you can also add a little something in between the parentheses. This is where we put **arguments** or **parameters**. Those are the raw materials I referred to earlier. They're the data that comes from _outside_ the function so that we can do the work we need to do _inside_ the function. In this case, our function, as you might guess, is going to multiply things times `3`. We need to know _what_ we're going to multiply times `3`, so we need something from the outside. We need some raw materials. The `3` we'll just build right into our factory here, but we need that other number from the outside. So we want to put something inside the parentheses. We'll just call it `n`.

```js
function timesThree(n) {

}
```

Put the identifier you want there. You don't have to put `let n`&mdash;just `n` will suffice&mdash;and it will create, essentially, a variable called `n`. Now `n` will only exist as long as this function sticks around. It's essentially a **local variable**, meaning this variable only exists inside the body of this function. It does not exist until we hit the opening curly brace, and it goes away as soon as we hit the closing curly brace. But anywhere in between, we can use `n`.

So what is this function meant to do? Well, it multiples `n` times `3`, and that's pretty much all it does.

```js
function timesThree(n) {
  n * 3;
}
```

Groovy, but we need to do something with the result. We don't just want to multiply it times `3` and leave it there. I said these are like factories that take some raw materials and then produce something of value, but this isn't really producing anything. It's doing some work, but we aren't able to do anything with the result. If we want to do something with the result, we need to use another reserved keyword in JavaScript, called `return`.

```js
function timesThree(n) {
  return n * 3;
}
```

If we say `return n * 3`, then we'll actually get that result, and we can do something with it. So this is a complete function now. It multiplies something times `3`. We could put this on two lines inside the body instead of one, if we wanted to.

```js
function timesThree(n) {
  let product = n * 3;
  return product;
}
```

Totally valid. Works just as well. And, interestingly, because we declared `product` inside the body of this function using the word `let`, `product` becomes a local variable&mdash;local to the function `timesThree()`, meaning `product` does not exist until it's been declared, and it goes away as soon as we hit the closing curly brace. `product` is only usable inside the body of this function, because that's where we declared it.

I'm going to keep this as a one-liner for right now, but it's perfectly fine to do it the other way.

```js
function timesThree(n) {
  return n * 3;
}
```

So that's how we _create_ a function, but how do we _use_ one? Here's a dirty little secret: We've already used one. We used one called `document.write()`. The name of the function is `write`, we put some opening and closing parentheses right afterward, and we put something in between. So we're going to do the same thing to call `timesThree()`&mdash;to call, or **invoke**, the function.

```js
timesThree();
```

So we'll write the name of the function, `timesThree`, and then a set of parentheses (don't forget your semicolon), and then between the parentheses we put the value that we want to be assigned to `n`. Out here where we invoke the function, it doesn't matter that we called the argument `n` up where we declared the function. `n` is simply the name we use to refer to this value _inside_ the function, inside our factory. Out here, in the raw materials world, whatever we put inside the parentheses will get assigned to `n`. It could be a literal, an expression, a variable. It doesn't matter. Whatever it is will be assigned to `n` and will be multiplied times `3`.

So let's give it shot. Let's start simple, using a number literal.

```js
timesThree(4);
```

This seems like it ought to work, but of course we can't see the result. The result isn't on the page anywhere, so let's save the result to a variable...

```js
let product = timesThree(4);
```

...and then let's write `product` to the page.

```js
let product = timesThree(4);
document.write(product);
```

Look at that: `12`. Totally worked. Could it have been an expression?

```js
let product = timesThree(4 + 3);
document.write(product);
```

You bet! You can put an expression inside parentheses. And now it's `21`. Could it have been a variable? Sure, why not!

```js
let multiplicand =  6
let product = timesThree(multiplicand);
document.write(product);
```

And we get `18`. Great!

Looks like I forgot my semicolon after the `6` here. JavaScript didn't complain. They are optional, but since I'm using semicolons, I should put one there.

```js
function timesThree(n) {
  return n * 3;
}

let multiplicand =  6;
let product = timesThree(multiplicand);
document.write(product);
```

Notice I did not put one after the function declaration. This is one of the exceptions. You do _not_ put a semicolon at the end of a function declaration. It does not belong there.

So what we've done here to use the function is called **invoking** the function: **Function invocation**. And I put my function invocation on the right side of an assignment&mdash;the right side of an equals sign. Totally valid. Function invocations are expressions, so you can assign their values to variables. And the _value_ of the function invocation is going to be whatever was _returned_. Some functions don't return anything, in which case it's going to evaluate to `undefined`, which is a fancy way of saying _nothing_, basically. But this one does return something, so it is just as though I had written `18` here.

```js
let product = 18;
```

Whatever value gets returned by the function is effectively what's on the right side of that equals sign. So as you might guess, you can also invoke `timesThree` inside the parentheses of `document.write()`. Let's try that.

Let's put our product here inside a paragraph, just to keep it separate.

```js
let multiplicand =  6;
let product = timesThree(multiplicand);
document.write('<p>' + product + '</p>');
```

Then let's do it again, and this time we'll say `document.write()` and actually put `timesThree()` inside the parentheses.

```js
document.write(timesThree(9));
```

There we go. And yeah, the second result on the page is `27`. It totally works to just invoke the function right inside a set of parentheses. It evaluates the function invocation, `27`, and it's just as though I had written `27` inside `document.write()`. Got it?

Now what if I had left the function as a two-line function instead of one line? What if I had said...

```js
function timesThree(n) {
  let product = n * 3;
  return product;
}

let multiplicand =  6;
let product = timesThree(multiplicand);
document.write('<p>' + product + '</p>');

document.write(timesThree(9));
```

Do you see a potential problem here? I have `let product` inside the function, and `let product` again outside the function. We've tried this before, and we weren't able to declare the same variable twice, but it's not complaining this time. Just to make sure it is running again, let's change `multiplicand` from `6` to `8`.

```js
function timesThree(n) {
  let product = n * 3;
  return product;
}

let multiplicand =  8;
let product = timesThree(multiplicand);
document.write('<p>' + product + '</p>');

document.write(timesThree(9));
```

And we see that it changes to `24`. So it _does_ still work.

So why is this happening? First of all, the lines inside the function don't actually run until you invoke the function. So the first four lines...

```js
function timesThree(n) {
  let product = n * 3;
  return product;
}
```

...are just declaring the function, not actually executing it. The lines inside...

```js
  let product = n * 3;
  return product;
```

...don't actually run yet. So the first one of these `product` variables it runs into is the one down here:

```js
let product = timesThree(multiplicand);
```

But then it runs the right side of the equals sign first, which invokes `timesThree()`, then it finally runs this line:

```js
  let product = n * 3;
```

And the variable it's declaring here is _local_, you'll recall, to this function&mdash;meaning it did not exist until we got here, and it ceases to exist as soon as we hit the closing curly brace. So _this_ `product` no longer exists once we finish running `timesThree()`, so it's no problem to then take the result and assign it to a brand new variable that happens to have the same name. They are two completely different variables&mdash;one that lives inside the function `timesThree()`, and one that does not. So I can totally say `let product` twice, as long as one of them is inside the function.

This is a phenomenon called **scope**. Scope tells us which variables are available to us at any given point in the program's execution, and it's a fairly complex topic worthy of a deeper dive. So we'll do that next time. For now, we have a basic understanding of functions. Functions are a very big topic, and we have only scratched the surface. But you have to start somewhere, right?

So until next time, I'm Davey Strus. Haaaappy hacking!
