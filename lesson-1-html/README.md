# HTML Intro

HTML stands for Hyper Text Markup Language and is the standard markup language for Web pages. It allows us to describe the structure of a Web page through a series of elements that tell the browser how to display the content. With HTML you can create your own Website.

https://dev.to -> Right click and select View Page Source

# Web Browsers

The purpose of a web browser (Chrome, Edge, Firefox, Safari) is to read HTML documents and display them correctly. A browser does not display the HTML tags, but uses them to determine how to display the document.

# Text Editors

Notepad, Text Edit, Visual Studio Code
Cloud based environments - CodeSandbox, Stackblitz, AWS Cloud 9

# HTML Basics

index.html is a special file name that when placed at the root of the folder the browser will interpret that as the home page.

## HTML Element

An HTML element is defined by a start tag, some content, and an end tag:

```
<tagname>Content goes here...</tagname>
```

The HTML **element** is everything from the start tag to the end tag:

```
<h1>My First Heading</h1>
```

| Start tag | Element content  | End tag |
| --------- | ---------------- | ------- |
| `<h1>`    | My First Heading | `</h1>` |
| `<br>`    | none             | none    |

> **Note:** Some HTML elements have no content (like the `<br>` element). These elements are called empty elements. Empty elements do not have an end tag!

## HTML Attributes

HTML attributes provide additional information about HTML elements. Attributes are always specified in **the start tag** and usually come in name/value pairs like: **name="value"**

### The src Attribute

The `<img>` tag is used to embed an image in an HTML page. The `src` attribute specifies the path to the image to be displayed.

```
<img src="img_girl.jpg">
```

### The href Attribute

The `<a>` tag defines a hyperlink. The `href` attribute specifies the URL of the page the link goes to.

```
<a href="https://www.google.com">Search!</a>
```

### The width and height Attributes

The `<img>` tag should also contain the `width` and `height` attributes, which specifies the width and height of the image (in pixels).

```
<img src="img_girl.jpg"  width="500"  height="600">
```

Now that we understand a little more about the building blocks of a web page, let's begin building the basic skeleton that every html page has.

## DOCTYPE

```
<!DOCTYPE html>
<html>
<head>
<title>Title of the document</title>
</head>

<body>
The content of the document......
</body>
</html>
```

All HTML documents must start with a `<!DOCTYPE>` declaration.

The declaration is not an HTML tag. It is an "information" to the browser about what document type to expect.

In HTML 5, the declaration is simple:

```
<!DOCTYPE html>
```

## html

The `<html>` tag represents the root of an HTML document. The `<html>` tag is the container for all other HTML elements.

## head

The `<head>` element is a container for metadata (data about data) and is placed between the `<html>` tag and the `<body>` tag. Metadata is data about the HTML document. Metadata is not displayed. Metadata typically define the document title, character set, styles, scripts, and other meta information.

## body

The `<body>` tag defines the document's body. The `<body>` element contains all the contents of an HTML document, such as headings, paragraphs, images, hyperlinks, tables, lists, etc.

## title

The `<title>` tag defines the title of the document. The title must be text-only, and it is shown in the browser's title bar or in the page's tab. The `<title>` tag is required in HTML documents! The contents of a page title is very important for search engine optimization (SEO)! The page title is used by search engine algorithms to decide the order when listing pages in search results.

## <!-- >

The comment tag is used to insert comments in the source code. Comments are not displayed in the browsers. You can use comments to explain your code, which can help you when you edit the source code at a later date. This is especially useful if you have a lot of code.

> **Note:** Notice the indentation on the head and body tags inside the html tags. A general rule of thumb is to indent any tags that inside other tags.

> **Note:** Developers may reference elements using familial terminology. For example, the `<html>` tag is a parent of the `<head>` tag or the `<title>` tag is a grandchild of the `<html>` tag.

## headings

HTML headings are titles or subtitles that you want to display on a webpage. HTML headings are defined with the `<h1>` to `<h6>` tags. `<h1>` defines the most important heading. `<h6>` defines the least important heading.

## paragraph

The `<p>` tag defines a paragraph. Browsers automatically add a single blank line before and after each `<p>` element.

## line break

The `<br>` tag inserts a single line break. The `<br>` tag is an empty tag which means that it has no end tag.

## lists

The `<ol>` tag defines an ordered list. An ordered list can be numerical or alphabetical.

The `<ul>` tag defines an unordered (bulleted) list.

The `<li>` tag defines a list item. The `<li>` tag is used inside ordered lists `<ol>`, unordered lists `<ul>`, and in menu lists `<menu>`. In `<ul>` and `<menu>`, the list items will usually be displayed with bullet points. In `<ol>`, the list items will usually be displayed with numbers or letters.

## links

Links are found in nearly all web pages. Links allow users to click their way from page to page.

> **Note:** A link does not have to be text. A link can be an image or any other HTML element!

The HTML `<a>` tag defines a hyperlink. It has the following syntax:

`<a href="url">link text</a>`

The most important attribute of the `<a>` element is the `href` attribute, which indicates the link's destination. The _link text_ is the part that will be visible to the reader. Clicking on the link text, will send the reader to the specified URL address.

