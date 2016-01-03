# Lab XX: Let's make a lab!

<!-- This is the code for the terminal thingie at the top -->
<div class="text-left terminal type-wrap">
<div>
  <span id="command">$ </span>
</div>
<br>
<div class="readme">
  <ol>
    <li>
      This CSE 15L lab has two components: a lab exercise, and a quiz. 
    </li>
    <li>
      For the lab exercise, you’ll be working in a team of two: pair programming, two people to one machine. You just need to login as ONE of you, using your cs15xxx user name.
    </li>
    <li>
      For the lab quiz, you will work individually.
    </li>
    <li>
       Switch drivers (student on the keyboard) every 20 minutes.
    </li>
  </ol>
</div>
</div>

# Hello Lab Maker!

We use Showdown to convert MD files to HTML using JavaScript. Please see the below to see how formatting works with the Markdown file and what it looks like when it gets converted.

![Showdown][sd-logo]

Showdown is a Javascript Markdown to HTML converter, based on the original works by John Gruber. It can be used client side (in the browser) or server side (with Node or io). 

# Here's some of the syntax supported


# Paragraphs

Paragraphs in Markdown are just one or more lines of consecutive text followed by one or more blank lines.

    On July 2, an alien mothership entered Earth's orbit and deployed several dozen saucer-shaped "destroyer" spacecraft, each 15 miles (24 km) wide.
    
    On July 3, the Black Knights, a squadron of Marine Corps F/A-18 Hornets, participated in an assault on a destroyer near the city of Los Angeles.

Result:

On July 2, an alien mothership entered Earth's orbit and deployed several dozen saucer-shaped "destroyer" spacecraft, each 15 miles (24 km) wide.

On July 3, the Black Knights, a squadron of Marine Corps F/A-18 Hornets, participated in an assault on a destroyer near the city of Los Angeles.

# Headings

You can create a heading by adding one or more # symbols before your heading text. The number of # you use will determine the size of the heading. This is similar to [**atx style**][atx].

    # The largest heading (an <h1> tag)
    ## The second largest heading (an <h2> tag)
    …
    ###### The 6th largest heading (an <h6> tag)

You can also use [setext style][setext] headings.

    This is an H1
    =============
    
    This is an H2
    -------------

# Blockquotes

You can indicate blockquotes with a >.

    In the words of Abraham Lincoln:
    
    > Pardon my french


# Styling text

You can make text **bold** or *italic*.

    *This text will be italic*
    **This text will be bold**

Both bold and italic can use either a `*` or an `_` around the text for styling. This allows you to combine both bold and italic if needed.

    **Everyone _must_ attend the meeting at 5 o'clock today.**


# Lists

## Unordered lists

You can make an unordered list by preceding list items with either a * or a -.

    * Item
    * Item
    * Item

    - Item
    - Item
    - Item

Result:

* Item
* Item
* Item

## Ordered lists

You can make an ordered list by preceding list items with a number.

    1. Item 1
    2. Item 2
    3. Item 3

Result:

1. Item 1
2. Item 2
3. Item 3

## Nested lists

You can create nested lists by indenting list items by two spaces.

	1. Item 1
		1. A corollary to the above item.
		2. Yet another point to consider.
	2. Item 2
		* A corollary that does not need to be ordered.
		* This is indented four spaces, because it's two spaces further than the item above.
		* You might want to consider making a new list.
	3. Item 3

Result:

1. Item 1
	1. A corollary to the above item.
	2. Yet another point to consider.
2. Item 2
	* A corollary that does not need to be ordered.
	* This is indented four spaces, because it's two spaces further than the item above.
	* You might want to consider making a new list.
3. Item 3

# Code formatting

## Inline formats

Use single backticks (\`) to format text in a special monospace format. Everything within the backticks appear as-is, with no other special formatting.

    Here's an idea: why don't we take `SuperiorProject` and turn it into `**Reasonable**Project`.

## Multiple lines

Showdown wraps a code block in both `<pre>` and `<code>` tags.

To produce a code block in Markdown, simply indent every line of the block by at least 4 spaces or 1 tab.

    This is a normal paragraph:
    
        This is a code block.

You can also use triple backticks to format text as its own distinct block.
    
    ```
    x = 0
    x = 2 + 2
    what is x
    ```

Result:

```
x = 0
x = 2 + 2
what is x
```

# Links

Showdown supports two style of links: *inline* and *reference*.

## Inline

You can create an inline link by wrapping link text in brackets ( `[ ]` ), and then wrapping the link in parentheses ( `( )` ).

For example, to create a hyperlink to `showdown.github.io`, with a link text that says, Showdown is great!, you'd write this in Markdown: 

    [Showdown is great!](http://showdown.github.io/)

Result:

[Showdown is great!](http://showdown.github.io/)

## Reference

Reference-style links use a second set of square brackets, inside which you place a label of your choosing to identify the link:

    This is [an example][id] reference-style link.

Then, anywhere in the document (usually at the end), you define your link label like this, on a line by itself:

    [id]: http://example.com/  "Optional Title Here"

Result:

This is [an example][id] reference-style link.

# Images

You can add an image in various ways, with manual dimensions.

	![tag1](example.png)
	![tag2](example.png =100x80)     <!-- simple, assumes units are in px -->
	![tag3](example.png =100x*)      <!-- sets the height to "auto" -->
	![tag4](example.png =80%x5em)  <!--Image with width of 80% and height of 5em -->

Result:

![tag1](example.png)
![tag2](example.png =100x80)     <!-- simple, assumes units are in px -->
![tag3](example.png =100x*)      <!-- sets the height to "auto" -->
![tag4](example.png =80%x5em)  <!--Image with width of 80% and height of 5em -->

# Tables

Tables aren't part of the core Markdown spec, but they are part of GFM and Showdown supports them by turning on the flag `tables`.

```
| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| **col 3 is**  | right-aligned | $1600 |
| col 2 is      | *centered*    |   $12 |
| zebra stripes | ~~are neat~~  |    $1 |
```

this will produce this:

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| **col 3 is**  | right-aligned | $1600 |
| col 2 is      | *centered*    |   $12 |
| zebra stripes | ~~are neat~~  |    $1 |


Colons can be used to align columns.

The outer pipes (|) are **NOT** optional. But you don't need to make the raw Markdown line up prettily.

You can also use other markdown syntax inside them.


[sd-logo]: https://raw.githubusercontent.com/showdownjs/logo/master/dist/logo.readme.png
[releases]: https://github.com/showdownjs/showdown/releases
[atx]: http://www.aaronsw.com/2002/atx/intro
[setext]: https://en.wikipedia.org/wiki/Setext
[id]: http://example.com/  "Optional Title Here"