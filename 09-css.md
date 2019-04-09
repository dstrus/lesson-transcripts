Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

We now have all of our HTML built out for this project, but it's supposed to look like this...

![finished design](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/bard-screenshot.png)

...and right now, it looks like this.

![in progress design](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/bard-progress.png)

It's perfectly functional, and there's plenty to be proud of here, but it could be prettier. For that, we need Cascading Stylesheets, or CSS. We define content and structure in the HTML, and appearance and style in the CSS.

Believe it or not there's absolutely no difference between the HTML in those two screenshots. The HTML is identical. The only difference is CSS. So let's talk about it a bit.

Where HTML is made up of elements, CSS is made up of **rulesets**, also called **rules**.

```css
h1 {
  background-color: white;
  color: black;
}
```

This ruleset says that every `h1` on the page should have a white background and black text. That seems straightforward enough to read. Let's look at the different parts of a rule. CSS rules consist of a **selector**...

![CSS selector](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/css-selector.png)

...and a **declaration block**.

![CSS selector](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/css-declaration-block.png)

The **selector** tells the browser which HTML elements this rule applies to. Selectors can be quite complex, or very simple like this one. If you want a rule to apply to every element of a particular type, the selector is simply the element type&mdash;in this case, `h1`.

Everything else in the rule is part of the **declaration block**, which is inside a pair of curly braces. Curly braces may not get a whole lot of use on your keyboard today, but that's about to change. Inside the declaration block, you'll find one or more **declarations**.

![CSS selector](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/css-declaration.png)

This is where we actually style the elements. This rule has two declarations: One for background color, and another for color. Each of these declarations consists of a **property**, like `color` or `background-color`...

![CSS selector](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/css-property.png)

...and a **value**, like `black` or `white`.

![CSS selector](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/css-value.png)

Between the property name and value, there's a **colon**. And every declaration ends with a **semicolon**.

![CSS selector](https://cdn.jsdelivr.net/gh/dstrus/lesson-transcripts/assets/css-semicolon.png)

If and whenever your CSS isn't working, look first for a missing semicolon. They're very easy to miss, and their absence breaks everything.

If all of this new information seems a bit overwhelming, don't panic. You'll pick up on the way rules are structured as we go along, and frankly, it isn't terribly important that you know terms like "declaration block" off the top of your head. But I'll need to call them something as we work with them, so I may as well use the proper terms, and now you've been introduced to those terms.

Next time, we'll dive in and start making our web page more stylish by actually writing our own CSS.

Until then, I'm Davey Strus. Haaaappy hacking!
