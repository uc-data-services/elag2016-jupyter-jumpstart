
# Markdown 101: Lesson Goals

**NOTE** - This lesson is adapted from Programming Historian's [Getting Started with Markdown](https://github.com/programminghistorian/jekyll/blob/gh-pages/lessons/getting-started-with-markdown.md)
* Intro to markdown, plain text-based syntax for formatting docs
* markdown is integrated into the jupyter notebook

## What is markdown?

* developed in 2004 by john gruber
  - a way of formatting text file
  - a perl utility for converting markdown into html

**plain text files** have many advantages of other formats
1. they are readable on virt. all devices
2. withstood the test of time (legacy word processing formats)

by using markdown you'll be able to produce files that are legible in plain text and ready to be styled in other platforms

ex: 
* blogging engines, static site generators, sites like (github) support markdown & will render markdown into html
* tools like pandoc convert files into and out of markdown

markdown files are saved in extention `.md` and can be opened in text editors like textedit, notepad, sublime text, or vim

We will be using the Jupyter notebook to write markdown in this lesson:

create a new jupyter document
#### Headings
#### Headings

Four levels of heading are avaiable in Markdown, and are indicated by the number of `#` preceding the heading text. Paste the following examples into a code box.

```
# First level heading
## Second level heading
### Third level heading
#### Fourth level heading
```

# First level heading
## Second level heading
### Third level heading
#### Fourth level heading

First and second level headings may also be entered as follows:

```
First level heading
=======

Second level heading
----------
```

First level heading
=======

Second level heading
----------

Notice how the Markdown syntax remains understandable even in the plain text version.

#### Paragraphs & Line Breaks

Try typing the following sentence into the textbox:

```
Welcome to the Jupyter Jumpstart.

Today we'll be learning about Markdown syntax.
This sentence is separated by a single line break from the preceding one.
```

**This renders as:**

Welcome to Jupyter Jumpstart.

Today we'll be learning about Markdown syntax.
This sentence is separated by a single line break from the preceding one.

* Paragraphs must be separated by an empty line
* leave an empty line between `syntax` and `This`
* some implementations of Markdown, single line breaks must also be indicated with two empty spaces at the end of each line


#### Adding Emphasis

* Text can be italicized by wrapping the word in `*` or `_` symbols
* bold text is written by wrapping the word in `**` or `_`

Try adding emphasis to a sentence using these methods:

```
I am **very** excited about the _Jupyter Jumpstart_ workshop.
```

**This renders as:**

 I am **very** excited about the _Jupyter Jumpstart_ lessons.


#### Making Lists

Markdown includes support for ordered and unordered lists. Try typing the following list into the textbox:

```
Shopping List
----------
* Fruits
  * Apples
  * Oranges
  * Grapes
* Dairy
  * Milk
  * Cheese
```

Indenting the `*` will allow you to created nested items.


**This renders as:**

Shopping List
-------------
* Fruits
  * Apples
  * Oranges
  * Grapes
* Dairy
  * Milk
  * Cheese

**Ordered lists** are written by numbering each line. Once again, the goal of Markdown is to produce documents that are both legible as plain text and able to be transformed into other formats. 

```
To-do list
----------
1. Finish Markdown tutorial
2. Go to grocery store
3. Prepare lunch
```

**This renders as:**

To-do list
----------
1. Finish Markdown tutorial
2. Go to grocery store
3. Prepare lunch


**This renders as:**

To-do list
----------
1. Finish Markdown tutorial
3. Go to grocery store
3. Prepare lunch

NOTE the proper order doesn't matter.

#### Code Snippets

* Represent code by wrapping snippets in back-tick characters like `````
* for example `` `<br />` ``
* whole blocks of code are written by typing three backtick characters before and after each block

Try typing the following text into the textbox:

    ```html
    <html>
        <head>
            <title>Website Title</title>
        </head>
        <body>
        </body>
    </html>
    ```

**This renders as**:

```
    <html>
        <head>
            <title>Website Title</title>
        </head>
        <body>
        </body>
    </html>
```

**specific languages** 

in jupyter you can specify specific lanauages for code syntax hylighting

example:

```python

for item in collection:
    print(item)
```

note how the keywords in python are highlighted


#### Blockquotes

Adding a `>` before any paragraph will render it as a blockquote element.

Try typing the following text into the textbox:

```
> Hello, I am a paragraph of text enclosed in a blockquote. Notice how I am offset from the left margin. 
```

**This renders as:**

> Hello, I am a paragraph of text enclosed in a blockquote. Notice how I am offset from the left margin. 

#### Links

* Inline links are written by enclosing the link text in square brackets first, then including the URL and optional alt-text in round brackets

`For more tutorials, please visit the [Programming Historian](http://programminghistorian.org/ "Programming Historian main page").`

**This renders as:**

For more tutorials, please visit the [Programming Historian](http://programminghistorian.org/ "Programming Historian main page").


#### Images

Images can be referenced using `!`, followed by some alt-text in square brackets, followed by the image URL and an optional title. These will not be displayed in your plain text document, but would be embedded into a rendered HTML page.

`![Wikipedia logo](http://upload.wikimedia.org/wikipedia/en/8/80/Wikipedia-logo-v2.svg "Wikipedia logo")`

**This renders as:**

![Wikipedia logo](http://upload.wikimedia.org/wikipedia/en/8/80/Wikipedia-logo-v2.svg "Wikipedia logo")


#### Horizontal Rules

Horizontal rules are produced when three or more `-`, `*` or `_` are included on a line by themselves, regardless of the number of spaces between them. All of the following combinations will render horizontal rules:

```
___
* * *
- - - - - -
```

**This renders as:**

---
***
- - - - - - - 


#### Tables

The core Markdown spec does not include tables; however, some sites and applications use variants of Markdown that may include tables and other special features. [GitHub Flavored Markdown](https://help.github.com/articles/github-flavored-markdown/) is one of these variants, and is used to render `.md` files in the browser on the GitHub site. 

To create a table within GitHub, use pipes `|` to separate columns and hyphens `-` between your headings and the rest of the table content. While pipes are only strictly necessary between columns, you may use them on either side of your table for a more polished look. Cells can contain any length of content, and it is not necessary for pipes to be vertically aligned with each other.

```
| Heading 1 | Heading 2 | Heading 3 |
| --------- | --------- | --------- |
| Row 1, column 1 | Row 1, column 2 | Row 1, column 3|
| Row 2, column 1 | Row 2, column 2 | Row 2, column 3|
| Row 3, column 1 | Row 3, column 2 | Row 3, column 3|
```

**This renders as:**

| Heading 1 | Heading 2 | Heading 3 |
| --------- | --------- | --------- |
| Row 1, column 1 | Row 1, column 2 | Row 1, column 3|
| Row 2, column 1 | Row 2, column 2 | Row 2, column 3|
| Row 3, column 1 | Row 3, column 2 | Row 3, column 3|

To specify the alignment of each column, colons `:` can be added to the header row as follows:

```
| Left-aligned | Centered | Right-aligned |
| :-------- | :-------: | --------: |
| Apples | Red | 5000 |
| Bananas | Yellow | 75 |
```
**This renders as:**

| Left-aligned | Centered | Right-aligned |
| :-------- | :-------: | --------: |
| Apples | Red | 5000 |
| Bananas | Yellow | 75 |

