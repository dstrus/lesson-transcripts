Hey, folks. Welcome to Kenzie Academy. I'm Davey Strus.

We have a salamander photo in the background of our header now, but it really a HERO IMAGE? Maybe, but our text isn't super readable on top of it. So let's learn some more advanced background image techniques to see if we can fix it. I bet we can.

Along the way, we'll learn to use **linear gradients**&mdash;where one color fades into another&mdash;as background images. We'll also learn how to stack backgrounds on top of each other. And although we've used color before, we're learn how to gain access to 16.7 million colors by mixing our own using red, green, and blue values. But that's not all, folks. We'll also learn how to make colors translucent by adding an **alpha** value alongside the red, green, and blue values.

Whew! Sounds like a lot. It's good stuff though. We can do it!

Code along with me using the editor on this page, and remember to pause the video as often as you need to.

We're messing with the background image of the `header` element, so I'll scroll down to those rules, and it turns out that the `background-image` property can take more than just the URL of an image as its value. It can also take a **linear gradient**. A gradient is when one color fades into another. For the moment, I'm going to add a second `background-image` declaration, and we're not going to keep it this way (we're doing something wrong here), but it turns out if you put two of the same declarations in the same ruleset, it will ignore the first one and use whatever value you put in the second one. So that's what we're going to do. We're going to add a linear gradient here. I'll just show you a quick example.

```
header {
  ...
  background-image: linear-gradient(red, yellow);
}
```

`background-image`, `linear-gradient`, parentheses, and then a comma-separated list of colors: `red, yellow`.

![linear gradient](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/gradient1.png)

Beautiful! That also fixes our readability problems, doesn't it? The text is really readable against that gradient background.

You can also use more than two colors. You can list any number of colors that you like. Let's add `white` to the mix here.

```
header {
  ...
  background-image: linear-gradient(red, yellow, white);
}
```

![linear gradient](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/gradient2.png)

There we go. It becomes slightly less readable, but now it fades very nicely into that white background. There's a problem here though. We can't see our salamander at all, and that's kind of the whole point.

Well, guess what? We can put background images on top of each other.So we can put our gradient _on top_ of our image. Right now, the gradient is the only background image it's using, because it comes second in the list. We used two `background-image` declarations. Let's go back down to just one `background-image` declaration, and let's separate our two values&mdash;our gradient and the URL&mdash;with a comma. So let's move the actual image URL to right after the `linear-gradient` value, with a comma in between the two. And let's get rid of this first `background-image` declaration now.

```
header {
  ...
  background-image: linear-gradient(red, yellow, white), url(...salamander.jpg);
}
```

 This is a little hard to read all on one line. It turns out, CSS, like HTML, doesn't really care where you put line breaks. Let's just put a line break before `linear-gradient` and right after the comma.

```
header {
  ...
  background-image:
    linear-gradient(red, yellow, white),
    url(...salamander.jpg);
}
```

There we go. That's a little clearer. So we have a comma-separated list of background images as the value for our `background-image` property, and that _should_ put the gradient _on top_ of the image. And it did. You just can't tell, because, well, the gradient is covering up the whole image. We need those colors to be semi-transparent if we want to actually see the image poking out underneath. And to do that, we're going to need to learn how to mix colors manually instead of just referring to them by name. Referring to colors by name is great, and there are 147 different color names we can use. But by mixing our own colors, we have access to 16.7 million. And 16.7 million is bigger than 147. So let's learn how to do that now.

Anyplace that you can use a named color, you can also use an **RGB** color: RGB as in red, green, blue&mdash;the three primary colors of light.

```
color: rgb(255, 50, 100);
```

Each of the three primary colors can have one of 256 values, 0-255. A value for red (`255` is this example), a value for green (`50`), and one for blue (`100`), in that order. This particular color <span style="background-color: rgb(255, 50, 100); color: white;">looks like this</span>.

What do you think `rgb(255, 255, 255)` would be? All three colors turned all the way up? That's white. How about all zeroes, `rgb(0, 0, 0)`? You guessed it. That's black. You should experiment and mix some interesting colors of your own.

Let's use RGB colors in our gradient instead of named colors. So instead of `red, yellow, white`, let's try... let's try red again. So RGB is red, green, and blue in that order. So the red should be `255`, and the green and blue should both be zero: `rgb(255,0,0)`. So that's one color in our gradient. For the second color, let's see if we can do yellow again. So that's red all the way up, green all the way up, and no blue: `rgb(255,255,0)`.

```
header {
  ...
  background-image:
    linear-gradient(rgb(255,0,0), rgb(255,255,0)),
    url(...salamander.jpg);
}
```

And there we go. We have our red-to-yellow gradient. Perfect.

So what has this gained us? Well, it gets us one step closer to having transparency. To specify transparency in our colors, we use **RGBA** instead of just RGB. That's red, green, blue, and an addition value for **alpha**. So instead of `rgb()`, we use `rgba()`.

```
color: rgba(255, 50, 100, 1);
```

That fourth value ranges from 0, for completely transparent, to 1 for completely opaque. So for translucency, we use a decimal value between 0 and 1.

So let's replace our yellow with an RGBA value. First, we add the `a`, then we add a fourth value. What if that fourth value is simply `0`?

```
header {
  ...
  background-image:
    linear-gradient(rgb(255,0,0), rgba(255,255,0,0)),
    url(...salamander.jpg);
}
```

![linear gradient](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/gradient3.png)

Well, then the yellow becomes completely transparent, and we get a gradient from red to transparent. That actually looks pretty nice. What if we made it `0.5`?

OK, then we get a gradient from opaque red to translucent yellow. What if we make the red RGBA as well and say it's `0.7` to start?

```
header {
  ...
  background-image:
    linear-gradient(rgba(255,0,0, 0.7), rgba(255,255,0,0.5)),
    url(...salamander.jpg);
}
```

![linear gradient](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/gradient4.png)

All right, then we get translucent red to translucent yellow, and our text is pretty readable, and we can still see our salamander. That actually looks pretty nice as it is.

If we wanted to just darken the image, and not change its color at all, we could use an RGBA black and fade from 50% transparent black (`0.5`) to 50% transparent black.

```
header {
  ...
  background-image:
    linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)),
    url(...salamander.jpg);
}
```

So we just want to darken the image. We don't actually want to change its color. So come up with something that you like. Just make sure the text is readable, and you can see the salamander underneath. Got it? Great.

This is starting to look pretty good, but we have awfully boring fonts on the page. We're just using the defaults. So next time, we'll learn how to replace those using web fonts.

Until then, I'm Davey Strus. Haaaappy hacking!
