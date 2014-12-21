##Rope Divs
__Goals__: To explore block level elements, normal flow, and floating.

__Prep__: 4 x volunteers (red team), two very long pieces of rope

__Instructions__:

You are a block level element called a "div". You follow three rules:

1. You are as __wide__ as you can be.
2. You are a __short__ as you can be.
3. You don't let things on your __left__ or __right__.

Assume the following page layout (omitting html boilerplate):
```
<body>
    <div id="red-team"></div>
<body>
```

- Where do you stand?
- What is your height?
- What is your width?
- What color are you? (trick question!)

Now, let's play with styling:
```
div {
    height: 3ft;
    /*width: 3ft;*/
    /*float: left;*/
    /*float: right;*/
}
```

- Again, where do you stand as your style changes?

Let's add some more html content, like so:
```
<body>
    <div id="red-team">
      <div class="chair"></div> <!-- Who wants to volunteer? -->
    </div>
<body>
```

Let's assume a chair has the following style:
```
chair {
  display: block;
  height: 3ft;
  width: 2ft;
  border: 1px solid white;
  background-color: gray;
}
```
- Where do you go?
- Div, how tall are you? What if we remove your height?
- What if we add two more chairs (volunteers)?
- What if we float our chairs left?
- The div no longer knows how tall to be! (We'll talk about how to solve this later)

Let's get 4 more volunteers (blue team) in the following layout:
```
<body>
    <div id="red-team"></div>
    <div id="blue-team"></div>
<body>
```

- Where do *you* stand?
- What is your height?
- What is your width?

Now, let's use the following css stylesheet:
```
div {
    height: 3ft;
    width: 50%
    /*margin-bottom: 3ft;*/
}
```
- Again, where do you stand?
- What is your height?
- What is your width?

Now, let's float!
```
div {
    width: 50%;
    float: left;
    /*float: right;*/
}
```

- Again, where do you stand? In what order?
- What happens if your width gets smaller? Bigger?
- What about your margin?

Now, let's float one by one!
```
div {
    height: 3ft;
  width: 50%;
}

div.red-team {
    float: left;
}
```
```
div {
    height: 3ft;
  width: 50%;
}

div.blue-team {
    float: left;
}
```
- Uh oh, what happens now?

Now, let's clear!
```
div {
    width: 50%;
    float: left;
    clear: left; /* Get out the way! I'm floating here! */
}
```

- Can you float center?

```
div {
    width: 50%;
  height: 3ft;
    margin-left: auto;
    margin-right: auto;
}
```


Finally, let's play with positioning:
```
div {
    height: 3ft;
  width: 50%;
    float: right;
}

div.blue-team {
    position: absolute;
}
```

```
div {
    height: 3ft;
  width: 50%;
    float: right;
}

div.blue-team {
    position: absolute;
    bottom: 0;
    left: 0;
}
```

```
/* blue-team, go ahead and sit down! */

div.red-team {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
}
```

### Review
- float behavior
- relative size of child (based on parent!)
- positioning (also relative to parent!)
- collapsing margins