Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

Right now, we have something that looks like this...

![in progress design](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/bard-progress.png)

...and we want it to look like this.

![finished design](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/bard-screenshot.png)

We know that we're going to make it happen with CSS, so now it's time to start doing it. In this video, we'll learn how to target different elements using **selectors**, and how to specify an element's color and background. Ready? Here we go.

My editor is showing the HTML. Yours is showing the CSS, which is empty right now. That's fine. Just follow along with the video for the moment until we're ready to actually start writing CSS.

Now before we start writing CSS, let's get the lay of the land really quickly. Let's look at the header of the page. The header encompasses the `h1`, the `h2`, and the Beasley image. That's what we're going to focus on styling right now.

So let's start with changing the background of the entire `header`.

Code along with me using the editor on this page, and remember to pause the video as often as you need to.

So a CSS ruleset begins with a selector, and the selector tells it which elements on the page this ruleset applies to. And the simplest possible selector is one that targets elements simply by the element type&mdash;in this case, `header`.

```css
header
```

And what that selector means is that this ruleset will apply to any and every header on this page. We only have one, but if we had more than one, it would apply to all of them. So that's the selector.

The rest or the CSS rule, or ruleset, consists of the declaration block, which we know belongs inside a set of curly braces. As soon as you type the opening curly brace (`{`), CodePen will automatically put the closing curly brace there for you. As soon as that happens, it will put the cursor in between the two, and we can just hit the enter (or return) key, and it will go onto the next line, and it will indent that line. Similar to the way we indented elements that are nested inside other elements, we want to indent the declarations inside a CSS ruleset. It makes it a lot easier to find that closing curly brace, so we know for sure where a CSS ruleset ends.

```css
header {

}
```

Now that we're inside the declaration block, we need a declaration, consisting of a property name and a value. The property we want to change here is the background color. You saw in the slides earlier that `background-color` is a valid CSS property, but there's also one called just plain `background`. That works too, and it's in fact a lot more flexible than `background-color`, so let's use it.

```css
header {
  background
}
```

So we have the property name `background`, then we put a colon, a space, and then the value that we want. And the value can be any color. There are a whole bunch of named colors in CSS. We'll look at a list of them in a minute. Let's for right now just pick something like `gray`. How about that?

```css
header {
  background: gray
}
```

Look&mdash;it changes! Now we know we need to put a semicolon at the end of that.

```css
header {
  background: gray;
}
```

The gray background did show up on the page before we put the semicolon there, so the missing semicolon hadn't broken anything yet, but it would have soon, so we may as well go ahead and put it there before we forget.

The other CSS property that you saw in my examples earlier was simply `color`, which changes the color of the text inside an element. So what happens if we change the color inside the `header`?

Let's add another line to our ruleset and add another declaration. Type `color` (the property we want to change), colon... and then how about we change it to white? White on gray.

```css
header {
  background: gray;
  color: white;
}
```

Beautiful. Look at that. Notice that changing the color of the `header` changed the colors of the `h1` and the `h2`, because they are inside the `header`. Now if we had specific rules for `h1` and `h2`, those would override the color of the header, because that would be more specific. So we can try that too.

So what colors can we refer to by name in CSS? [Here's a list on the CSS-Tricks web site](https://css-tricks.com/snippets/css/named-colors-and-hex-equivalents/). And there are a whole bunch of colors we can refer to by name. From `AliceBlue` and `BlanchedAlmond` to `CornflowerBlue` and `DarkOliveGreen`, as well as every color that you can probably name off the top of your head. You have all kinds of choices, so pick a couple that seem nice to you, and we'll use those to style the `h1` and `h2`.

```css
h1 {
  color: gold;
}
```

We need another ruleset&mdash;put a blank line in between&mdash;and we need a selector: `h1`. That will target every `h1` on the page. Then we have our declaration block inside curly braces. Then we specify `color` as the property, colon, and then the value. How about `gold`? Don't forget your semicolon. Look at that&mdash;lovely.

So then we want to also style the `h2`.

```css
h2 {
  color: beige;
}
```

So the selector is just `h2`, we have our curly braces, the property name `color`, and the actual color value... how about `beige`? Who doesn't love beige? And then the semicolon. Now that's a subtle distinction from white, but it is noticeably different.

Great, so now the `h1` and `h2` have colors of their own, and the `color: white` declaration under `header` isn't actually doing anything. If we were to add some other text inside the header, but outside the `h1` and `h2`, then that text would be white. But that's not something we actually want to do.

So does yours look like mine&mdash;except maybe you used different colors than I did? Great.

Next time, we'll learn how to set the dimensions of an element.

Until then, I'm Davey Strus. Haaaapy hacking!
