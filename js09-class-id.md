Hey, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

Remember IDs and classes? We used them to target elements in CSS. We targeted an element with a specific ID by using a selector with a hash (`#`) in front of that ID. We targeted elements with a specific class by using a selector with a dot (`.`) in front of that class name.

Well, the selectors we use with `querySelector()` in JavaScript are the very same ones we use with CSS. So we can grab an element by its ID or class in JavaScript by using those familiar selectors. Let's give it a shot.

At the moment, we're grabbing that `h1` containing the album title by using the selector `h1`&mdash;its element type. And that works fine, for now, because it happens to be the first `h1` on the page. But were that ever to change, it would no longer work? So why don't we try grabbing it by its ID&mdash;after all, it does have one. If we check the HTML, we see that that `h1` has an ID of `album`.

So how would we grab that using `querySelector()`? Well, the selector would be `#album`, right? Since this is JavaScript, that selector does have to be in a string, so leave the quotes in place, and simply put `#album`. And that selector says, "grab the element with the ID of `album`".

```js
let heading = document.querySelector('#album');
```

 We want to make sure it really is using our new selector. Let's just change the title again&mdash;this time, "Night of the Coriander". That's the same plant as cilantro.

 ```js
 heading.innerHTML = 'Night of the Coriander';
 ```

All right. Looks like it worked. I said this selector will find whatever element has the ID `album`, regardless of the _type_ of element. It doesn't care if it's an `h1`, a paragraph, a footer, or anything else. If you want to make that it not only has that ID, but is also of a specific element type, you can combine the two selectors. Simply put `h1` in front of the `#`.

```js
let heading = document.querySelector('h1#album');
```

Notice there's no space there. It's just `h1#album`, and that says, "find me an `h1` with an ID of `album`". That's not necessary, so I won't do it this time, but that's a good trick to keep in your back pocket. We might need it here in a minute.

So how about using a class with `querySelector()`? "Pre-order now!" Look at that big exclamation point. "The cool kids will all be there". That deserves an exclamation point too. Let's put one at the end. Sure, we could flip back to the HTML and do it there, but where's the fun in that?

All right, so I'm going to create a new variable called `preorder`, and I'm going to try to grab that paragraph. Looking at our HTML, that paragraph has a class of `dark`. OK, but so does that `h1` right above it. Hmm. So if I say `document.querySelector('.dark')`, that will find the first element on that page with a class of `dark`. And then let's try to append an exclamation point to the end.

```js
let preorder = document.querySelector('.dark');
preorder.textContent += '!';
```

And what happened? It put a second exclamation point at the end of that `h1`: "Pre-order now!!" I wanted it at the end of the paragraph underneath. Ah-ha, but instead of saying, "find me the first element with a class of `dark`", I could say, "find me the first paragraph with a class of `dark`" by changing the selector to `p.dark`, combining the element type selector with the class selector.

```js
let preorder = document.querySelector('p.dark');
preorder.textContent += '!';
```

Excellent. Now we've not only used ID and class selectors in CSS, we've used them in JavaScript as well.

Next time, we're going to learn about JavaScript **functions**, so GET PSYCHED!

Until then, I'm Davey Strus. Haaaappy hacking!
