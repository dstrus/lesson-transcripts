Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

What time is it? It's scope time! Scope refers to which variables are available at any point in the code. We started looking at this in the last video, but we need to explore the topic a little further.

So far, we've established that variables declared inside a function are unavailable outside that function. That is, functions create a new **scope**.

Let's what through what this code does.

```js
function doSomething() {
  let lunch = 'spaghetti';
  document.write('<h1>Inside: ' + lunch + '</h1>');
}

let breakfast = 'cereal';
doSomething();

document.write('<h1>Outside: ' + breakfast + '</h1>');
```

The first four lines declare the function `doSomething()`. Nothing between the curly braces actually runs at this point. Those lines just become part of the function, to be run whenever the function is invoked with a set of parentheses.

Next, we declare a variable called `breakfast` and set its value to the string `'cereal'`.

Then we invoke the function `doSomething()`. At that point, execution actually jumps to between the curly braces. Now we're here:

```js
  let lunch = 'spaghetti';
  document.write('<h1>Inside: ' + lunch + '</h1>');
```

We then declare a variable inside the function called `lunch` and set its value to `'spaghetti'`. Then we write an `h1` to the page containing the text "Inside: " and whatever value `lunch` holds&mdash;"spaghetti" in this case. Then, having reached the end of the function, execution returns to just after we invoked the function.

We then write another `h1` to the page with the text "Outside: " and whatever is in the variable `breakfast`&mdash;namely "cereal".

In this example, we have two scopes. Everything in JavaScript that isn't inside some other scope, like the scope of a function, is said to be in the **global** scope. Aside from the global scope, we have the scope for the `doSomething()` function. So which variables are part of each scope?

The global scope contains the variable `breakfast`. It also contains the function `doSomething`. Yes, the function itself is effectively a variable that happens to contain a function instead of a number or a string. So that's everything in the global scope.

The scope for the function `doSomething()`&mdash;that is, the scope internal to that function&mdash;contains the variable `lunch`. That makes `lunch` **local** to that function.

So where are each of these variables available? Is `breakfast` available inside `doSomething()`? Let's try putting it in that "Inside" `h1` in place of `lunch`.

```js
function doSomething() {
  let lunch = 'spaghetti';
  document.write('<h1>Inside: ' + breakfast + '</h1>');
}
```

Sure enough. It worked. Surprised? As it turns out, variables in the global scope are available everywhere. The variable `breakfast` is declared before we invoke the `doSomething()` function, so it does exist at that point, and it actually doesn't go out of scope when we enter the function.

What if we have another variable in the global scope, but we don't declare it until after we invoke the function? Add a new variable `salad` and try using it in the `h1` in the function.

```js
function doSomething() {
  let lunch = 'spaghetti';
  document.write('<h1>Inside: ' + dinner + '</h1>');
}

let breakfast = 'cereal';
doSomething();

let dinner = 'salad';

document.write('<h1>Outside: ' + breakfast + '</h1>');
```

Uh-oh! Everything went away, so I think it's safe to say that didn't work. Remember your old friend the JavaScript console? Well, if you pop that open, you'll see an error message: "Uncaught ReferenceError: dinner is not defined". Indeed, `dinner` is _not_ defined at that point in the code. But `dinner` is in the global scope, so it should be available everywhere, right? Well, sure... once it exists. But the line where we invoke `doSomething()` comes before the line where we bring `dinner` into existance.

Remember when we walked through line-by-line. The first thing that happens is we declare the function. Then we declare and initialize the variable `breakfast`. Then we run `doSomething()`. Then we declare and assign `lunch`, and then we write this `h1`. So when that happens, we have not yet run the line where we create `dinner`, right? So it doesn't work. It's not an issue of global versus local scope. The variable just doesn't exist yet. So let's change the function back so that it writes `lunch`.

```js
function doSomething() {
  let lunch = 'spaghetti';
  document.write('<h1>Inside: ' + lunch + '</h1>');
}

let breakfast = 'cereal';
doSomething();

let dinner = 'salad';

document.write('<h1>Outside: ' + breakfast + '</h1>');
```

OK, that's better. So global variables are available _everywhere_, as soon as they're available _anywhere_. `dinner` just wasn't available _anywhere_ yet when we tried to use it.

So what about `lunch`? `lunch` is local to the function `doSomething()`, so we don't expect it to exist outside the function. Let's confirm that. Let's make the "Outside" `h1` also try to print `lunch`.

```js
document.write('<h1>Outside: ' + lunch + '</h1>');
```

Well, it prints inside the function, but not outside. Just as we suspected. If you pop open the JavaScript console, you'll see another error: "Uncaught ReferenceError: lunch is not defined". Because, again, `lunch` is not defined at that point in the code. Although the line that declares and initializes the variable `lunch` _has_ executed by the time we try to write it to the page that second time, that variable went out of scope before we got there. It ceased to be in scope as soon as we hit that curly brace at the end of the function.

Going through line-by-line again, the first thing that happens is we declare the function `doSomething()`. Then we set the variable `breakfast`. Then we execute `doSomething()`. We create the variable `lunch` (`lunch` is in scope now). We write that first `h1`. Then we hit the end of that function, and `lunch` ceases to exist. Control returns to after the function invocation. We create `dinner`. Then we try to write the second `h1`, which contains `lunch`, but `lunch` no longer exists.

Now we have a very basic understand of scope in JavaScript. There's a lot more to it than we've covered. It gets pretty complicated and, frankly, a little strange. But this overview covers what we need to know for now.

Next time, we'll use our newfound understanding of functions to update our Beasley page.

Until then, I'm Davey Strus. Haaaappy hacking!
