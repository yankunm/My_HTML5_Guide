# HTML5 Tutorial

Useful Links:
* [Mozilla Developer Network Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
* [Emmet Shortcut Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

## What is HTML5?

Hypertext MarkUp Language (HTML) describes the contents of a webpage. HTML is not a language that you download, but more of a **standard** that browsers implement. [HTML5](https://developer.mozilla.org/en-US/docs/Glossary/HTML5) refers to the latest HTML standard established in 2014, as well as some JavaScript APIs.

Given some text, HTML "marks up" (like annotating) that text using *tags* to structure and organize the webpage. 

## HTML Basic Elements

Some basic tags for annotating text:
* `<b>` - bring attention to (bold)
* `<i>` - italicize
* `<sup>` - superscript
* `<sub>` - subscript

Some basic tags for organizing text:
* `<p>` - paragraph (chunk of content)
* `<ol>` - ordered list with `<li>` list items
* `<ul>` - unordered list with `<li>` list items
* `<hr>` - thematic break (horizontal rule)
* `<br>` - line break

Header tags which should be used for *meaning (html)* not *style (css)* (good coding practice):
* `<h1>` - main header, should be only one in a page
* `<h2>, <h3>, <h4>, ...` - subheaders organized for structure not font size


Sometimes tags have *attributes*, which is information passed to a tag:
* `<a href="">` - anchor/link tag 
* `<img src="" alt="">` - image tag w/o closing

## HTML Entities

[HTML Entities](https://developer.mozilla.org/en-US/docs/Glossary/Entity) used for reserved or special characters:
* `&` can be written as  `&amp;`
* `<` can be written as `&lt;`
* `>` can be written as `&gt;`
* &#9731; can be written a `&#9731;`   

## HTML Grouping Elements

Grouping elements group together elements, which is usually for the purpose of easy CSS styling. Here it is important to distinguish between *block elements (e.g. `<p>`)* and *inline elements (e.g. `<b>`)*

* `<div>` - a block-level generic *container division* 
* `<span>` - an inline generic group

## HTML Semantic Elements

[Semantic Elements](https://developer.mozilla.org/en-US/docs/Glossary/Semantics) are tags that function exactly like divs, but they have *meaning* so it's easier to know what it points to and more friendly for screen-readers (cmd-f5). **All HTML code should be written in a way that's screen-reader friendly.**

Some common ones are:
* `<main>` - main content for a page excluding cross page contents
* `<nav>` - navigation links, breadcrumbs (show us where we are)
* `<section>` - a section of content within a page
* `<article>` - self-contained independently redistributable 
* `<aside>` - non-essential (e.g. side bar)
* `<header>` and `<footer>`
* `<time datetime=””>` - inline element for time
* `<figure>` - an illustration with caption `<figcaption>`

### Emmet Shortcuts

Emmet is what allows you to type something and press tab to generate the code. 
* `>` - child (within in tags e.g. `main>header`)
* `+` - sibling (same level e.g. `header + footer`)
* `*` - multiply (multiple times e.g. `li*5`)
* `$` - number counting from 1 (e.g. `a$*5`)
* `[]` - custom attribute (e.g. `a[href=""]`)
* `{}` - repetitive text (e.g. `a{click me!}`)

## HTML Tables

Used for rows and columns of information to display in a tabular format.

Common Table Elements:
* `<table>`
* `<tr>` - table row
* `<td>` - table data cell
* `<th>` - table header 

Table Organization:
* `<thead>` - headers
* `<tbody>` - body of a table
* `<tfoot>` - footer of a table

Common Table Attributes:
* `colspan=""` - how many columns should it occupy
* `rowspan=""` - how many rows should it occupy

## HTML Forms

This is the most useful collection of elements in HTML. Some examples are the login area of a page, the search bar. It is **a collection of interactive controls for submitting information.**

* `<form>` - a container or shell to be filled in with form controls
* `action=""` - attribute that specifies where the form should be sent

### HTTP Request and Response Cycle

When you type into a search bar (a form), an **HTTP Request** is fired off to the enpoint that `action` specifies.

The server then handles that request, or your "query", then it queries its database for whatever you typed in.

The server find the corresponding webpage, then sends it back to you as an **HTTP Response**.

Then your browser interprets and displays the contents that the server sent back for you to view.

e.g. Try it out by typing in your "query", or whatever you want to lookup, at the end of `www.reddit.com/search/?q=`

* `method=""` - attribute that specifies which HTTP Method to use (e.g. `get`, `post`)

### What goes in a form?
#### [Input](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)

* `<input>` - element used to create 20+ varieties of form controls
* `type=""` - attribute to specify what type of input we want (e.g. `text`, `password`, `color`, `number`, `checkbox`, `radio`, etc.)
* `placeholder=""` - attribute to specify the text that shows up when its empty
* `id=""` - attribute that is used for reference when labeling (unique for each input)
* `name=""` - attribute that is the "key" of this input that the server will use (corresponding to user input "value")

The **name attribute is crucial**, because when the data is sent it will be labeled using that name.

Note: `id` is the reference this input element, `name` is the reference for the data in this input element. 

#### [Label](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label)

Interactive text label for input crucial for accessibility.

* `<label>` - element to associate some input with some piece of text (link text and input)
* `for=""` - attribute to specify which input this links to (the "id" of the input)
* `<input id="">` - attribute *id* is used for linking on the input side (it should be unique per input)

Note: Usually Labels and Inputs are siblings

#### [Buttons](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button)

* `<button>` - the default action of button inside form is to submit the form (i.e. `type="submit"`)
* `type=""` - attribute that specifies what type of button it is (e.g. `button`, `submit`)

#### More Inputs

Some other common inputs are:
* `type="checkbox"` - this is a checkbox where you can also add attribute `checked` to make it intially checked
* `type="radio"` - this is a select one and only one checkbox 

Note: if you have multiple radio options with same `name` (same group), you have to specify not only `name` but also `value=""` so the server knows "what is on".

* `type="range"` - Slide Bar with attributes `min=""` and `max=""`, also can give `step=""` (which is by default `step="1"`) and `value=""`, which is the initial value (these attributes also work with `type="number"`)

Other common tags that are also inputs are:

* `<select>` with multiple `<option>` - Drop down menu
* `<textarea>` - Textbox where the user can input text








 











