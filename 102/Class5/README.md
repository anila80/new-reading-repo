# What is CSS?
CSS (Cascading Style Sheets) allows you to create great-looking web pages, but how does it work under the hood? 

## What is CSS for?
CSS is a language for specifying how documents are presented to users — how they are styled, laid out, etc.

A document is usually a text file structured using a markup language — HTML is the most common markup language, but you may also come across other markup languages such as SVG or XML.

**Presenting** a document to a user means converting it into a form usable by your audience. Browsers, like Firefox, Chrome, or Edge, are designed to present documents visually, for example, on a computer screen, projector, or printer.

CSS can be used for very basic document text styling — for example, for changing the color and size of headings and links. It can be used to create a layout — for example, turning a single column of text into a layout with a main content area and a sidebar for related information. It can even be used for effects such as animation. Have a look at the links in this paragraph for specific examples.

***CSS syntax:***
CSS is a rule-based language — you define the rules by specifying groups of styles that should be applied to particular elements or groups of elements on your web page.

For example, you can decide to have the main heading on your page to be shown as large red text. The following code shows a very simple CSS rule that would achieve the styling described above:

h1 {
  color: red;
  font-size: 5em;
}

## Starting with some HTML
Our starting point is an HTML document. You can copy the code from below if you want to work on your own computer. Save the code below as index.html in a folder on your machine.

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Getting started with CSS</title>
  </head>

  <body>
    <h1>I am a level one heading</h1>

    <p>
      This is a paragraph of text. In the text is a
      <span>span element</span> and also a
      <a href="https://example.com">link</a>.
    </p>

    <p>
      This is the second paragraph. It contains an <em>emphasized</em> element.
    </p>

    <ul>
      <li>Item <span>one</span></li>
      <li>Item two</li>
      <li>Item <em>three</em></li>
    </ul>
  </body>
</html>



Note: If you are reading this on a device or an environment where you can't easily create files, then don't worry — live code editors are provided below to allow you to write example code right here in the page.

## Adding CSS to our document

The very first thing we need to do is to tell the HTML document that we have some CSS rules we want it to use. There are three different ways to apply CSS to an HTML document that you'll commonly come across, however, for now, we will look at the most usual and useful way of doing so — linking CSS from the head of your document.

Create a file in the same folder as your HTML document and save it as styles.css. The .css extension shows that this is a CSS file.

To link styles.css to index.html, add the following line somewhere inside the <head> of the HTML document:

<link rel="stylesheet" href="styles.css" />

This <link> element tells the browser that we have a stylesheet, using the rel attribute, and the location of that stylesheet as the value of the href attribute. You can test that the CSS works by adding a rule to styles.css. Using your code editor, add the following to your CSS file:

h1 {
  color: red;
}
Copy to Clipboard
Save your HTML and CSS files and reload the page in a web browser. The level one heading at the top of the document should now be red. If that happens, congratulations — you have successfully applied some CSS to an HTML document. If that doesn't happen, carefully check that you've typed everything correctly.

You can continue to work in styles.css locally, or you can use our interactive editor below to continue with this tutorial. The interactive editor acts as if the CSS in the first panel is linked to the HTML document, just as we have with our document above.

Styling HTML elements
By making our heading red, we have already demonstrated that we can target and style an HTML element. We do this by targeting an element selector — this is a selector that directly matches an HTML element name. To target all paragraphs in the document, you would use the selector p. To turn all paragraphs green, you would use:

p {
  color: green;
}
Copy to Clipboard
You can target multiple selectors at the same time by separating the selectors with a comma. If you want all paragraphs and all list items to be green, your rule would look like this:

p,
li {
  color: green;
}
Copy to Clipboard
Try this out in the interactive editor below (edit the code boxes) or in your local CSS document.


Changing the default behavior of elements
When we look at a well-marked up HTML document, even something as simple as our example, we can see how the browser is making the HTML readable by adding some default styling. Headings are large and bold and our list has bullets. This happens because browsers have internal stylesheets containing default styles, which they apply to all pages by default; without them all of the text would run together in a clump and we would have to style everything from scratch. All modern browsers display HTML content by default in pretty much the same way.

However, you will often want something other than the choice the browser has made. This can be done by choosing the HTML element that you want to change and using a CSS rule to change the way it looks. A good example is <ul>, an unordered list. It has list bullets. If you don't want those bullets, you can remove them like so:

li {
  list-style-type: none;
}
Copy to Clipboard
Try adding this to your CSS now.