```
<a href="https://www.google.com/">Search!</a>
```

By default, links will appear as follows in all browsers:

- An unvisited link is underlined and blue
- A visited link is underlined and purple
- An active link is underlined and red

> **Tip:** Links can of course be styled with CSS, to get another look!

By default, the linked page will be displayed in the current browser window. To change this, you must specify another target for the link.

The `target` attribute specifies where to open the linked document.

The `target` attribute can have one of the following values:

- `_self` - Default. Opens the document in the same window/tab as it was clicked
- `_blank` - Opens the document in a new window or tab
- `_parent` - Opens the document in the parent frame
- `_top` - Opens the document in the full body of the window

```
<a href="https://www.google.com/" target="_blank">Search!</a>
```

### Absolute URLs vs. Relative URLs

Both examples above are using an **absolute URL** (a full web address) in the `href` attribute.

A local link (a link to a page within the same website) is specified with a **relative URL** (without the "https://www" part):

```
<p><a href="/hello.html">Hello</a></p>
```

### Link to an Email Address

Use `mailto:` inside the `href` attribute to create a link that opens the user's email program (to let them send a new email):

```
<a href="mailto:someone@example.com">Send email</a>
```

## images

Images can improve the design and the appearance of a web page. The HTML `<img>` tag is used to embed an image in a web page. Images are not technically inserted into a web page; images are linked to web pages. The `<img>` tag creates a holding space for the referenced image.

The `<img>` tag is empty, it contains attributes only, and does not have a closing tag.

The `<img>` tag has two required attributes:

- src - Specifies the path to the image
- alt - Specifies an alternate text for the image

### The src Attribute

The required `src` attribute specifies the path (URL) to the image.

> **Note:** When a web page loads, it is the browser, at that moment, that gets the image from a web server and inserts it into the page. Therefore, make sure that the image actually stays in the same spot in relation to the web page, otherwise your visitors will get a broken link icon. The broken link icon and the `alt` text are shown if the browser cannot find the image.

### The alt Attribute

The required `alt` attribute provides an alternate text for an image, if the user for some reason cannot view it (because of slow connection, an error in the src attribute, or if the user uses a screen reader).

The value of the `alt` attribute should describe the image:

```
<img src="images/headshot.jpg"  alt="Michelle Lewis Profile">
```

## block and inline

Every HTML element has a default display value, depending on what type of element it is. There are two display values: block and inline.

### Block-level Elements

A block-level element always starts on a new line. A block-level element always takes up the full width available (stretches out to the left and right as far as it can). A block level element has a top and a bottom margin, whereas an inline element does not.
`<p>`
`<ol>`

### Inline Elements

An inline element does not start on a new line. An inline element only takes up as much width as necessary.
`<a>`
`<img>`

### The `<div>` Element

The `<div>` element is often used as a container for other HTML elements. The `<div>` element has no required attributes, but `style`, `class` and `id` are common. When used together with CSS, the `<div>` element can be used to style blocks of content.

```
<div style="background-color:black;color:white;padding:20px;">
<h2>London</h2>
<p>London is the capital city of England. It is the most populous city in the United Kingdom, with a metropolitan area of over 13 million inhabitants.</p>
</div>
```

## layout

Websites often display content in multiple columns (like a magazine or a newspaper).

### HTML Layout Elements

HTML has several semantic elements that define the different parts of a web page:

![HTML5 Semantic Elements](https://www.w3schools.com/html/img_sem_elements.gif)

- `<header>` - Defines a header for a document or a section
- `<nav>` - Defines a set of navigation links
- `<section>` - Defines a section in a document
- `<article>` - Defines an independent, self-contained content
- `<aside>` - Defines content aside from the content (like a sidebar)
- `<footer>` - Defines a footer for a document or a section
- `<details>` - Defines additional details that the user can open and close on demand
- `<summary>` - Defines a heading for the `<details>` element

### Section

The `<section>` tag defines a section in a document.

```
<section>
<h2>WWF History</h2>
<p>The World Wide Fund for Nature (WWF) is an international organization working on issues regarding the conservation, research and restoration of the environment, formerly named the World Wildlife Fund. WWF was founded in 1961.</p>
</section>

<section>
<h2>WWF's Symbol</h2>
<p>The Panda has become the symbol of WWF. The well-known panda logo of WWF originated from a panda named Chi Chi that was transferred from the Beijing Zoo to the London Zoo in the same year of the establishment of WWF.</p>
</section>
```

### Footer

The `<footer>` tag defines a footer for a document or section. A `<footer>` element typically contains:

- authorship information
- copyright information
- contact information
- sitemap
- back to top links
- related documents

```
<footer>
<p>Author: Someone</p>
<p><a href="mailto:someone@example.com">someone@example.com</a></p>
</footer>
```

## button

The `<button>` tag defines a clickable button.

> **Tip:** Always specify the `type` attribute for a `<button>` element, to tell browsers what type of button it is.

A few attributes:
Type (button , reset, submit) - Specifies the type of button
Disabled - Specifies that a button should be disabled
Form - Specifies which form the button belongs to
