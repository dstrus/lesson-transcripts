Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

Here we are talking about hypertext, and we don't even have any links on the page. Let's add some!

By the end of this video, you'll know how to add hyperlinks to a web page. Sound good? Let's make it so.

Code along with me using the editor on this page, and remember to pause the video as often as you need to.

We added some beautiful pixel art of our man Beasley to the page, and we've actually already credited the artist down here.

```
<p>Pixel art by Eric Alloway (@Iscaneus).</p>
```

"Pixel art by Eric Alloway", and there's his Twitter handle inside parentheses, so wouldn't it be cool if that were actually a link to his Twitter page? Well, it just so happens that the URL of his Twitter page is right here inside an HTML comment.

```
<!-- https://twitter.com/iscaneus -->
```

How convenient! So let's add a link. The element for links is `a`, for _anchor_. So right before the `@`, let's add an `<a>` tag. We'll add the closing tag, `</a>`, right after `@Iscaneus`.

```
<p>Pixel art by Eric Alloway (<a>@Iscaneus</a>).</p>
```

Great! Now the thing that makes it a link and not just an anchor is the `href` attribute. So let's add that attribute to the opening tag.

```
<a href="">@Iscaneus</a>
```

Inside the quotation marks, we'll put the URL that's down here inside the comment. So copy it from here...

```
<!-- https://twitter.com/iscaneus -->
```

...paste inside the quotation marks, and we have...

```
<a href="https://twitter.com/iscaneus">@Iscaneus</a>
```

Now notice that [@Iscaneus](https://twitter.com/iscaneus) is clickable in the preview. Now that we've done that, I think we can get rid of this comment.

Beautiful! We added a hyperlink to our page. Now it happens there's another link already on the page down here.

```
  <p>Fire salamander photo by Cristo Vlahos. <a href="https://creativecommons.org/licenses/by/3.0">CC BY 3.0</a></p>
</footer>
```

So, we have two links on our page now instead of just one. This is real hypertext. Excellent!

We happen to have put both of these links inside paragraphs, but links can be inside any element you want. They can be inside an `h1`, they can be inside `main` but outside a paragraph&mdash;anywhere you want. We could make any of this text linked to some other resource. And you can link to any URL you want on the entire web. The power is at your fingertips!

That about does it for links, so take this opportunity to make sure that yours looks like mine before we move on.

This is shaping up pretty nicely, but if you remember the original design, there's actually an entire form with two fields and a button that isn't even on the page. So we probably ought to do that next.

Until then, I'm Davey Strus. Haaaappy hacking!
