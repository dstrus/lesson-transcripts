Hey, everyone. Welcome to Kenzie Academy. This is Davey Strus.

It's time to get real! Let's start making our first web page. We'll start by focusing on HTML headings. By the end of this video, you'll know how to create six levels of headings in HTML. Ready? Let's jump right in.

In pretty much every video from here on out, I'm going to ask you to code along with me. Whenever I do so, I urge you to pause the video as often as you need to in order to keep up. Never be afraid to press _pause_. OK? So go ahead and follow along using the editor that's on this page. It may look a little different from the editor in my video, but that's OK.

Now the way that this is written right now, to start, all the text is smashed together in the preview, despite the fact that there are a bunch of line breaks over here. We have a line break after `Salamander` and before `The`, and yet we just see a space between the two here [in the preview]. This is how HTML works. It treats all _white space_&mdash;spaces, new lines, tabs, everything like that&mdash;as exactly one space. If I put five line breaks in between these two, it doesn't matter. It's still going to show up as a single space. It's just how HTML works. But it lets us put a lot of line breaks and spaces and tabs in, to make our code nice and readable. But if we want "Night of the Salamander" to be on a separate line from "The new release from Beasley the Bard", we're going to have to use HTML elements to do that.

So let's go ahead and use the HTML element that we know: H1, top level heading.

So at the very beginning, before "Night of the Salamander", put `<h1>`. Now as soon as we do that, notice what happens. Now the entire thing looks like an H1. All the fonts get big and bold. At the end of the first line ("Night of the Salamander"), go ahead and put the corresponding closing tag for the H1: `</h1>`.

```html
<h1>Night of the Salamander</h1>
```

Now it knows where the H1 ends, and so only "Night of the Salamander" is big and bold, and it's on a line by itself. That's good news. No longer is absolutely everything smashed together. Now everything _else_ is still smashed together. We still have work to do. But hey, it's a step in the right direction!

How about we make "The new release from Beasley the Bard" (the second line here) an H2. So let's put `<h2>` at the beginning&mdash;and again, the whole rest of the document changes to look like an H2, which is slightly smaller, but still bold&mdash;and at the end of the line, the closing tag: `</h2>`.

```html
<h2>The new release from Beasley the Bard</h2>
```

And now "The new release from Beasley the Bard" is on a line by itself, and it's big, but not as big as the H1.

Now, we only only have one H1 and one H2 on this page, but that's not a rule or anything. You can put as many H1s or H2s on a single page as you want. There's no rule that says you can only have one H1. We just happen to only need one H1 in this document.

Let's make "Album release party" an H3. Put the opening tag (`<h3>`) and the corresponding closing tag (`</h3>`)...

```html
<h3>Album release party</h3>
```

...and we'll see that "Album release party" is a little bigger than the rest of the text, and still bold, but not as big as an H2 or an H1. And there's automatically a line break at the end, and some space between it and what follows. If we wanted to put [a blank line] in between this and "We hope to see you October 13!", we can. It makes no difference in the way the page is rendered, but it makes our code&mdash;our _markup_&mdash;a little more readable.

So now we have an H1, an H2, and an H3. You may be wondering how many of these there are. There are six levels of heading in HTML, H1 through H6. There's no H7. H1 through H6 are all HTML headings, and the text gets progressively smaller as the number gets larger.

Does your screen look like mine? Great! You've taken your first step into a larger world and mastered the art of the HTML heading.

Next, we'll learn how to add the markup for paragraphs, and how to emphasize specific pieces of text, making them bold or italicized.

Until then, I'm Davey Strus. Haaaappy hacking!
