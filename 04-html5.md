Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

Let's add some structure to our invitation page. In this video, we'll learn some new elements that were added in HTML 5. By the end, you'll know the `header`, `main`, and `footer` elements. Ready? Let's go.

Code along with me using the editor on this page, and remember to pause the video as often as you need to.

All we're going to do is add three new elements that were new in HTML 5. HTML 5 was released in 2014 and is very well supported by now. And all these elements do is add some structure to the page. They don't actually change its appearance. They will, however, be convenient when we get around to adding style to the page later.

H1, H2... these are part of the _header_ of our document. The H3 and the paragraph underneath it... that's really the main content section of our page. And the two credits at the bottom are the footer of the page. So let's wrap them in elements that indicate such.

At the very beginning of the document, I'm going to add an element,  `<header>`. And I'm going to put a corresponding closing tag down here above "Album release party".

```html
<header>
<h1>Night of the Salamander</h1>
<h2>The new release from Beasley the Bard</h2>

<!-- https://s3-us-west-2.amazonaws.com/s.cdpn.io/1152887/beasley.png -->
</header>
```

So that includes the H1, the H2, and this weird little thing that we haven't talked about yet. We'll get to that soon. Don't worry. Now everything between the open and closing `header` tags is a header, right? It isn't terribly easy at a glance to tell where it begins and ends, because the opening tag and the closing tag are several lines away from each other. Sometimes you'll have pages and pages of markup, and you can make your life a whole lot easier by doing something to make these things easier to find. So what we can do is _indent_ the markup in between the opening and closing tags. CodePen makes this really easy. You can just highlight all of those lines&mdash;everything in between the opening and closing `header` tags&mdash;and hit <span style="font-family: monospace; border-radius: 4px; border: 2px solid #ccc; border-bottom-width: 3px; margin-right: 5px; font-size: 14px; padding: 1px 5px;">Command</span> + <span style="font-family: monospace; border-radius: 4px; border: 2px solid #ccc; border-bottom-width: 3px; margin-right: 5px; font-size: 14px; padding: 1px 5px;">]</span> on Mac, or <span style="font-family: monospace; border-radius: 4px; border: 2px solid #ccc; border-bottom-width: 3px; margin-right: 5px; font-size: 14px; padding: 1px 5px;">Ctrl</span> + <span style="font-family: monospace; border-radius: 4px; border: 2px solid #ccc; border-bottom-width: 3px; margin-right: 5px; font-size: 14px; padding: 1px 5px;">]</span> on Windows, which is common keyboard shortcut for indenting in code editors.

```html
<header>
  <h1>Night of the Salamander</h1>
  <h2>The new release from Beasley the Bard</h2>

  <!-- https://s3-us-west-2.amazonaws.com/s.cdpn.io/1152887/beasley.png -->
</header>
```

Now this indents that markup without actually changing the way it appears on the page. We are just indenting our markup to make it easier to tell where the corresponding closing tag is to this opening `<header>` tag.

Similarly, let's wrap the H3 and paragraph in a `main` element. Opening tag, closing tag, let's go ahead and indent everything that's in between...


```html
<main>
  <h3>Album release party</h3>

  <p>We hope to see <em>you</em> <strong>October 13</strong>!</p>
</main>
```

... beautiful! Look at that structure! And then everything else I'm going to put inside a `footer`. Opening `<footer>` tag, and then at the very, very bottom, a closing `</footer>` tag. And indent everything that comes in between.

```html
<footer>
  <p>Pixel art by Eric Alloway (@Iscaneus).</p>

  <!-- https://twitter.com/iscaneus -->

  <p>Fire salamander photo by Cristo Vlahos. <a href="https://creativecommons.org/licenses/by/3.0">CC BY 3.0</a></p>
</footer>
```

Nothing earth-shattering here, but I think it makes it a little easier to find what we're looking for as we look through the markup to have it organized this way.

Now then, does yours look like mine, with a `header` at the top, a `main` section in the middle, and a `footer` at the bottom? OK, great. Ready to move on.

Next time, we'll learn how to add images to a page, as well as how to add comments in HTML.

Until then, I'm Davey Strus. Haaaappy hacking!
