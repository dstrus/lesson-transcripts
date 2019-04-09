Hey, everyone. Welcome to Kenzie Academy. This is Davey Strus.

We're getting mighty close now. In fact, we could probably ship it like this, and it would be perfectly fine. But I'd like to tweak just a few more things.

For the most part, we're going to be using tricks we already know, but we will learn one new thing, and that's **font-weight**. Let's get started.

Code along with me using the editor on this page, and remember to pause the video as often as you need to.

So I would like the `h2` to actually not be bold. It is bold by default, but I want to change that. So let's look for our `h2` rule, and let's change it.

```css
h2 {
  color: beige;
  font-weight: normal;
}
```

`font-weight`, and I'm going to say `normal`. As you might expect, you can also say `bold`, but it's already bold. I want to make it normal. Then we can emphasize "Beasley the Bard". Go to our HTML and actually wrap that in a `strong` element.

```html
  <h2>The new release from <strong>Beasley the Bard</strong></h2>
```

Now we're talking. I like it. What else could we do a little differently?

Well, that "RSVP" button looks an awful lot like the inputs. It doesn't look quite the same. The color of the text is different, and it's centered, but it's a little too close for my taste. So let's make the button stand out a bit.

Scroll down to your ruleset for `button`, and let's add a background color. Let's say `forestgreen`.

```css
button {
  padding: 8px 24px;
  border: 1px solid gray;
  font-size: 12px;
  background-color: forestgreen;
}
```

Yeah, I like that, but black on forestgreen doesn't look great. Let's make the foreground color white.

```css
button {
  ...
  background-color: forestgreen;
  color: white;
}
```

White on green. Yeah, I like it.

Hmm. How about that footer? I wish the footer weren't quite so dark. It matches all the other text on the page, and really it should be de-emphasized a little bit. So let's change it. Let's make its color `gray`.

```css
footer {
  font-size: 12px;
  color: gray;
}
```

There we go. Gray on white versus black on white. It's not as prominent anymore. And you know what? I think we're getting really, really close to that original design.

But why stop there? I think I'd like to add a little bit to that original design. And you know what? There are a couple of tricks we haven't used yet that are pretty important. So next time, we'll take a look at `id` and `class` selectors in CSS.

Until then, I'm Davey Strus. Haaaappy hacking!
