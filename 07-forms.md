Hey, everyone. Welcome to Kenzie Academy. This is Davey Strus.

Let's continue our journey into HTML with an exploration of forms. Our design has a form in it. Our markup so far does not. In this video, we'll fix that. Along the way, we'll learn about forms themselves, form inputs, and buttons. Our magic journey continues now.

Code along with me using the editor on this page, and remember to pause the video as often as you need to.

It looks like the form is inside the main area of the page, after "We hope to see you October 13", but before the footer. So we'll add it to the page just before the closing `</main>` tag. So let's add an extra line here under the paragraph&mdash;maybe two extra lines&mdash;and let's create a form. Anyone care to guess what that element is called? That's right: `form`.

```
<main>
  <h3>Album release party</h3>

  <p>We hope to see <em>you</em> <strong>October 13</strong>!</p>

  <form></form>
</main>
```

Piece of cake. Now, that form had two places for users to type in input, as well as one button. So we need to put some stuff in between the opening and closing `form` tags. We'll go ahead and put those things on new lines inside the form element.

First, we'll put an input: Simply the `input` element. Like images, inputs are _empty_ elements. They have no contents, and they have no corresponding closing tag. Once again, the closing tag isn't optional; it's actually forbidden. We do not have one.

```
  <form>
    <input>
  </form>
```


So that's one input. That's one place for a user to type something, and we see that it shows up on the page. Nothing showed up when we just had a form, but a form with an input in it shows us something.

Now we need a second input.

```
  <form>
    <input>
    <input>
  </form>
```

And there it is! And once again, we see that these are side by side in the preview, despite the fact that there's a new line between them in the markup. The new line between them in the markup is the same as having one space between them. Makes no difference. Only if `input` were a _block_ element would they appear on separate lines. But it's not. `input` is _inline_, like `em` and `strong`, so they show up side by side.

So we have a form with two inputs. Now we need one more thing in our form, and that is a _button_. So after the second input, let's add another new element called, predictably enough, `button`. And `button` does have a closing tag. And whatever you put between the two tags is what will show up on the button. Our button said "RSVP" in the design, so we'll type "RSPV" between the opening and closing `button` tags...

```
  <form>
    <input>
    <input>
    <button>RSVP</button>
  </form>
```

...and there we go! A button that says "RSVP".

So here's our form. One input where we can type something, another input where we can type something, and a button labeled "RSVP". Beautiful! That wasn't so bad, was it?

Forms can get a lot more complicated than this. There are different types of inputs, and there are entirely different types of form controls besides inputs and buttons. But this will do for now. So does yours look like mine? Great. We have the form on the page.

Next time, we will look at different input types, and we'll look at how to label those inputs, because right now, the user has no idea what is supposed to go in each of those fields. They're blank.

So until then, I'm Davey Strus. Haaaappy hacking!
