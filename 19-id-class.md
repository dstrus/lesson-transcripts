Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

Remember selectors? They're the first part of a ruleset, outside the curly braces, and they're what determines which elements on a page a particular ruleset applies to. So far, we've only used one form of selector. We've selected elements by which _type_ of element they are&mdash;`h1`, `p`, `footer`, etc. But sometimes we need to select elements by something other than just the element type&mdash;if, for example, we want one `h1` to be a different color from all the other `h1`s. And sometimes we want a single ruleset to apply to elements of different types. Maybe we want all the `h2`s and some of the `h3`s to have a border.

We can achieve all of these things using IDs and classes.

If you flip over to the HTML, you'll see that I've made a couple of changes.

```html
<h1 id="album">Night of the Salamander</h1>
```

First, the `h1` at the top of the page now has an `id` attribute with a value of `album`. This, as you may have guessed, is an ID. IDs are used to uniquely identify a single element on a page, differentiating it not only from elements of other types, but also from all other elements of the same type. Any given value for `id` should only be used once per page. Using an ID here lets me target this `h1` separately from all other `h1`s, in case I want to style it differently.

I've also added two new elements to the page. A second `h1` and a paragraph underneath it.

```html
<h1 class="dark">Pre-order now!</h1>
<p class="dark">The cool kids will all be there</p>
```

Both of these elements have a `class` attribute with the value `dark`. Where IDs are used to _identify_ elements, classes are used to, well, _classify_ elements. These elements have something in common, despite being of different types, and giving them a `class` allows me to target both of them using a single ruleset in CSS.

So now that we've seen IDs and classes the HTML, let's learn how to build selectors that target elements by their IDs and classes.

```html
<h1 id="album">Night of the Salamander</h1>
```

Here's that `h1` from the top of the page. We already have a CSS rule that styles it, don't we?

```css
h1 {
  color: gold;
  margin-top: 0;
  font-size: 40px;
  font-family: Oswald, sans-serif;
}
```

Sure we do. And which part of this rule is the selector? `h1`, right? That's how we select elements by their type. The selector is simply the element type. But this selector affects the other `h1` on the page too, doesn't it? What if we didn't want that? What if we wanted, say, a 3-pixel double border on the bottom of just this first `h1`? How would we target this `h1` without targeting the other one? We would use its ID.

```css
#album {
  border-bottom: 3px double;
}
```

The selector to target an element by its ID is `#` (hash), followed by the ID you're looking for. Notice there's no space between the `#` and the ID. So `#album` is a perfectly good selector, and it will work on the `h1` we see here. It won't touch the other `h1` though. Let's actually add this rule to our CSS. Flip over to the CSS tab and scroll to the bottom. We'll add a new rule.

```css
#album {
  border-bottom: 3px double;
}
```

Our selector will be `#album`. To put a border on only the bottom of the element, we'll use the property `border-bottom` instead of just `border`. Say `3px double`. We'll leave the color out, because then it will just use the color of the element itself&mdash;gold&mdash;which is perfectly fine.

![h1 border](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/h1-border.png)

Great! We see that the first `h1` has that bottom border, but the other `h1` does not. Perfect! So that's how we target an element by its ID.

Now suppose I want a single rule to apply to that second `h1` and the following paragraph.

```html
<h1 class="dark">Pre-order now!</h1>
<p class="dark">The cool kids will all be there</p>
```

The two elements share a class, so we'll use a selector that targets them by class. Where you use a `#` (hash) to target elements by ID, you use a `.` (dot) to target them by class. The selector `.dark` says that this rule applies to all elements with a class of dark. That suits us nicely. So let's add another new CSS rule with the selector `.dark`.

```css
.dark {
}
```

And let's get rid of any margin on those elements&mdash;`margin: 0`, right?

```css
.dark {
  margin: 0;
}
```

And the reason I chose the class name `dark` is because I want to make sure they're a nice, dark color. Yellow doesn't look all that good against gray. So how about a lovely dark blue, like `51` for red, `51` for green, and `100` for blue?

```css
.dark {
  margin: 0;
  color: rgb(51,51,100);
}
```

Beautiful. Don't forget your closing curly brace. So now we know how to write a selector that targets elements by ID&mdash;`#` followed by the ID&mdash;and by class&mdash;`.` followed by the class. Excellent!

This is looking pretty good. I think we're ready to call it a day.

All right, you've done it! You've made your first web page using HTML and CSS. Go ahead and take a bow. Thanks for coming on this quest with me, folks. I had fun, and I hope you did too. We hope this is only the first step in your journey with Kenzie Academy. Be sure to get in touch with the Admissions team to learn more about Kenzie's full slate of programs.

This has been Davey Strus, and until next time... happy hacking!
