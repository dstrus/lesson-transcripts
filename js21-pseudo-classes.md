Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

Let's add a little more fancy CSS. This time, we'll use **pseudo-classes**. Pseudo-classes are something you can add to the end of a selector to indicate that it should only match an element when that element is in a particular _state_&mdash;for example, when the mouse is hovering over that element; or a link, but only if that link has been visited before. So we can do that with pseudo-classes.

Let's use a simple example here on our list item. I'm going to add a new rule in between `li` and `#attendees`, just because it's related to the list item. And I'll add a rule for `li:hover`. That `:hover` is a pseudo-class that says, as you might expect, that this rule only applies when that element is being hovered over with the mouse cursor. So what can we do differently when we're hovering? How about we change the background to `gold`?

```css
li:hover {
  background: gold;
}
```

Observe. Now, when I'm hovering over it, it's gold. When I'm not, it's white. Cool!

There are a whole bunch of pseudo-classes. Let's learn another. Right now, every list item has a top border. But the list itself also has a border, which means that the very first list item kind of ends up with a double border on the top&mdash;the one that's applied to the list items, and the one that's applied to the list itself. So let's get rid of the top border for `li` when it's the _first_ `li`.

So I'll add another rule. This time I'll use the pseudo-class `:first-child`.

```css
li:first-child {

}
```

An element is a **child** of another element when it appears inside that element&mdash;in other words, when it appears in between the opening and closing tags of another element. In this case, each of the list items is a child of the list itself. And the first list item is the first child of its parent, and that's what the `:first-child` pseudo-class means: Any element that is the first child of its parent. So this rule applies to any _list item_ that is the first child of its parent. That ought to apply to our first list item. So if we match that selector, let's go with `border: top: none;`, and then we no longer have a double border.

```css
li:first-child {
  border-top: none;
}
```

It's subtle, but it makes me feel better.

Next, I would like to alternate the background colors of the `li`s, so that every other one is a slightly different color. Let's see if we can do that. Make sure you have at least a couple of items in your list. I'm going to go ahead and put four in mine. There we go. That way I can be sure it's working. This time, I'm going to use a pseudo-class called `:nth-child`.

```css
li:nth-child {

}
```

`:nth-child` is interesting, because it takes a parameter.  You can put a number in here: `:nth-child(2)` for the _second_ child of its parent, or `:nth-child(3)` for the _third_ child of its parent. And you can actually get pretty crazy with this one. One cool thing I like to do is put `even` or `odd` in there.

```css
li:nth-child(even) {

}
```

And then you end up applying this rule to every other one. So that's what I'm going to do. I'm going to apply this rule only to the _even_ children of the parent. In other words, every other list item. And then I'm going to change the background color from white to a nice, light gray.

```css
li:nth-child(even) {
  background-color: rgb(246,246,246);
}
```

Look at that. Look at the stripeyness! Isn't that cool? Now, look at this&mdash;we lost a little something when we did that. Now my gold `:hover` effect only works on the _odd_ ones. Why do you suppose that is? That's because this rule for the even children is overriding the background for `:hover`. Whoops! If I put my `:hover` rule _after_ my `:nth-child(even)` rule, though, then I get my hover effect back. Sometimes the order does matter in CSS.

You'll notice I used `background-color` on my `:nth-child(even)` rule, but I used `background` in the `:hover` rule. `background-color` is just more specific. The `background` property can apply background images, background position, and a whole bunch of other stuff, but `background-color` targets only the color. There's nothing wrong with using just plain `background` when you're only applying the color, but I used `background-color` this time. It makes no difference. We can change it to `background`.

```css
li:nth-child(even) {
  background: rgb(246,246,246);
}
```

The effect is the same. It still stripes them, and because I ordered them correctly, I still get my hover effect as well.

This is looking pretty good. Let's make sure that "Reveal" button still works... yeah, it does. Look at that. Well, congratulations. You've learned just enough JavaScript to be dangerous, but we hope this is only the beginning of your journey. Remember to talk to the admissions team at Kenzie to learn about the full slate of programs.

Hope to see you again later. Until then, this is Davey Strus. Haaaappy hacking!
