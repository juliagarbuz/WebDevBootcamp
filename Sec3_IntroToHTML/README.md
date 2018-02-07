# Section 3 – Intro to HTML (Notes)

## TABLE OF CONTENTS:
| # | Lecture |
| :------: | :---------------------------------------- |
| 14 | [HTML Basics](#html-basics-lecture-14)   |
| 15 | [Intro to MDN](#intro-to-mdn-lecture-15) |
| 16 | Note about Introduction to MDN |
| 17 | [HTML Boilerplate and Comments](#html-boilerplate-and-comments-lecture-17) |
| 18 | [Basic Tags](#basic-tags-lecture-18) |
| 19 | [HTML Lists](#html-lists-lecture-19) |
| 20 | HTML Lists Assignment ([quiz1.html](/Sec3_IntroToHTML/quiz1.html)) |
| 21 | HTML Lists Assignment: SOLUTION |
| 22 | [Divs and Spans](#divs-and-spans-lecture-22) |
| 23 | [HTML Attributes](#html-attributes-lecture-23) |
| 24 | Recreate Webpage Assignment ([rusty.html](/Sec3_IntroToHTML/rusty.html)) |
| 25 | Recreate Webpage Assignment: SOLUTION |
| - | GO TO [Section 4 - Intermediate HTML](/Sec4_IntermediateHTML/notes.md) |

## HTML Basics _(Lecture 14)_:
- **HTML** = "_hyper text markup language_"
- History:
  - Created in 1989/1990
  - Allowed for publishing and exchanging of scientific and technical documents (with consistent style/formatting)
- **HTML** is the **CONTENT** ("_nouns_") of a webpage
- allows electronic linking of documents (via "_hyperlinks_")
- **General rule:** "sandwich" content between opening and closing tags: `<tagName> Some Content </tagName>`
  - Tag examples:
      1) Headings: `<h1>ABSTRACT</h1>`
      2) Bold: `<b>Function</b>:`
      3) Paragraph: `<p> The question is whether... </p>`

## Intro to MDN _(Lecture 15)_:
- **MDN** = "[Mozilla Developer Network](https://developer.mozilla.org/)"
  - A resource for HTML, CSS, Javascript

## HTML Boilerplate and Comments _(Lecture 17)_:
- Every HTML document we create will start with this **boilerplate**:
  ```HTML
  <!-- HTML BOILERPLATE: -->
  <!DOCTYPE html>
  <html>
    <head>
      <!-- Our metadata goes here -->
      <title></title>
    </head>
    <body>
      <!-- Our content goes here -->
    </body>
  </html>
  ```
  - typing `html` and then hitting _tab_ in text editor automatically adds "boilerplate"
  - **`<!DOCTYPE>`** = indicates you are using HTML5
  - **`<html>`** = indicates root of an html document (all other elements must be descendants of this element)
    - _everything we write must go inside HTML root element_
    - Permitted content: one head element followed by one body element
  - **`<head>`** = provides general information (metadata) about document including title and links to or definition of scripts and style sheets
    - _everything you don't see on the page as a user goes here, while body is the content_
  - **`<body>`** = represents the content of an HTML document
  - **`<title>`** determines title on tab and important for search engines
- **Comments**: `<!-- This is a comment. It doesn't do anything! -->`
   - hitting _cmd-'/'_ while cursor on line (or while block is highlighted) will automatically comment it out

## Basic Tags _(Lecture 18)_:
- [MDN Element Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) = list of all elements in HTML
- Common tags _cheat-sheet_:
  ```HTML
  <!-- Common tags overview: -->
  <h1>I'm a header</h1>
  <h2>I'm a slightly smaller header</h2>
  <h6>I'm the smallest header</h6>

  <p>I'm a paragraph</p>

  <button>I'm a button!</button>

  <ul>
      <li>List Item 1</li>
      <li>List Item 2</li>
  </ul>

  <ol>
      <li>List Item 1</li>
      <li>List Item 2</li>
  </ol>
  ```
    - **Block-level element** = each will be on its own line  
      - **`<h1>` - `<h6>`** = six levels of document headings _(h1 is most important/largest, h6 is least important/smallest heading)_  
      - **`<p>`** = used to represent paragraphs or text, considered block-level element
    - **In-line element** = will not force element to new line  
      - **`<b>`** = bolded (_**NOTE**: not the best way of bolding_)
        - recommended to use **`<strong>`** (_bc of "semantic markup" -> giving meaning and separating styling from structure_)  
      - **`<i>`** = italicized (_**NOTE**: not the best way of italicizing)
        - recommended to use **`<em>`** = "emphasis" (_bc of "semantic markup" again_)

## HTML Lists _(Lecture 19)_:
- Two types of lists:
  - *Ordered list*: `<or>`
  - *Unordered list*: `<ul>`
- both require *list items* to actually create list: `<li>`
  ```HTML  
  <!-- nested ordered/unordered lists example: -->
  <h4>My Color List</h4>
  <ol>
    <li><strong>Red</strong></li>
    <li>Orange</li>
    <li>Yellow
      <ul>
        <li>Sunflower</li>
        <li>Banana</li>
      </ul>
    </li>
  </ol>
  ```
- type tag name (without <>) and hit _tab_ to autocomplete open/close

## Divs and Spans _(Lecture 22)_:
- **`<div>` and `<span>`** = allow you to group content together
  - **`<div>`** = generic container (_block level element_)
    ```HTML
    <!-- div example: -->
    <div>
      <h1>H1 is part of div</h1>
      <p>Paragraph 1 is part of div</p>
    </div>
    This is not part of the div
    ```
    - _block level element_ means that if you were to include a div in the middle of the `<p>`, that portion would begin on a new line
  - **`<span>`** = also a generic container (_in-line element_)
      - used for grouping "in-line" content

## HTML Attributes _(Lecture 23)_:
- [MDN Attribute Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes) = list of all attributes in HTML
- **attributes** add additional information to tags (in form of key/value pairs)
  - FORMAT: `<tag name="value"></tag>`
  ```HTML
  <!-- Attribute overview: -->
  <img src="corgi.png">
  <p class="selected">woof woof</p>
  <a href="www.google.com">Click me to go to Google</a>
  <link rel="stylesheet" type="text/css" href="style.css">
  ```
  - not all attributes work on all elements (_often they only work on 2-5, some only on 1_)
  - **`src=""`** attribute with `<img>`/_image_ tag: `<img src="img_path">`
    ```HTML
    <!-- src attribute example: -->
    <img src="corgi.png">
    ```
    - self closing (does not need closing tag)
  - **`href=""`** attribute (with `<a>`/_anchor_ tag): `<a href="url">Link this text</a>`
    ```HTML
    <!-- href attribute example: -->
    <a href="http://www.google.com">Click this to go to Google</a>
    <a href="page2.html">Click to go to page2.html</a>
    ```
    - **`<a>`** is an _in-line element_
    - make sure links to external sites (not from local files) use **HTTP protocol**: `http://url-here`
    - use **relative paths** to link to other pages in same directory

## NEXT SECTION: Section 4 - Intermediate HTML
GO TO [Section 4 - Intermediate HTML](/Sec4_IntermediateHTML/notes.md)
