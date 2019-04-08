Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

We've changed some colors, and we've set the dimensions of a couple of elements, but our journey is far from over. It's time to talk about **alignment**.

I don't mean alignment with the forces of good or evil, but rather the way things line up on the page. In particular, we're interested in centering things, and there's more to it than you might think.

We'll also briefly dip back into HTML to learn about everyone's favorite element: `div`.

Ready to go?

Code along with me using the editor on this page, and remember to pause the video as often as you need to.

Let's begin our alignment quest by trying to center all the text on the page. Looking at the original design, all of the text is, in fact, centered. Let's start with the `header`. There a CSS property called `text-align`. (Notice that anytime there's a CSS property with more than one word, we separate those words with a hyphen.) `text-align` can take values like `left`, which is the default; `right`; `justify`, which aligns left and right like a newspaper, but none of the elements in our header go onto multiple lines, so we can't really see what that does; and `text-align` can take the value `center`.

```
header {
  background: gray;
  color: white;
  height: 400px;
  text-align: center;
}
```


And, lo and behold, that does what we want&mdash;at least from the perspective of left and right. It even centers our image. Images are treated like text, as far as `text-align` is concerned.

Not bad, but since we want to center all the text on the page, not just within the `header`, maybe there's a way that we could apply this rule to every element at once instead of going through element by element. Well, it turns out that although CodePen hides it from us, all of these elements are inside an element called `body`, so we can target the `body` element, apply rules to it, and it should apply to every element on the page.

So I'm going to add a rule above `header`&mdash;it doesn't really matter, but I like to put it at the top&mdash;and my selector is going to simply say `body`. This is going to target the `body` element, which again is hidden from us in CodePen, but it's there, and everything else is inside it. So, don't forget your curly braces, and now let's say `text-align: center;`.

```
body {
  text-align: center;
}
```

Notice the text inside `main` is now centered, and the text inside `footer` is centered. We could even take `text-align: center;` out of the `header`, and the `header` would remain centered.

```
header {
  background: gray;
  color: white;
  height: 400px;
}
```

Again, this is only aligning things left-to-right. You'll notice the `header` is not centered vertically. And although the text within `main` is centered, `main` itself is not centered on the page. So `text-align: center;` gets us a lot of the way there, but there are several ways to center elements, and we're going to have to use at least three of them. One down, two to go.

It's very common to want to center a box like `main` on the page, and we have a trick specifically for that scenario. We will add a rule to the `main` element. The property is going to be `margin`, and the value is going to be `0 auto`.

```
main {
  background: silver;
  width: 400px;
  margin: 0 auto;
}
```

And, lo and behold, `main` is centered on the page. We haven't learned about the `margin` property before. We'll get to that a bit later. For now, all you need to know is that the value `0 auto` will center elements left-to-right on the page. It's an essential thing to know how to do.

So use `text-align: center;` when you want to center the text within an element, and use `margin: 0 auto;` when you want to center some sort of box on the page, left-to-right.

Finally, we want to center the contents of the `header` vertically. Let's scroll to the top of our CSS and have a look at the rules for `header`. Verical alignment in CSS has been a shockingly difficult problem to solve over the years. Thankfully, in recent years, a solution has presented itself that works very reliably and is not difficult to do. So that's what we're going to do today.

There's a very powerful layout system in CSS called **flexbox**. We don't need to fully understand flexbox right now, but it would sure be nice to borrow it for the purpose of centering things vertically, because it gives us by far the easiest and most reliable means of doing so.

Before we add the CSS for this trick, we actually need to make a small tweak to our HTML. Inside the `header`, we need all three of these things&mdash;`h1`, `h2`, and `img`&mdash;to be inside another element, so I'm going to put an element inside the `header` called a `div`. A `div` is just a generic **block** element. It doesn't _mean_ anything. It's just a container that we sometimes need to target with CSS. So I'm going to put an opening `<div>` tag above the `h1`, and then a closing `</div>` tag right before the closing `</header>` tag. And I'm going to go ahead and indent the `h1`, the `h2`, and the `img` another level so that it's obvious that they're inside the `div`.

```
<header>
  <div>
    <h1>Night of the Salamander</h1>

    <h2>The new release from Beasley the Bard</h2>

    <img src="...beasley.png" alt="Beasley the Bard">
  </div>
</header>
```

Again, the `div` doesn't really mean anything. It's just necessary to make our CSS rule work. So here's the CSS for vertical alignment. This goes inside the `header` rule. First, we need to tell it to use flexbox within the header. For that, we use the `display` property. The `display` property, by default, is either `block` or `inline`, depending of what type of element it is (`block` in this case). But we want to set it to `flex`.

```
header {
  background: gray;
  color: white;
  height: 400px;
  display: flex;
}
```

This, quite simply, turns on flexbox for the header. Now that actually un-centers things, so to re-center them, we need to say `justify-content: center;`.

```
header {
  ...
  display: flex;
  justify-content: center;
}
```

There we go. But we're here to align things vertically. And for that, we use the property `align-items`, and once again give it the value `center`.

```
header {
  ...
  display: flex;
  justify-content: center;
  align-items: center;
}
```

In flexbox, `justify-content` aligns things horizontally, and the `align-items` property aligns things vertically. And now we have something vertically centered on the page&mdash;something that until flexbox was a huge pain in the neck to achieve.

Now you may be thinking, "That actually doesn't look perfectly centered vertically." You're rignt. That's because of some margin, and we're going to look at how to adjust margin very shortly. But for now, is yours matching mine? If so, you're in great shape.

Next time, we will learn about padding and margin, which help us really tighten up the spacing of things on our page.

Until then, I'm Davey Strus. Haaaappy hacking!
