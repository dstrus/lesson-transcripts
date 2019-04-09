Hey, everyone. Welcome to Kenzie Academy. This is Davey Strus.

With some newly added borders, we grow ever closer to our finished product. In this video, we'll learn how to set the font size of an element. It's pretty straightforward. We'll just make a few adjustments here and there. Let's begin!

Code along with me using the editor on this page, and remember to pause the video as often as you need to.

Right now, everything is shown at whatever font size the browsers displays by default for a particular element, and really, it all looks pretty fine. I'd just like to make a few adjustments.

We'll start with the `h1`. So go to the rule for the `h1`, and we'll add a new declaration for the property `font-size`. As you might expect, we can use the same units that we've used for width, padding, border, and so on, and we'll stick with pixels (`px`) for this one. So I'm going to make the font size for all `h1`s on the page `40px;`.

```css
h1 {
  color: gold;
  margin-top: 0;
  font-size: 40px;
}
```

There we go. It got a little bigger. What else? How about inputs? Let's change the font size for `input`. I'll change it to `12px`.

```css
input {
  padding: 8px;
  border: 1px solid gray;
  font-size: 12px;
}
```

There. That, too, got a little bigger. And I think the button should match the input, so let's add `font-size: 12px;` to our `button` ruleset as well.

```css
button {
  padding: 8px 24px;
  border: 1px solid gray;
  font-size: 12px;
}
```

One more change. Let's make the `footer` font `12px`. Right now, we don't have a rule for the footer, so we'll have to add one. Add a new ruleset with the selector `footer`, curly braces, and our declarations. We just have one: `font-size: 12px;`.

```css
footer {
  font-size: 12px;
}
```

In this case, it gets a little smaller. Great! I'm pretty happy with those sizes. Does yours look like mine? Wonderful!

Next time, we'll add a hero image to the top of our page. Ooh, _hero image_. That sounds exciting. Yeah, it is. So that's next time.

Until then, I'm Davey Strus. Haaaappy hacking!
