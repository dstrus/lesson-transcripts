Hey, everyone. Welcome to Kenzie Academy. This is Davey Strus.

We now have our element spacing tweaked just so, but we're not finished yet. Let's talk about borders. In this video, you'll learn how to add a border to an element. You'll learn how to set the border width, style, and color. You'll even learn how to add borders with rounded corners. Ready?

Code along with me using the editor on this page, and remember to pause the video as often as you need to.

Let's take a closer look at that image of Beasley.

![finished design](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/bard-screenshot.png)

In the original design, Beasley is in a white circle. That's not using a different image. The white circle is nothing more than a **border**. We can add borders to an element with the `border` property in CSS.

```
border: 1px solid blue;
```

Border accepts any combination of these three values: Border width, style, and color. You can specify any one of these values, any combination of two, or all three. Any that you leave out will have a default value.

Let's add a border to our image. We don't have a ruleset for our image yet, so let's add one at the very bottom. Go ahead and scroll down, and we'll add a new rulset with the selector `img`, because that's why type of element it is. Don't forget your curly braces, and we'll add the `border` property to our new declaration, and let's just experiment with some values here.

```
img {
  border: 1px solid pink;
}
```

`1px solid pink`. Why not? Hey, there we go. It showed up. How about `10px`?

```
img {
  border: 10px solid pink;
}
```


Yeah, all right! So, width, style, and color. With can be something like this&mdash;just a value in pixels or some other unit&mdash;or it can be something like `thin`, `medium`, or `thick`. I actually like `thick` for this. That happens to be the same as `5px`.

```
img {
  border: thick solid pink;
}
```

Border style can be a number of different things: `solid` (probably the most common), `dashed`, `dotted` (which is not the same thing as `dashed`), `double` (that's fun!). There are a few others, but I think you get the picture. `solid` is what we want. And then any color we can think of: `pink`, `cornflowerblue`, or, you know, just `white`.

```
img {
  border: thick solid white;
}
```

`thick solid white`. That seems like a pretty good border to me. Now how do we make it round? We do that with `border-radius`. So we'll add a new declaration: `border-radius`. And `border-radius` takes a value in pixels or some other unit. Let's try `5px`. Let's see what that gets us.

```
img {
  border: thick solid white;
  border-radius: 5px;
}
```

OK, it's a little bit rounded now. I don't know if you can see that. Let's try `15px`.

```
img {
  border: thick solid white;
  border-radius: 15px;
}
```

Now it is more dramatically rounded. How about `25px`? We can just keep going until we find something we like, but I had it as an actual circle. You can do that by setting the radius to half the width of the image, assuming that the image is, in fact, square&mdash;which ours is. I don't know off the top of my head how many pixels wide this image is, so I can use a different unit. How about `50%`?

```
img {
  border: thick solid white;
  border-radius: 50%;
}
```

A `border-radius` of `50%` will always get you a perfect circle if you have a square image. Obviously, if you don't have a square image, your mileage may vary. But 50% will get us a circle in this case, and that's exactly the border that I was hoping for. Perfect!

Here's another little secret: You can have a different border on each side. There are properties `border-top`, `-right`, `-bottom`, and `-left`.

```
img {
  border-top: thick solid white;
  border-radius: 50%;
}
```

Now we only have a border on top. How about `border-right: 10px dashed pink;`?

```
img {
  border-top: thick solid white;
  border-right: 10px dashed pink;
  border-radius: 50%;
}
```

OK, a little silly looking, but we can totally do that if we want to. I'm just going to stick with one border all the way around.

```
img {
  border: thick solid white;
  border-radius: 50%;
}
```

As long as I'm handing out borders, I'd like to give borders to our inputs and button. So those are the two preceding rulesets in our stylesheet.

```
input {
  padding: 8px;
}

button {
  padding: 8px 24px;
}
```

On `input`, let's go with `1px solid gray;`.

```
input {
  padding: 8px;
  border: 1px solid gray;
}
```

There we go. And for the button, let's do the same: `1px solid gray;`.

```
button {
  padding: 8px 24px;
  border: 1px solid;
}
```

You know what? I like it.

Feel free to play around with borders a little more if you want to. If you're satisfied with what you have, then we'll move on. Next time, we'll learn how to adjust font sizes.

Until then, I'm Davey Strus. Haaaappy hacking!
