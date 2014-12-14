#Week 1
## Meet & Greet

## Intro to FEWD
Our Building Blocks (Client-Side):
* __HTML__ (Hyper Text Markup Language)
* __CSS__ (Cascading Style Sheets)
* __JS__ (JavaScript)


### A look back
How did we get from "HyperText" to the media-rich, responsive, modern web?
* 1990: Tim Berners-Lee describes "[HyperText](http://www.w3.org/History/19921103-hypertext/hypertext/WWW/WhatIs.html)"
* What's a browser? ([lee's definition](http://www.w3.org/History/19921103-hypertext/hypertext/WWW/Terms.html#browser))
* The browser wars ([infographic](https://upload.wikimedia.org/wikipedia/commons/7/74/Timeline_of_web_browsers.svg))
* Evolving standards / developing standards ([infographic](../img/unit_1/Timeline_of_web_technologies.jpg) [*](http://www.onbile.com/info/wp-content/uploads/2013/09/Timeline-of-web-technologies-639x168.jpg))
* New Frontiers: smartphones, tablets, the "native app" wars!

![infographic](../img/unit_1/Timeline_of_web_technologies.jpg)

# Diving in

## HTML
### HTML Basics
* Exercise 01: HyperText!
* What's a markup language? What's a WYSIWYG? [demo](#hypertext)
* HTML Tag Syntax
![HTML Syntax](../img/unit_1/tags.png)

### Common Content Tags

####Heading Elements
* ```<h1>```Largest Heading```</h1>```
* ```<h2>``` . . . ```</h2>```
* ```<h3>``` . . . ```</h3>```
* ```<h4>``` . . .```</h4>```
* ```<h5>``` . . . ```</h5>```
* ```<h6>```Smallest Heading```</h6>```


#### Text Elements
* ```<p>```This is a paragraph```</p>```
* ```<code>```This is some computer code```</code>```

#### Unordered list
* ```<ul>``` ```</ul>```

#### Unordered list item
* ```<li>```First item```</li>```
*   ```<li>```Next item```</li>```


#### Links
* ```<a href="Link">```First item```</a>```

#### Escaping
* What characters are illegal in html?
  * If it looks like a tag, html will treat it like a tag!
  * e.g. `<fake>`
  * In order to display the brackets you need to convert them to their legal form: "<" or `&lt;` (less than), ">" or `&gt;` (greater than).
  * This is why you will sometimes see `&` represented as `&amp;` (ampersand).
* What about special characters like the accented `é`?
  * This is where `<meta charset="utf-8">` comes into play!
  * utf-8 supports additional/special characters. Without specifying a character encoding your `é` will become `Ã©`!

### HTML Layout
* Nesting Tags & Indentation
  * Rule of thumb: Every time you open a new tag, tab *in* one level of indentation!
* HTML5 Declaration: ```<!DOCTYPE html>```
* Basic HTML Skeleton:

``` html
<!DOCTYPE html>

<html>
  <head>
    <meta charset="utf-8">
    <title>My Website</title>
    <link rel="stylesheet" href="css/your_external_stylesheet.css">
  </head>

  <body>
    <!-- Your Content Here! -->
  </body>
</html>
```

* What is the root element or node? <html>
* How many children does html have? 2! head and body.

* Exercise 02: HTML5 Press Release


## CSS
### CSS Basics
* What's a style? Stylesheet? [demo](#strip-styles)
* Exercise 03: About Me
* CSS Syntax

![CSS Syntax](../img/unit_1/css_syntax.png)

####Where can styles live?
* Inline
* In the `head` inside of a `<script></script>` tag
* In a separate file (preferred)

What are the benefits/limitations of each of these options?


####CSS Break Down
Here's an example css **rule**:

```
p {
  color: red;
  font-weight: bold;
}
```

The `p` is called a **selector**, and it's followed by a set of **declarations** in a **declaration block**.

Work together to describe the syntax.

#### Syntax
The **selector** (`p`) specifies what parts of the HTML document should be styled by the declaration. It can be read as "For all `<p>` elements on the page, apply the following rules..."

Every declaration is a **property** followed by a **value**, separated by a colon, ending in a semicolon.

In this declaration, we are setting the `color` **property** to the **value** `red`.

Try writing a new set of styles for another element, like an `h1`.


#### Linking to External Stylesheets
Its best practice to put CSS in its own file and link to it from the `<head>`.

* ```<link rel="stylesheet" href="style.css">```
  
Note:
"The `link` tag needs two attributes: `rel="stylesheet"` and an `href` attribute.

The `href` attribute value works very similarly to linking to an image, or to another page.

#### Colors
  * Colors are most commonly expressed as hexadecimal values, like `#00CC99` or with their English equivalent, like "teal".
  * Hex values are a way of encoding how much Red (R), Blue (B) and Green (G) "paint" get mixed together, e.g. #RRBBGG.
  * Hexadecimal is base 16! Here's how you count to 32 in Hexadecimal: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 1A, 1B, 1C, 1D, 1E, 1F, 20.
  * 16^6 = 16,777,216 colors!

#### Specificity
* Which style wins!?
  * Later styles overwrite earlier styles.
  * More specific selectors beat less specific selectors.
  * Inline styles beat external stylesheets.

#### Default Styling
* Eventually you will start fighting with the default styles applied to html tags. For example, h1 tags have a top and bottom margin of .67em.
* Here's a helpful reference point: http://www.w3.org/TR/CSS2/sample.html
* Remember, this can also vary from browser to browser!

#### Remaining Time
* Exercise 04: Resume

### Looking Forward:
* What's javascript? [demo](#click-it-good)
* What's a document tree? [demo](#firefox-3d)

## HMWK:
* Finish class exercises.
* Make your own "About Me" page and "Resume" page.
* Upload your project to the "Week 1" folder on Schoology (under "Materials"). Since you will be submitting multiple files, you need to make sure to zip/compress your project folder. How-to: [mac](http://www.macinstruct.com/node/159), [win](http://www.sevenforums.com/tutorials/175864-zip-file-folder-how.html).


## In-Class Demos
#### HyperText
* Explore Tim Berners-Lee's demonstration of "[HyperText](http://www.w3.org/History/19921103-hypertext/hypertext/WWW/WhatIs.html)"
* Did Tim use Chrome? Can we still open the file!? Can we render his mark up!?
* What tags are still in use today? What's changed? (Make sure to [view source](view-source:http://www.w3.org/History/19921103-hypertext/hypertext/WWW/Terms.html#browser)!)
* What is "plain text" anyhow?

#### Strip Styles
* What gives a website its looks?
* Remove all stylesheets from [sfchronicle.com](http://www.sfchronicle.com/) using:
`$('style,link[rel="stylesheet"]').remove()`
* What's seperation of concerns? 

#### Click it good
* What makes a website interactive?
* Go to [cornify.com](http://www.cornify.com/) and click the "Cornify" button. Again. And again.

# Tips
## Essential Tools
### SublimeText
* It's best to open your entire project *folder*, not individual files. The easiest way to do this is to drag your folder onto the SublimeText icon in your dock. Alternatively, from SublimeText, click "File > Open" and click on the folder you want to open.
* To view your project's file structure, click "View > Show Sidebar". This makes opening project files way easier!

### Chrome Developer Tools
* Chrome is our preferred browser because it comes with a powerful toolset for exploring and debugging websites.
* The first tool we'll be using is "Inspect Element." Try it out: open a web page, right click a random element on the page, and select "Inspect Element". This will pop open a window with the current line of html, highlighted on the left, and the css styles that are affecting it, listed on the right. Poke around and explore! We'll be using this tool a lot!
* Your browser is also a handy way to explore your file system! The next time you open a project in chrome, take a close look at the url. You should see something like: `file:///Users/NAME/fewd/week%201/starter_code/index.html`. Try deleting "index.html" from the url and hit enter. This is a great way to sanity check that everything is linked together properly.

### Finder / File Explorer
* It's important to stay organized! I recommend you create a folder for all of your FEWD projects, organized by week. Take a moment to think it over: where are you downloading/unzipping files? Where do you need to move them? Don't forget to clean up!
* Are you comfortable with the various ways of displaying your files? Try toggling your view to show your files as icons, a list, and as columns. I prefer columns.

## Essential Shortcuts
####Basics
* `cmd+z` (undo) / `cmd+shift+z` (redo)
* `ctrl+c` (copy) / `ctrl-x` (cut)
* `ctrl+v` (paste)
* `cmd+tab` (toggle windows) / `cmd+shift+tab` (toggle in reverse)

####SublimeText
* `tab`  or `shift+]` (indent)
* `shift+tab` or `shift+[` (unindent)
* `cmd+/` (comment code)
* `cmd+arrow-key` (jump to the beginning/end of a line, or the top/bottom of the page).

Learn 'em and use 'em! Don't forget you can always click on the menu to jog your memory! The keyboard shortcuts are listed next to each menu option.

## Resources
* How do I know what HTML tag to use? [List of HTML5 Tags](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5/HTML5_element_list?redirectlocale=en-US&redirectslug=HTML%2FHTML5%2FHTML5_element_list)