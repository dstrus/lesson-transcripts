Hey, everyone. Welcome to Kenzie Academy. This is Davey Strus.

Now we have a form on the page. It's not bad, but it could be better. So let's explore forms a little more. In this video, we'll cover different input types and labeling inputs with placeholders. All right? On with the show.

Code along with me using the editor on this page, and remember to pause the video as often as you need to.

We have a form with two inputs and a button on the page, but the inputs are entirely unlabeled, so we have no idea what to put in them. Looking at the design, it seems the first input is meant to capture the person's email. All right, let's see if we can give the user some sort of clue that that's what goes there. We can do that by adding a new **attribute** to the first input. That attribute is called `placeholder`.

```
<input placeholder="">
```

So as with other attributes, we have the attribute name, `placeholder`, an equals sign, and quotation marks. Whatever's inside the quotation marks is what will show up as a placeholder in the form field. So we'll write `Email`.

```
<input placeholder="Email">
```

And looks what happens in the preview. Now it says "Email" in there, but as soon as we start typing something else, the placeholder goes away. Backspace over it, and the placeholder comes back. So a placeholder appears as a label of sorts whenever a form field is empty.

I mentioned that inputs have different types. You specify the type of an input, predictably enough, with the `type` **attribute**. The default happens to be `text`.

```
<input placeholder="Email" type="text">
```

Even though we didn't have `type="text"` in this input until now, we may as well have, because that is the default. But there are a whole bunch of types, and one of them just happens to be `email`.

```
<input placeholder="Email" type="email">
```

So we can put `type="email"`, and that's a little more accurate. `type="text"` will work here, but `type="email"` is better. You may not see any difference in the browser we're using right now, but in some browsers it may enforce the format of an email address, or on a mobile device, it may give you a special keyboard just for entering emails. In any case, you ought to use the `type` that best describes the sort of data that goes in the field. In this case, that's `email`, so we'll put `type="email"`.

Looking at the second form field in the design, it looks like that's meant to capture the number of guests the person is bringing. All right, so let's add an appropriate placeholder to the second input: `placeholder="# of guests"`.

```
<input placeholder="Email" type="email">
<input placeholder="# of guests">
```

What about `type`? Again, by default the type is `text`, and that's just fine. There's nothing stopping you from typing in the number of guests in a `text` field. But what would be even better is `type="number"`.

```
<input placeholder="Email" type="email">
<input placeholder="# of guests" type="number">
```

Yes, that's a thing. If we do that, and we look at the field in the preview, notice we can't actually type anything but numbers in here. We can only type numbers. The browser actually stops us from typing non-numerical data. We also get nifty little up and down arrows. Again, this may be slightly different in your browser, because this does depend on the browser and platform you're running it on, but one way or another, `type="number"` ought to give you something that makes it a little more convenient to enter numbers.

So now we have two inputs that are properly labeled and that have proper types. Does yours look like mine? Does it behave more or less like mine? Great!

All right, I think the HTML for this page is done. Nice work! Next time, we'll introduce Cascading Stylesheets for adding a little style to the page.

Until then, I'm Davey Strus. Haaaappy hacking.
