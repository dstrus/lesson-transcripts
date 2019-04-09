Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

Looking at our design, it seems we ought to have an image of our man Beasley at the end of our page header. In this lesson, we'll learn how to do just that. Along the way, we'll also learn about HTML comments. Are you ready? Are you _psyched_?! Here we go.

Code along with me using the editor on this page, and remember to pause the video as often as you need to.

Sometimes, you want to add a comment to the page&mdash;something that will appear in the markup that you can see, that will now show up in the finished product. Let's do that right now. Let's add a comment at the very beginning of the document.

So put a couple of blank lines before `<header>`, and then let's add a comment. Type angle bracket, exclamation point, and two hypens: `<!--`. That's the beginning of a comment. Now let's type our actual comment: `My first web page`. Now everything will be considered part of the comment until it runs into `-->`, which it sees here at the end of line 8...

```html
...beasley.png -->
```

...which means that our H1 and H2 actually disappear from the page, because now they're part of a comment. Whoops! We want the comment to end after line 1. Let's add `-->` there...

```html
<!-- My first web page -->
```

...and we see our H1 and H2 come back. We just added a comment to the page. Feel free to use comments as liberally as you want. Leave yourself little notes.

So now we know that this funny looking this at the end of our header...

```html
<!-- https://s3-us-west-2.amazonaws.com/s.cdpn.io/1152887/beasley.png -->
```

...is a comment. That's why it doesn't show up on the page. Now in this case, the comment contains a URL (a web address). That's the URL of an image that we're about to add to the page. It's here for our convenience so we can copy and paste the URL when we actually add the image to the page. And that's what we're going to do next.

Now that's add the image of that handsome devil Beasley. For this, we'll need a new element: `img`. And unlike every element we've added so far, `img` is an **empty element**, meaning it has no contents, and thus has no closing tag. Mind you, the closing tag isn't optional, it's actually forbidden. `img` is always empty and does not have a closing tag.

```html
  <h2>The new release from Beasley the Bard</h2>

  <img>

  <!-- https://s3-us-west-2.amazonaws.com/s.cdpn.io/1152887/beasley.png -->
```

So we have `<img>`, but now somehow we need to specify the URL of the image that we want to add. For that, we'll need to use something we haven't used before: An HTML **attribute**.

```html
<img src="beasley.png">
```

Here's an `img` element with a `src` attribute. You can think of attributes as the _options_ for an element. This attribute tells the document the URL or address of the image to be displayed. Attributes have a name&mdash;`src`, in this case&mdash;and most attributes also have a value&mdash;in this case, the URL of the image. The attribute name and value are separated by an equals sign, and the value is enclosed in quotation marks. For elements that also have a closing tag, the attributes always belong in the opening tag. Never put attributes in a closing tag.

Let's add the `src` attribute to our `img` element. Put a space after `img`, type `src=""`, and then inside the quotation marks, we need the URL of our image, which is right here inside an HTML comment.

```html
  <h2>The new release from Beasley the Bard</h2>

  <img src="">

  <!-- https://s3-us-west-2.amazonaws.com/s.cdpn.io/1152887/beasley.png -->
```

So copy the URL out of there, put it inside the quotation marks, and then you can get rid of the comment.

```html
  <h2>The new release from Beasley the Bard</h2>

  <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1152887/beasley.png">
```

And you should see the image actually show up on the page. Now there's one other attribute that is considered mandatory for images, and that is `alt`. That's where we can provide a text alternative in the event that the image doesn't show up, which could be because it simply failed to load, or because the user is using a screen reader and can't see images. In that event, we need to provide some text that will show up in the image's place. This is just an image of Beasley the Bard, so I'll put `alt="Beasley the Bard"`.

```html
  <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1152887/beasley.png" alt="Beasley the Bard">
```

Piece of cake! And we have an image on our page. Now, does yours look like mine? Wonderful!

Now that we've learned about HTML comments, and we've learned how to add images to the page&mdash;and along the way we learned all about HTML attributes&mdash;next, we'll learn about **hyperlinks**.

Until then, I'm Davey Strus. Haaaappy hacking!