The list-style-type property is a good property to look at on MDN to see which values are supported. Take a look at the page for list-style-type and you will find an interactive example at the top of the page to try some different values in, then all allowable values are detailed further down the page.

Looking at that page you will discover that in addition to removing the list bullets, you can change them — try changing them to square bullets by using a value of square.

Adding a class
So far, we have styled elements based on their HTML element names. This works as long as you want all of the elements of that type in your document to look the same. To select a subset of the elements without changing the others, you can add a class to your HTML element and target that class in your CSS.

In your HTML document, add a class attribute to the second list item. Your list will now look like this:
<ul>
  <li>Item one</li>
  <li class="special">Item two</li>
  <li>Item <em>three</em></li>
</ul>
Copy to Clipboard
In your CSS, you can target the class of special by creating a selector that starts with a full stop character. Add the following to your CSS file:
.special {
  color: orange;
  font-weight: bold;
}
Copy to Clipboard
Save and refresh to see what the result is.
You can apply the class of special to any element on your page that you want to have the same look as this list item. For example, you might want the <span> in the paragraph to also be orange and bold. Try adding a class of special to it, then reload your page and see what happens.

Sometimes you will see rules with a selector that lists the HTML element selector along with the class:

li.special {
  color: orange;
  font-weight: bold;
}
Copy to Clipboard
This syntax means "target any li element that has a class of special". If you were to do this, then you would no longer be able to apply the class to a <span> or another element by adding the class to it; you would have to add that element to the list of selectors:

li.special,
span.special {
  color: orange;
  font-weight: bold;
}
Copy to Clipboard
As you can imagine, some classes might be applied to many elements and you don't want to have to keep editing your CSS every time something new needs to take on that style. Therefore, it is sometimes best to bypass the element and refer to the class, unless you know that you want to create some special rules for one element alone, and perhaps want to make sure they are not applied to other things.

Styling things based on their location in a document
There are times when you will want something to look different based on where it is in the document. There are a number of selectors that can help you here, but for now we will look at just a couple. In our document, there are two <em> elements — one inside a paragraph and the other inside a list item. To select only an <em> that is nested inside an <li> element, you can use a selector called the descendant combinator, which takes the form of a space between two other selectors.

Add the following rule to your stylesheet:

li em {
  color: rebeccapurple;
}
Copy to Clipboard
This selector will select any <em> element that is inside (a descendant of) an <li>. So in your example document, you should find that the <em> in the third list item is now purple, but the one inside the paragraph is unchanged.

Something else you might like to try is styling a paragraph when it comes directly after a heading at the same hierarchy level in the HTML. To do so, place a + (an adjacent sibling combinator) between the selectors.

Try adding this rule to your stylesheet as well:

h1 + p {
  font-size: 200%;
}

## Styling things based on state
The final type of styling we shall take a look at in this tutorial is the ability to style things based on their state. A straightforward example of this is when styling links. When we style a link, we need to target the <a> (anchor) element. This has different states depending on whether it is unvisited, visited, being hovered over, focused via the keyboard, or in the process of being clicked (activated). You can use CSS to target these different states — the CSS below styles unvisited links pink and visited links green.

a:link {
    color: pink;
}

a:visited {
  color: green;
}

You can change the way the link looks when the user hovers over it, for example by removing the underline, which is achieved by the next rule:

a:hover {
  text-decoration: none;
}

## Interactive editor

a:link {
    color: pink;
}

a:visited {
    color: green;
}

a:hover {
    text-decoration: none;
}


## Combining selectors and combinators
It is worth noting that you can combine multiple selectors and combinators together. For example:

/* selects any <span> that is inside a <p>, which is inside an <article>  */
article p span {
}

/* selects any <p> that comes directly after a <ul>, which comes directly after an <h1>  */
h1 + ul + p {
}

You can combine multiple types together, too. Try adding the following into your code:

body h1 + p .special {
  color: yellow;
  background-color: black;
  padding: 5px;
}


# How to Add CSS

Example:
<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" href="mystyle.css">
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>

An external style sheet can be written in any text editor, and must be saved with a .css extension.

The external .css file should not contain any HTML tags.

Here is how the "mystyle.css" file looks:

"mystyle.css"

body {
  background-color: lightblue;
}

h1 {
  color: navy;
  margin-left: 20px;
}

Note: Do not add a space between the property value and the unit:
Incorrect (space): margin-left: 20 px;
Correct (nospace): margin-left: 20px;

