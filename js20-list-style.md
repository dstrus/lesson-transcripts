Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

Well, our behavior is finished for this page, so wer're done with the JavaScript. So we're going to spend some time on the CSS to make that list look a little bit better.

Right now, the list items are centered, which, with the bullets on the left, looks a little funny. Why are they centered? Because at the very top, everything is centered; the `body` itself is centered. So that affects everything.

So let's add a new rule, and we'll target each and every list item. So our selector will simply be `li`.

```css
li {

}
```

Now let's add some properties and values, starting with `text-align: left;`.

```css
li {
  text-align: left;
}
```

There we go. That looks better, doesn't it? Do we event want the bullets though? What if we didn't? There's a property called `list-style` that lets us change the bullets. The default value is `disc`. That's what we see now, but it can also be things like `circle`, which does a circle that isn't filled in; or square; or a surprising number of others. One of the options, however, is `none`. I'm going to go with `none` for right now.

```css
li {
  text-align: left;
  list-style: none;
}
```

So why bother using a list with list items in the first place? Well, because that's what it is. It _is_ a list with list items. We just want it to display a little differently. So I like using these elements and then just overriding the style.

Very good, now how about we give each list item a background? Let's make it `white`.

```css
li {
  text-align: left;
  list-style: none;
  background: white;
}
```

Excellent. Now it could use a little space around it. Let's add some padding. How about `8px` on every side?

```css
li {
  text-align: left;
  list-style: none;
  background: white;
  padding: 8px;
}
```

Good, I like that better. Now what if we had a second one? Let's add a second attendee here. Hmm. I wish there were a little more differentiating each one from the one above it. Why don't we add a border in between. Let's achieve that by adding a border to the _top_ of each `li`. So `border-top` is the property, so we'll give it a `1px solid` border... how about a nice, light gray? How about `238,238,238`?

```css
li {
  text-align: left;
  list-style: none;
  background: white;
  padding: 8px;
  border-top: 1px solid rgb(238,238,238);
}
```

This isn't the first time I've done it, so you may have noticed that if the red, green, and blue values are all the same, you're always going to get a shade of gray. The closer that number is to `255`, the closer it's going to be to white&mdash;in other words, the lighter the gray.

There. I think our list items look pretty good, but it looks like they're supposed to be centered within that gray box, but they're not, are they? They're quite a bit closer to the right edge than the left. That's because there's some left padding on the actual list. We've style the list items; now let's style the list itself.

We could put `ul` as the selector and target all unordered lists on the page&mdash;after all it is the only one&mdash;but since it has an ID, why don't we target it by ID? So we'll put `#attendees`.

```css
#attendees {

}
```

That's the same selector we used to grab the list with `querySelector()` in JavaScript. We'll use it for our CSS rule as well. And let's get rid of the padding.

```css
#attendees {
  padding: 0;
}
```

Whenever the value is `0`, you don't need a unit. You don't need to say `0px`. Zero is zero. And how about a border around the whole thing&mdash;around the entire list? We have a border at the top of each list item, but how about a border around the whole list? So I'll say `border` instead of `border-top`, because it's on all four sides, but I'll use the same value.

```css
#attendees {
  padding: 0;
  border: 1px solid rgb(238,238,238);
}
```

There's. That's pretty subtle, but it's there. And that's looking pretty good. There's a little more we could do to fancy it up, but we're going to need to learn some new tricks in order to do those, so that's enough for this time.

Next time, we'll learn a new trick in CSS called **pseudo-classes**. Until then, I'm Davey Strus. Haaaappy hacking!
