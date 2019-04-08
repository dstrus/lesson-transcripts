Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

We're getting ever closer to our final design. In this video, we'll make some adjustments to the spacing inside and around our elements using **padding** and **margin**. Shall we?

Code along with me using the editor on this page, and remember to pause the video as often as you need to.

Some elements have some blank space around them by default. Sometimes it seems like it's not enough space; sometimes it seems like it's a bit much; and sometimes, if we're lucky, it feels about right. In other cases, there's no space around an element be default, and it really feels like there ought to be some. We can tweak this using the **padding** and **margin** properties in CSS.

Padding and margin both refer to empty space around an element, but what's the difference between the two?

![](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/box-model.png)

Padding and margin are part of the **box model**, the model for how elements are laid out on the page.

![](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/box-model-margin.png)

I think of the margin, highlighted here, as space _outside_ an element...

![](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/box-model-padding.png)

...and padding as space _within_ the element, because padding is inside any **border** that might be on the element, and the element's background color is visible through the padding. Margin, on the other hand, is outside the element's border, and the background color is _not_ visible through the margin.

![](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/box-model-border.png)

I've casually mentioned borders twice now. Borders appear between the padding and the margin, and we'll learn more about them later. For now, we want to focus on padding and margin.

So where do we need to make some adjustments? Well, we employed our trick to vertically center the contents of the header, but there's actually quite a bit more space at the top than there is at the bottom. That's because the browser is automatically adding margin to the top and bottom of the `h1`. The bottom margin seems fine. We want some space between the `h1` and the `h2`, but that top margin is just throwing off our efforts to center the content. So let's get rid of it!

The element we're changing is the `h1`, so let's find the ruleset for the `h1`...

```
h1 {
  color: gold;
}
```

...and then what we're changing is the _top_ margin. There are margin properties named `margin-top`, `margin-right`, `margin-bottom`, and `margin-left`. If you're only wanting to change _one_ of those, then you only need the property for that side. In this case: `margin-top`. We're changing it to simply zero.

```
h1 {
  color: gold;
  margin-top: 0;
}
```

Ordinarily, margins take the same kinds of units that `width` and `height` take, which can be pixels (`px`) or a number of other things, but if the value is `0`, then you just need to say `0`, because zero _pixels_ is the same as zero _anything else_. It's just zero.

Notice that "Night of the Salamander" moved up, as did the rest of the contents of the header, and we now have perfectly vertically centered content.

Have you noticed that there's some empty whitespace around the entire thing? Turns out, the `body` itself has a margin by default, and that's stopping our header from going edge-to-edge like we want it to. Let's remove that margin as well. This time, the element we're changing is the `body`, so let's scroll back up to the `body` ruleset, which right now just has `text-align`, and this time we want to give it _no_ margin on _every_ side. We could put `margin-top: 0; margin-right: 0; margin-bottom: 0; margin-left: 0;`. But since we want the margin to be the same on every side, we can simply use the property `margin`.

```
body {
  text-align: center;
  margin: 0;
}
```

`margin: 0;` will give it a margin of `0` on all four sides, and padding works the same way. There's `padding-top`, `-right`, `-bottom`, `-left`, and there's just plain `padding` when you want it to be the same on every side. Now we have our header going edge-to-edge. In fact, the entire page is going edge-to-edge, although that wasn't terribly visible in other places. Now we have the margin we want on the body.

I think we could use some padding in the `main` section of the page. Looking at the `main` box with "Album release party", "We hope to see you October 13", and the form, there's no space at all around the edge, especially at the top and bottom. On the left and right, there is space, because it's centered and we specified the total width. But it could really use some padding all the way around. So let's try to do that. Scroll down to `main`, and let's add a declaration for `padding`. And we want it on all four sides, so we'll just say `padding: `... how about `20px`?

```
main {
  background: silver;
  width: 400px;
  margin: 0 auto;
  padding: 20px;
}
```

Well, that certainly is padded, but it's a little funny looking, isn't it? All of a sudden, there's no space between `header` and `main`, and now there's way too much space above "Album release party". So, "Album release party" is an `h3`. There's no rule for `h3` right now. We've styled the `h1` and `h2`, but not the `h3`. So let's add a rule for `h3`, and let's say `margin-top: 0;`, just like we did for `h1`.

```
h3 {
  margin-top: 0;
}
```

OK, that helps. There's no longer way too much space above the `h3`. But we still don't have any space between the header and `main`, and we really want there to be some. There are several ways we could fix this. One of the most obvious to me is to have some margin above `main`, so let's look at that. Back down in `main`, we already have `margin`. We have `margin: 0 auto;`.

```
main {
  background: silver;
  width: 400px;
  margin: 0 auto;
  padding: 20px;
}
```

We've learned about the properties `margin-top`, `-right`, `-bottom`, and `-left`, and we've learned about the property `margin`, but the way that we've used `margin`, we used it to set the margin on all four sides to a single value. Here we have _two_ values. I told you this was a trick for centering things, but what do the `0` and `auto` actually refer to here? What does it mean when there are two values for `margin?

`margin`, it turns out, can have one, two, three, or four values. When there's only one value, that same margin is applied to all four sides. You can use four values to specify different values for each of the four sides using a single declaration. You specify them in clockwise order: top, right, bottom, and left, always in that order, each separated by a space. And keep in mind that all of this applies to padding as well. So what if you only specify two values? In that case, the first value applies to both the top and the bottom, and the second values applies to both the left and the right. So this declaration that says `margin: 0 auto;` is really saying `0` margin on the top and bottom, and `auto` margin on the left and right. So it turns out, `auto` applied to left and right margin _centers_ an element. It doesn't necessarily center its contents; it centers the element itself. So the `0` refers to top and bottom, and that's where it isn't looking quite right. So what if we change this from `0 auto` to `20px auto`?

```
main {
  ...
  margin: 20px auto;
  padding: 20px;
}
```

Ah ha! There we go. Now have margin on the top, and there is space between `header` and `main`. this is starting to look right. So where else could we use a little more space? Personally, I'd like to see a little more space inside our form inputs. So let's add a rule for `input`. `input` is the name of the element, so we should be able to write a selector `input` and have it apply to both form fields. Let's just give it `8px` of padding all the way around.

```
input {
  padding: 8px;
}
```

Nice. I like it, but that button looks a little silly now, doesn't it? So let's apply some padding to the button as well. Again, our selector can be just plain `button`, and let's give it padding of `8px`.

```
button {
  padding: 8px;
}
```

OK, that's not terrible, but I'd kind of like a little extra padding on the left and right inside that button. `8px` looks good on the top and bottom, but I want a little extra on the left and right. So how about giving `padding` two values, the way that we did `margin`? `8px` on the top and bottom; `24px` on the left and right.

```
button {
  padding: 8px 24px;
}
```

There we go. I like the way that looks.

So we've learned how padding and margin work, and we've applied both to several elements. Is yours looking like mine? Great!

Next time, we're going to look at borders, including how to make rounded borders.

Until then, I'm Davey Strus. Haaaappy hacking!
