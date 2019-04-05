Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

We now have all of our HTML built out for this project, but it's supposed to look like this...

![finished design](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/bard-screenshot.png)

...and right now, it looks like this.

![in progress design](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/bard-progress.png)

It's perfectly functional, and there's plenty to be proud of here, but it could be prettier. For that, we need Cascading Stylesheets, or CSS. We define content and structure in the HTML, and appearance and style in the CSS.

Believe it or not there's absolutely no difference between the HTML in those two screenshots. The HTML is identical. The only difference is CSS. So let's talk about it a bit.

Where HTML is made up of elements, CSS is made up of **rulesets**, also called **rules**.

```
h1 {
  background-color: white;
  color: black;
}
```

This ruleset says that every `h1` on the page should have a white background and black text. That seems straightforward enough to read. Let's look at the different parts of a rule.
