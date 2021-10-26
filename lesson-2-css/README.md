# CSS Intro

CSS is the language we use to style a Web page. CSS stands for Cascading Style Sheets. It describes how HTML elements are to be displayed on screen, paper, or in other media. HTML was NEVER intended to contain tags for formatting a web page! HTML was created to describe the content of a web page, like:

```
<h1>This is a heading</h1>

<p>This is a paragraph.</p>
```

When tags like `<font>`, and color attributes were added to the HTML 3.2 specification, it started a nightmare for web developers. Development of large websites, where fonts and color information were added to every single page, became a long and expensive process. To solve this problem, the World Wide Web Consortium (W3C) created CSS. CSS removed the style formatting from the HTML page!

# Syntax

A CSS rule consists of a selector and a declaration block.
![CSS selector](https://www.w3schools.com/css/img_selector.gif)

The selector points to the HTML element you want to style.

The declaration block contains one or more declarations separated by semicolons.

Each declaration includes a CSS property name and a value, separated by a colon.

Multiple CSS declarations are separated with semicolons, and declaration blocks are surrounded by curly braces.

```
p {
color: blue;
text-align: center;
}
```

- `p` is a selector in CSS (it points to the HTML element you want to style: <p>).
- `color` is a property, and `blue` is the property value
- `text-align` is a property, and `center` is the property value

# CSS Selectors

A CSS selector selects the HTML element(s) you want to style.
CSS selectors are used to "find" (or select) the HTML elements you want to style.

We can divide CSS selectors into five categories:

- Simple selectors (select elements based on name, id, class)
- Combinator selectors (select elements based on a specific relationship between them)
- Pseudo-class selectors (select elements based on a certain state)
- Pseudo-elements selectors (select and style a part of an element)
- Attribute selectors (select elements based on an attribute or attribute value)

## Element Selector

The element selector selects HTML elements based on the element name.

Here, all `<p>` elements on the page will be center-aligned, with a blue text color.

```
p {
text-align: center;
color: blue;
}
```

## ID Selector

The id selector uses the id attribute of an HTML element to select a specific element. The id of an element is unique within a page, so the id selector is used to select one unique element! To select an element with a specific id, write a hash (#) character, followed by the id of the element.

The CSS rule below will be applied to the HTML element with id="first-paragraph"

```
#first-paragraph {
text-align: center;
color: green;
}
```

## Class Selector

The class selector selects HTML elements with a specific class attribute. To select elements with a specific class, write a period (.) character, followed by the class name.

In this example all HTML elements with class="center" will be green and center-aligned.

```
.green-paragraph {
text-align: center;
color: green;
}
```

## Universal Selector

The universal selector (\*) selects all HTML elements on the page.

The CSS rule below will affect every HTML element on the page.

```
* {
text-align: center;
color: blue;
}
```

# How to Add CSS

When a browser reads a style sheet, it will format the HTML document according to the information in the style sheet.

## Three Ways to Insert CSS

There are three ways of inserting a style sheet:

- Inline CSS
- Internal CSS
- External CSS

## Inline CSS

An inline style may be used to apply a unique style for a single element.

To use inline styles, add the style attribute to the relevant element. The style attribute can contain any CSS property.

```
<p style="color:red;">This is a paragraph.</p>
```

> **Tip:** An inline style loses many of the advantages of a style sheet (by mixing content with presentation and lack of re-use since they are written in the html element). Use this method sparingly.

## Internal CSS

An internal style sheet may be used if one single HTML page has a unique style.

The internal style is defined inside the `<style>` element, inside the head section.

```
<head>
<style>
body  {
background-color:  yellow;
}

h1  {
color:  blue;
}
</style>
</head>
```

> **Tip:** These styles are only available on the page you add them on.

## External CSS

With an external style sheet, you can change the look of an entire website by changing just one file!

Each HTML page must include a reference to the external style sheet file inside the `<link>` element, inside the head section.

```
<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" href="workshop.css" />
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```

workshop.css

```
body {
background-color:  lightblue;
}

h1 {
color:  navy;
}
```

# Comments

CSS comments are not displayed in the browser, but they can help document your source code.

Comments are used to explain the code, and may help when you edit the source code at a later date.

Comments are ignored by browsers.

A CSS comment is placed inside the `<style>` element, and starts with `/*` and ends with `*/`:

```
/* This is a single-line comment */
p {
color:  red;
}
```

# CSS Colors

Colors are specified using predefined color names, or RGB, HEX, HSL, etc.

## RGB Value

An RGB color value represents RED, GREEN, and BLUE light sources.

In CSS, a color can be specified as an RGB value, using this formula:

rgb(_red,_ _green_, _blue_)

Each parameter (red, green, and blue) defines the intensity of the color between 0 and 255.

For example, rgb(255, 0, 0) is displayed as red, because red is set to its highest value (255) and the others are set to 0.

To display black, set all color parameters to 0, like this: rgb(0, 0, 0).

To display white, set all color parameters to 255, like this: rgb(255, 255, 255).

## HEX Value

A hexadecimal color is specified with: #RRGGBB, where the RR (red), GG (green) and BB (blue) hexadecimal integers specify the components of the color.

In CSS, a color can be specified using a hexadecimal value in the form:

#_rrggbb_

Where rr (red), gg (green) and bb (blue) are hexadecimal values between 00 and ff (same as decimal 0-255).

For example, #ff0000 is displayed as red, because red is set to its highest value (ff) and the others are set to the lowest value (00).

To display black, set all values to 00, like this: #000000.

To display white, set all values to ff, like this: #ffffff.

## HSL Value

HSL stands for hue, saturation, and lightness.

In CSS, a color can be specified using hue, saturation, and lightness (HSL) in the form:

hsl(_hue_, _saturation_, _lightness_)

Hue is a degree on the color wheel from 0 to 360. 0 is red, 120 is green, and 240 is blue.

Saturation is a percentage value, 0% means a shade of gray, and 100% is the full color.

Lightness is also a percentage, 0% is black, 50% is neither light or dark, 100% is white

# Backgrounds

## Background Color

The `background-color` property specifies the background color of an element.

```
body {
background-color:  lightblue;
}
```

## Background Image

The `background-image` property specifies an image to use as the background of an element.

By default, the image is repeated so it covers the entire element.

```
body {
background-image:  url("landscape.jpg");
}
```

# Borders

The CSS border properties allow you to specify the style, width, and color of an element's border.

## CSS Border Style

The `border-style` property specifies what kind of border to display.

The following values are allowed:

- `dotted` - Defines a dotted border
- `dashed` - Defines a dashed border
- `solid` - Defines a solid border
- `double` - Defines a double border
- `groove` - Defines a 3D grooved border. The effect depends on the border-color value
- `ridge` - Defines a 3D ridged border. The effect depends on the border-color value
- `inset` - Defines a 3D inset border. The effect depends on the border-color value
- `outset` - Defines a 3D outset border. The effect depends on the border-color value
- `none` - Defines no border
- `hidden` - Defines a hidden border

The `border-style` property can have from one to four values (for the top border, right border, bottom border, and the left border).

```
p {
border:  2px solid red;
}
```

## CSS Rounded Borders

The `border-radius` property is used to add rounded borders to an element:

```
p {
border:  2px solid red;
border-radius:  5px;
}
```

# Margins

Margins are used to create space around elements, outside of any defined borders.

## CSS Margins

The CSS `margin` properties are used to create space around elements, outside of any defined borders.

With CSS, you have full control over the margins. There are properties for setting the margin for each side of an element (top, right, bottom, and left).

All the margin properties can have the following values:

- auto - the browser calculates the margin
- _length_ - specifies a margin in px, pt, cm, etc.
- _%_ - specifies a margin in % of the width of the containing element
- inherit - specifies that the margin should be inherited from the parent element

> **Tip:** Negative values are allowed.

## Margin - Individual Sides

CSS has properties for specifying the margin for each side of an element:

- `margin-top`
- `margin-right`
- `margin-bottom`
- `margin-left`

```
p {
margin-top:  100px;
margin-bottom:  100px;
margin-right:  150px;
margin-left:  80px;
}
```

# Padding

Padding is used to create space around an element's content, inside of any defined borders.

## CSS Padding

The CSS `padding` properties are used to generate space around an element's content, inside of any defined borders.

With CSS, you have full control over the padding. There are properties for setting the padding for each side of an element (top, right, bottom, and left).

## Padding - Individual Sides

CSS has properties for specifying the padding for each side of an element:

- `padding-top`
- `padding-right`
- `padding-bottom`
- `padding-left`

All the padding properties can have the following values:

- _length_ - specifies a padding in px, pt, cm, etc.
- _%_ - specifies a padding in % of the width of the containing element
- inherit - specifies that the padding should be inherited from the parent element

> **Note:** Negative values are not allowed.

```
div {
padding-top:  50px;
padding-right:  30px;
padding-bottom:  50px;
padding-left:  80px;
}
```

# Fonts

Choosing the right font for your website is important!

## Font Selection is Important

Choosing the right font has a huge impact on how the readers experience a website.

The right font can create a strong identity for your brand.

Using a font that is easy to read is important. The font adds value to your text. It is also important to choose the correct color and text size for the font.

## Generic Font Families

In CSS there are five generic font families:

1.  **Serif** fonts have a small stroke at the edges of each letter. They create a sense of formality and elegance.
2.  **Sans-serif** fonts have clean lines (no small strokes attached). They create a modern and minimalistic look.
3.  **Monospace** fonts - here all the letters have the same fixed width. They create a mechanical look.
4.  **Cursive** fonts imitate human handwriting.
5.  **Fantasy** fonts are decorative/playful fonts.

All the different font names belong to one of the generic font families.

## Difference Between Serif and Sans-serif Fonts

![Serif vs. Sans-serif](https://www.w3schools.com/css/serif.gif)

> **Note:** On computer screens, sans-serif fonts are considered easier to read than serif fonts.

## The CSS font-family Property

In CSS, we use the `font-family` property to specify the font of a text.

The `font-family` property should hold several font names as a "fallback" system, to ensure maximum compatibility between browsers/operating systems. Start with the font you want, and end with a generic family (to let the browser pick a similar font in the generic family, if no other fonts are available). The font names should be separated with comma.

> **Note**: If the font name is more than one word, it must be in quotation marks, like: "Times New Roman".

```
.p1 {
font-family:  "Times New Roman", Times, serif;
}

.p2 {
font-family:  Arial, Helvetica, sans-serif;
}

.p3 {
font-family:  "Lucida Console", "Courier New", monospace;
}
```

## Font Style

The `font-style` property is mostly used to specify italic text.

This property has three values:

- normal - The text is shown normally
- italic - The text is shown in italics
- oblique - The text is "leaning" (oblique is very similar to italic, but less supported)

```
p.normal {
font-style:  normal;
}

p.italic {
font-style:  italic;
}

p.oblique {
font-style:  oblique;
}
```

## Font Weight

The `font-weight` property specifies the weight of a font:

```
p.normal {
font-weight:  normal;
}

p.thick {
font-weight:  bold;
}
```

## Font Size

The `font-size` property sets the size of the text.

Being able to manage the text size is important in web design. However, you should not use font size adjustments to make paragraphs look like headings, or headings look like paragraphs.

Always use the proper HTML tags, like <h1> - <h6> for headings and <p> for paragraphs.

The font-size value can be an absolute, or relative size.

Absolute size:

- Sets the text to a specified size
- Does not allow a user to change the text size in all browsers (bad for accessibility reasons)
- Absolute size is useful when the physical size of the output is known

Relative size:

- Sets the size relative to surrounding elements
- Allows a user to change the text size in browsers

> **Note:** If you do not specify a font size, the default size for normal text, like paragraphs, is 16px (16px=1em).

## Set Font Size With Pixels

Setting the text size with pixels gives you full control over the text size:

```
h1 {
font-size:  40px;
}

h2 {
font-size:  30px;
}

p {
font-size:  14px;
}
```
