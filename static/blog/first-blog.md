# Welcome
**Welcome** to my first-ever blog post here! This whole blog post system will probably end up changing at some point, but this is what I have so far. I actually want to talk about how I built this blog system for this post.
## How my website is built
This entire site is built with two main systems. The main framework/server, ***Svelte*** and ***Tailwind.css***, the CSS framework. For the main part of the site, this is all that is used, but, I wanted to use a little more for this blogging part of the site.
## How I wanted the blogs to work
When I set out to make this Svelte/Tailwind-powered blogging system, I had a few criteria I wanted it to fulfill:
 - full Markdown support
 - Image Support
 - Easy editing
 - <div style="color: red">Colors!</div>
 - and full support for raw HTML if I wanted to get... creative
## How I made it
The system I ended up going with reads data from a markdown file, and then uses an npm library called `marked` to transform the markdown into HTML. Svelte then proceeds to render the entire HTML-ified string with the `@html` Svelte property. All of this is componentized, with the main page document just calling a component "*BlogRenderer*", which sets up the blog site, and calls the "*MarkdownRenderer*" component to actually render the markdown with the code described before.
## Why use this complicated system
You're right, to an extent. This system is extremely complicated, and essentially does the same thing as just writing it all in HTML in one large document. However, it does provide a few major benefits.
1. Making a new blog post is dead simple. Just create a new folder, a simple +page.svelte that calls the renderer, and start writing away in the markdown file. Again, dead simple.
2. Editing existing blog posts is simple as well, just edit the markdown and everything updates.
3. No messing around with HTML elements is required, meaning I can just write super quick and efficient markdown.
4. Changing the blog design, or adding new features can just be done once, and update globally, across all blog posts. No need to update each page.
5. It's quick, not slow and buggy. All the markdown conversion is done server-side (due to Svelte being **AWESOME**), and quick and plain HTML is sent to the browser.

So yeah, that's why I did it like this!
## Conclusion
Thank you for reading this, and thank you for visiting my site. Individual blogging is getting less popular, but it can really still provide insight into the lives of people who actually use the tools in projects. Please check back here every once in a while, because I may write something you are interested in. I will be writing a whole bunch of tech and development-related content here, so please, enjoy! And as always, Happy Coding!