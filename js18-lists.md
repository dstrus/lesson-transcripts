Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

Our form currently adds to a list of attendees, except we don't use list elements in our HTML. We have a `div` containing the entire list, and then each new item in the list is a paragraph. I think we could choose elements better suited to the task.

There are two common types of lists in HTML: **Ordered lists** and **unordered lists**. There's a third type, the **description lists**, but it's far less common, and we're not going to worry about it for right now.

First up: Ordered lists. Ordered lists are automatically numbered. The element for ordered lists is `<ol>`, "ordered list". That's the list itself.

Each item in the list, then, is a **list item**. The element for list items is `<li>`, "list item". Inside the list item, you can have just about any elements you want: paragraphs, headings, even another list. Regardless of what's inside the list items, each list items will automatically have a number beside it. By default, the counting starts at `1`, but you can change that by adding a `start` attribute to the `ol`.

```html
<ol start="5">
  <li>California</li>
  <li>Colorado</li>
  <li>Connecticut</li>
<ol>
```

That's pretty much all there is to ordered lists.

The other lists we're interested in are unordered lists. Rather than being numbered, unordered lists show up as bulleted lists. The element: `<ul>`, "unordered list". And again, you populate it with list items (`<li>`). This time, instead of having numbers show up automatically, bullets will show up automatically next to each list item.

```html
<ul>
  <li>Woke up</li>
  <li>Got out of bed</li>
  <li>Dragged a comb across my head</li>
</ul>
```

Even though it's called an _unordered_ list, the items will still appear in the order you specify. The only real difference is _bullets_ versus _numbers_. And that's really all there is to it.

Let's try adding our attendees as items in a list, rather than paragraphs in a `div`.

First, we'll want to pop over to the HTML and change that `div` into some sort of list.

```html
  <div id="attendees"></div>
```

There's the `div` with the ID `attendees`. I'm going to change it to an unordered list. I think I'd rather have bullets than numbers. I don't really care what order the people RSVD'd in.

```html
  <ul id="attendees"></ul>
```

All right. Very good.

In our JavaScript, we add each individual attendee to the list. And right now, we're adding them as paragraphs. Let's add them instead as list items. So I'll change the `p` to an `li`, and it should automatically change your closing tag as well, but make sure that it does. If it doesn't, change it manually.

```js
function handleSubmit(event) {
  ...
  list.innerHTML += `<li><strong>${email}</strong>, plus ${guests}</li>`;
}
```

Very good. Now let's see what happens when we fill out the form... and there we go. It's bulleted. The fact that it's centered makes it look a little funny, but we can worry about CSS details later. The fact is, now it's adding list items instead of paragraphs. Let's add a second person... boom. Still works. Adds a second list item to our unordered list. And that's about all there is to it.

Now when I add an attendee, the form doesn't clear out, and my cursor doesn't go back into that email field. I really wish that happened. As it is, I have to click back up there, and then erase what's there... it's just... ugh... it's just _foul_. I wish it just did that automatically. So we'll learn how to do that automatically next time, using JavaScript.

Until then, I'm Davey Strus. Haaaappy hacking!
