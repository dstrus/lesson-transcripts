Hey, everyone. Welcome to Kenzie Academy. This is Davey Strus.

There's a little something missing from this page. I know: A salamander! Yes, we need Beasley's album art on the page. We need... a HERO IMAGE!

There's a trend in web design to have a huge image front-and-center on the page, maybe with some nice text on top of it. And we want the trendiest folks in the city to attend the album release party, so far be it from us to shy away from a trend. Let's learn how to add a giant image that always displays at just the right size.

Code along with me using the editor on this page, and remember to pause the video as often as you need to.

The image we're adding this time is different from the image that's already on the page. This one is a **background image**, which means we're not going to use an `img` element to add it. It is simply going to be added with CSS. And it belongs in the background of the `header` element, specifically. We already have a `background` on the `header` element. Let's go ahead and get rid of that gray background. We're going to have a background _image_ instead, so let's add a new declaration to our `header` ruleset with the property `background-image` (notice the hyphen). To specify a background image, we need to give it the URL. We do that by actually typing `url` and then a set of parentheses. Inside the parentheses, we put the URL to our image. You can copy and paste the URL of the image from this code block below:

```css
header {
  color: white;
  height: 400px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/1152887/salamander.jpg);
}
```

There we go. The image is there. It's not where we want it. It doesn't look quite right, but, by golly, the image is there. It's a start. Among other things, the image is just way too big. The tail is all that shows up, and even that is just barely there. So I'd like to resize this background image. Wouldn't you know it&mdash;there's a CSS property called `background-size`. You can give it values like we've given values in the past, like pixels. Let's make it `100px` and see what happens.

```css
header {
  ...
  background-size: 100px;
}
```

OK, now we have a whole bunch of salamanders. Not quite what we wanted. It's repeating over and over. Well, guess what? There's another property `background-repeat`, and we can give it the value `no-repeat`, just like that.

```css
header {
  ...
  background-size: 100px;
  background-repeat: no-repeat;
}
```

And now it doesn't repeat. But now we can see that `100px` is just way too small. So what are our other choices here? We don't have to give it a pixel value. We can also say things like `contain`. `contain` will shrink the image so that the whole image fits in the element, but it might not necessarily cover the entire element. We want to make sure we cover the entire element. As it is now, it had to shrink it so that there's way too much blank space at the bottom. So for that, we can say `background-size: cover;`.

```css
header {
  ...
  background-size: cover;
  background-repeat: no-repeat;
}
```

We'll be guaranteed that the image will cover the entire element. It will make it as big or small as it needs to, in order to just barely cover it. That's `background-size`. It would sure be nice if the image were centered though. For that, we can turn to `background-position`. `background-position` can take values like `top`, `top right`, `top left`, etc., and one of those options is, naturally, `center`.

```css
header {
  ...
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}
```

There we go: `background-position: center;`. That's more like it.

At this point, this probably qualifies as a **hero image**, but it's not perfect. Our text is a little hard to read over that. I really wish there were some sort of color overlay on top of the image, so that the text were a little easier to read. Next time, we'll do exactly that.

Until then, I'm Davey Strus. Haaaappy hacking!
