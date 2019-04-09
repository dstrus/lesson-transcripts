Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

We've dipped our toes into the ocean that is CSS, but our page certainly doesn't match the design yet. Next up, we'll use CSS to set the dimensions of an element. By the end of this video, you'll know how to set the width and the height of an element. Let's dive right in.

Code along with me using the editor on this page, and remember to pause the video as often as you need to.

In our efforts to make this match the final design, let's add a bit of vertical space to the `header`. It's not as tall as I would like right now. To do that, we'll set a height on the header. Add a new declaration to the existing `header` rule in the CSS.

```css
header {
  background: gray;
  color: white;
  height: 400px;
}
```

There is, as you might expect, a `height` property in CSS. You can use a variety of different units for your value, but we're going to keep it simple and stick with **pixels**. How about 400 pixels? `400px`&mdash;no space between the number and `px`. That gives us 400 pixels and, of course, don't forget your semicolon. And there we go. We have a bit more vertical space there. Ideally, I would like it to be centered within that space, but we'll deal with that later.

Now let's take a closer look at the `main` content area of our page. Scroll down to that in the HTML, and remember that `main` encompasses the `h3`, the paragraph, and the `form`. It's hard to tell exactly how much space `main` is taking up without a background color. Let's add a background really quickly.

```css
main {
  background: silver;
}
```

So we'll add a new ruleset for the element `main`, and I'll give it a background... let's say `silver`. There we go. Now I can see that it is taking up the full width and taking up just as much vertical space as it needs. In the original design, the `main` section does _not_ take up the full width, so let's limit its width a bit.

```css
main {
  background: silver;
  width: 400px;
}
```

Predictably enough, there is a `width` property in CSS, and let's again use `400px` as our value. Don't forget your semicolon. And there we go. Now it is not the entire width of the page. All **block** elements take of the full width of their container by default. If you want it to be any narrower than that, you have to set a width, as we've done here.

Once again, I wish the contents of this gray box were centered, and I really wish the gray box itself were centered as well. But we don't yet have the tools to do that. So that's probably a good thing to do next.

Is yours matching mine at this point? Great.

Next time, we will in fact learn how to align elements and the contents of elements&mdash;especially how to center them.

Until then, I'm Davey Strus. Haaaappy hacking!
