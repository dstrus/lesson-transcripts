Hi, everyone. Welcome to Kenzie Academy. I'm Davey Strus.

So you want to learn how to build things for the web? Great&mdash;let's do it! Over the next several videos, you'll be building an invitation to an album release party using a pair of technologies called <strong>HTML</strong> and <strong>CSS</strong>.

In this first video, we're going to get started with HTML. By the end, you should be able to describe the role of HTML in authoring web content, and describe the different parts of an HTML element.

Ready? Let's get started.

HTML is the language we use to author all of the content of our web pages and how we add structure to that content. With HTML, we're not yet terribly concerned with how a web page looks, just with how it's structured and what the content is.

It all started in 1989 when this guy, Tim Berners-Lee, proposed a project called WorldWideWeb for sharing scientific documents in hypertext.

Wait, hyper<em>what</em>? Hypertext! Hypertext is "a software system that links topics on the screen to related information and graphics, which are typically accessed by a point-and-click method." In other words: Text that links to other text.

And that's all the web was initially: A bunch of text documents with links between them. No videos, no cat GIFs&mdash;it was just plain hypertext. And although hypertext existed before the web, when Tim Berners-Lee first launched the World Wide Web in 1990, he created a new language for authoring hypertext documents, and he called it HTML. Care to guess what the <em>HT</em> stands for? No, not "helicopter turtles." Good guess though. That's right: Hypertext!

HTML stands for <strong>Hypertext Markup Language</strong>. We know what hypertext is now, and we've established that HTML is a language. But what is <em>markup</em> in this context? Well, it's a bit like the way a proofreader marks up a page. In HTML, we mark up a document to indicate the different parts of that document and the relationships between those parts. Each of those individual parts is an HTML <strong>element</strong>, and we indicate where each element begins and ends using <strong>tags</strong>.

This is an HTML version of <cite>Pride and Prejudice</cite>. What do we have here? We have a heading for the title, a subheading for the author, another subheading for the chapter, some navigation made up of links to jump between chapters and the full text, and a bunch of paragraphs. Each of those things is an element, so let's have a look at one of them.

```html
<h1>Pride and Prejudice</h1>
```

This is an HTML element. The beginning and end of the element are marked with tags. The tags are what makes this markup instead of just text. We have two tags here: An opening tag and a closing tag. Both tags are enclosed in angle brackets&mdash;the <em>less than</em> and <em>greater than</em> signs.

Inside the angle brackets, the opening tag simply has the element type&mdash;in this case, H1, which represents a heading. Because it's a heading, the browser will, by default, display the text large and bold.

The closing tag also contains the element type, but this time there's a forward slash (<code>/</code>) in front of it. That slash indicates that this is a closing tag, marking the end of the current element rather than the beginning of a new element. (The forward slash, by the way, is the one that shares a key with the question mark on most keyboards. Be sure to use that one and not a backslash. A backslash will not work.)

Everything between the two tags is the <em>content</em> of the element. In this case, it's just text. This is what will actually show up on the page. The browser does not draw the tags themselves on the finished product, just the content in between. How that content looks depends on the type of element. In this case, big and bold, because it's an H1.

So put it all together, and we have an HTML element. Let's review.

HTML is the language we use to author the content of web pages and define the structure of that content. It stands for Hypertext Markup Language. Hypertext refers to text that contains links. Markup refers to the way we indicate the different elements of the document, using tags&mdash;an opening tag to indicate where an element starts, and a closing tag with a forward slash in it to indicate where an element ends.

Got it? Great!

In the next video, we'll actually get an editor set up so we can start writing HTML of our own.

Until then, I'm Davey Strus. Haaaappy hacking!
