# Introduction to Web Development!!!

### Learning Objectives
- Become aware of the tools a developer frequently uses
- Describe the web at a high level
- Recognize and identify HTML and CSS syntax
- Differentiate between front-end and back-end web development
- Get a clearer picture of how UX designers and web developers can communicate fruitfully

# Setup and introduction to tools

### GitHub

Git is a **version control manager** for code. Sort of like how you can step back to previous versions of a Google Doc. GitHub is a place that many developers host their projects. You can think of GitHub like google docs for code -- it allows for collaboration, and keeps a record of changes made. 

### Code Editors

One of the most important tools in a developer's belt is their _editor_. Developers use special editors that can handle multiple programming languages, provide syntax highlighting, and give additional functionality. Sort of like Word or Pages for code.

I use VSCode. Other popular editors are Sublime, Atom, and Brackets.

[Here's the setup steps for VSCode.](https://code.visualstudio.com/docs/setup/mac)

### The terminal

Another thing developers use constantly is the _terminal_. The terminal is a direct interface to the underlying operating system. Usually you interact with your file structure through a **Graphic User Interface**, or **GUI**. The terminal strips out all of the extraneous things.

Let's set up a couple of things in the terminal:

1. Hit `cmd` + space to open up Spotlight. Type "Terminal" in the bar & hit enter to open terminal.
2. Type `gls -F` to **l**i**s**t all the files & folders in the current directory.
3. Type `mkdir code` to make a new folder called `code`.
4. Type `cd code` to **c**hange **d**irectory into the `code` folder.
5. Type `touch index.html` to create a new file called `index.html`.
6. Type `open .` to open the current directory in the finder.
7. Right-click on `index.html` and select "Open With > Visual Studio Code".

You just learned a bunch of terminal commands! Developers spend a _lot_ of time in the terminal. It's good to at least be able to recognize what's going on.

### Phew. 

Now that we're all set up, let's move on to talking about the internet and maybe even writing a little code!!

# What is the internet???

At its base, the internet is just a collection of documents that are linked to each other. That's it! I mean, that's definitely _not_ it, since there's so much that websites these days do -- but at its core, that's all it is.

The internet was invented by Tim Berners-Lee at CERN to centralize scientific research.

> But J! Didn't Al Gore invent the internet?

[He didn't, actually](http://www.snopes.com/quotes/internet.asp). He helped create an environment where the internet could flourish.

### What is the internet _made of_, though?

The internet that you see on a day-to-day basis is made up of _HTML documents_. HTML stands for **H**yper**t**ext **M**arkup **L**anguage. When the browser loads a webpage, it's looking for HTML.

# HTML

Every HTML document has two basic parts: the **head** and the **body**.

- The **head** has information about the page: any stylesheets that may be necessary (we'll get to those in a second), the SEO information, the title, etc. It doesn't display in the browser.
- The **body** is the webpage itself.

## HTML Syntax

- Tags are elements on the page. Each have their own name and are enclosed by the caret syntax.

![HTML Tag Syntax](./assets/tags.png)

- Most tags have attributes that can add additional information to the element.

![HTML Tag Attributes](./assets/tags_attributes.png)

## HTML Structure

HTML is structured in a tree-like way: elements can contain elements, which can contain elements, which can contain elements... and so on, ad nauseum. 

Here's an example:

```
<!DOCTYPE html>
<html>
<head>
	<title>Website Title</title>
</head>
<body>
	<div>
    <h1>My Awesome Site</h1>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </div>
  <div>
    <div>
      <h2>About Our Company</h2>
      <div>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc rhoncus lacus sit amet accumsan facilisis. Vivamus mattis sodales mauris, sed dignissim mi iaculis quis. Suspendisse ultrices turpis a lorem elementum luctus. Vestibulum pretium ipsum eu magna feugiat dignissim. Phasellus mauris massa, tincidunt a sollicitudin eu, tempus eu elit.</p>
        <p>raesent et est dolor. Aenean efficitur tellus vel fringilla porta. Vestibulum condimentum porta elit, in cursus sapien facilisis sed. Maecenas in est placerat, sollicitudin erat in, consequat mauris. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Suspendisse scelerisque auctor dictum. Maecenas cursus pellentesque nunc.</p>
      </div>
    </div>
  </div>
</body>
</html>
```

- The doctype tells the browser that the document is an HTML document.
- The `head` tag is where certain tags go that send information to the browser. The `title` tag is an example of this.
- The elements that users will see should go in the `body` tag.

## Common HTML Tags

##### Div:
- Divs are like empty rectangles.
- They help organize content on the page.

```
<div class="logo">
	My Text Inside
</div>
```

#### Heading Elements

```
<h1>Most Semantically Important Heading</h1>
<h2>...</h2>
<h3>...</h3>
<h4>...</h4>
<h5>...</h5>
<h6>Least Semantically Important Heading</h6>
```

#### Text Elements

```
<p>This is a Paragraph</p>

<strong>This is some Bold Text</strong>

<small>This is some Small Text</small>
```

#### Lists

```
<ul>
	<li>First List Item</li>
	<li>Second List Item</li>
	<li>Third List Item</li>
	<li>Fourth List Item</li>
</ul>
```

```
<ol>
	<li>First List Item</li>
	<li>Second List Item</li>
	<li>Third List Item</li>
	<li>Fourth List Item</li>
</ol>
```

#### Links

```
<a href="mylink.html">My Link</a>
```

# CSS

From [W3Schools]():

> CSS is the language for describing the presentation of Web pages, including colors, layout, and fonts. It allows one to adapt the presentation to different types of devices, such as large screens, small screens, or printers.

Check out [this example](https://www.w3schools.com/css/css_intro.asp).

CSS often goes in its own file: `style.css`. This is linked within the `head` tag:

```
<link rel="stylesheet" href="./style.css" />
```

### Selectors, declarations, and properties

From W3Schools:

![css rule](./assets/selector.gif)

- The selector points to the HTML element you want to style.
- The declaration block contains one or more declarations separated by semicolons.
- Each declaration includes a CSS property name and a value, separated by a colon.
- A CSS declaration always ends with a semicolon, and declaration blocks are surrounded by curly braces.

### Media Queries

One of the main things about modern web development -- and for that matter, modern UX design -- is the ability to make websites **responsive**. This is done using media queries.

A media query looks like this:

```css
@media screen and (min-width: 1025px) {
  /* write your declarations in here! */
}
```

It makes sense when you read it out loud, too: "Hey, media where the screen size is over 1025px..."

Responsive design is a big topic. One article I really love is by a guy named Frank Chimero, called [The Web's Grain](https://www.frankchimero.com/writing/the-webs-grain/). He describes webpages like this:

> An edgeless surface of unknown proportions comprised of small, individual, and variable elements from multiple vantages assembled into a readable whole.

The point of responsive design is to manage that reassembly in a way that benefits the user.

#### The job of a designer or developer is to structure a page so that at any given moment, no matter the size of the screen or the device of the user, the user is seeing precisely the information they need most.

# Front-End and Back-End Development

## Draw It Out
- At the end of the day, the internet is about humans and the people who use these systems, so let's start there when we think of how it all works.
- Get in to groups and think about the web. What happens when our humans fire up Chrome or Safari and type in a URL?
- Draw with as much detail as you can what you think happens between that act and finally getting the page back in the browser.

## Overview of Front-End Web Development
- Front-end web development consists of writing code in HTML, CSS, and JavaScript.
- HTML is the structure of the page. It is the scaffold that adds various layout elements to your website.
- CSS is a set of style properties that give your page its look and feel. It gives HTML style.
- JavaScript adds interactivity to your pages and makes them dynamic. Think of dropdown menus, sliding and fading boxes, dynamic content reloading, etc.

## Overview of Back-End Web Development
- The back-end is a set of tools that enable the greater functionality of the website.
- Usually included in the back-end logic is database interaction.
- Here are a few examples of back-end languages:
	- Ruby
	- PHP
	- Python
	- C++


