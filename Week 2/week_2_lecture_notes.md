### How was homework?
- Problems / Sticking points / Questions?
- Anyone want to demo?
- Let's keep adding to the Glossary!

## Part 1: Everything is a box!
###Learning Objectives
* Define CSS Box Model, and demonstrate the ability to properly manipulate the "box" around tags.
* Differentiate between classes vs IDs and know when to use them.
* Select nested elements to apply styling. 

#### Exercise 1: Box Model
- Use your Chrome Developer Console!

#### Exercise 2: Boxes inside boxes! ([span span span span](https://www.youtube.com/watch?v=anwy2MPT5RE))
- Intro to CSS Descendant Selectors
- If only we had a way to differentiate between boxes...

#### Naming your box!
- Classes vs. Ids
- Classes are Plural, Ids are singular.
- Any html tag can have a class or id:
```
<a href="page.html" id="unique">The One And Only!</a>
<p class="red">Is this text red yet?</p>
<p class="red">Hey, you used it here too!</p>
```
- In css you use a "." to mean class and a "#" to mean id. E.g. `.red` or `#unique`.


#### CSS selector challenge [doc](activity-1-css-selector-challenge.docx)
How would you write a CSS rule that grabs a *specific* anchor tag, without grabbing all the others?
```
  <div>
    <h1>Look at me!</h1>
    <a href='home.html'>Back</a>      <!-- not this anchor! -->
    <a href='about.html'>About me</a>     <!-- and not this! -->
    <ul>
      <li>
        Here is list.
      </li>
      <li>
        It's chilling.
      </li>
      <li>
        Dang, try to grab this bit <a href='select_me.html'>here<a>. 
      </li>
    </ul>
  </div>
```
- `li a` ("find me all anchors inside of li's")
- `ul li a`  ("find me all anchors inside of li's inside of uls")
- `ul a`  ("find me all anchors inside of uls's")
- `html body div ul li a`, etc.

- The syntax for descendant selectors is: `node` `node` `node`...
  - The whitespace is significant! --> read it as "inside of"
  - Note: It's easiest in English to read selectors backwards, from right to left.
- Examples of nodes: `html`, `body`, `div`, `a`, `ul`, `li`.
  - More examples: `p.red`, `a#unique`
  - e.g. "find me `p` tags that have class red", "find me an `a` tag with an id of 'unique'".
- You can't have ids or classes without first attaching them to a piece of html.
  - If we use a "naked" class or id for our selector, e.g. `.red` or `#unique`, we are implicity saying "find me __any__ tag with a class of.../ or id of...".
    - In other words, there's always an implied tag: `__.red`
  - This is super powerful! It means we can now group together disparate html elements by giving them a common class. It means we can style our html based on a shared class name, not just on shared tag names!


### ~~Exercise 3: Ids & Classes (divs)~~
### Exercise 4: Fashion blog p1
Open `Fashion Blog - Final Product.png`, this is what we want our page to look like. Then, open `index.html` and `css/style.css`, and see how close you can get it!

## Part 2: Everything is a box!
###Learning Objectives

* Apply header, footer, sidebar, and multi-column layouts to develop a web page.

* Experiment and predict effects of floats and clearing CSS positioning.

* Describe the use of Normalize and reset.css files.

#### Review: Types of boxes.
#### Review: Classes & Ids.
#### Act-div-ity: You da box. [link](/activity-1-you-da-box.md)
- topics: floats, divs, positioning
- If you missed class or want to review:
  - Play with this codepen: http://codepen.io/pen/def?fork=Byzvxd
  - Read this [awesome article about floats](http://alistapart.com/article/css-floats-101) (and make sure to look at the examples).

#### Exercise 5: Float Layout
- topics: floats, clearing, and clearfix
- see codepen above

#### Exercise 6: Fashion blog p2

## HMWK
* Finish the fashion blog.
* Read this [awesome article about floats](http://alistapart.com/article/css-floats-101) (and make sure to look at the examples).
* Play this awesome [css selector game](http://flukeout.github.io/)
* Have a great break!
