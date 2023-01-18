---
marp: true
header: Intro to CSS
footer: "[github.com/paloobi/introtocss](https://www.github.com/paloobi/introtocss)"
---

<style>
    header {
        font-size: 16px;
        font-weight: bold;
        color: #4a00e0;
    }

    footer {
        font-size: 16px;
    }

    h1, h2, h3 {
        color: #4a00e0;
    }

    h1>strong, h2>strong, h3>strong, h4>strong {
        color: #D000FF;
    }


    a {
        color: #D000FF;
    }
</style>


<!--  SECTION 1: INTRO  -------------------------------->

<!-- _backgroundImage: linear-gradient(to right, #4a00e0, #D000FF ); -->
<!-- _color: white -->
<!-- _header: "" -->
<!-- _footer: "**Allie Polubiec**\nemail: alexandra.polubiec@gmail.com\nslides: [github.com/paloobi/intro-to-css]([github.com/paloobi](https://www.github.com/paloobi))" -->
<!-- _class: titlePage -->
<style>
    section.titlePage footer {
        background-color: rgb(255, 255, 255, 0.8);
        color: #000;
        padding: 8px 18px;
        border-radius: 0 4px 4px 0;
        font-size: 20px;
        left: 0;
        box-shadow: 0 2px 5px 2px rgb(0, 0, 0, .4);
    }
</style>

# Intro to CSS

---

# Agenda

* What is CSS?
* How to use CSS
* Basic CSS syntax
* The Cascade
* Intro to CSS Lab (after lecture)

---

# How CSS Fits Into the Web

<!-- JavaScript = Programming Language = Procedures & Logic, Instructions-->
* ### **JavaScript** - Programming Language

<!-- HTML = Markup Language = Content & Structure, Relationships -->
* ### **HTML** - Markup Language

<!-- CSS = Style Sheet Language = Presentation -->
* ### **CSS** - Style Sheet language

---

<!--  SECTION 2: WHAT IS CSS  -------------------------------->

<!-- _backgroundImage: linear-gradient(to right, #4a00e0, #D000FF ); -->
<!-- _color: white -->
<!-- _header: "" -->
<!-- _footer: "" -->

# What is CSS?

---

<!-- _header: Intro to CSS > What is CSS? -->

## Cascading Style Sheets

---

<!-- _header: Intro to CSS > What is CSS? -->

## **Cascading** Style Sheets
<!-- CASCADING - we'll come back to this -->

---

<!-- _header: Intro to CSS > What is CSS? -->

## Cascading **Style Sheets**
<!-- Style Sheet = (like in print media) List of Styles to be applied to structured content -->

---


<!-- _header: Intro to CSS > What is CSS? -->

<!-- _class: threecolumn -->
<style>
section.threecolumn ul { columns: 3; }
</style>

<!--

HTML handles content and structure 

CSS handles how that content is presented.

For example, CSS is used in these slides to set the text size, color and weight.
-->

# What CSS Does

- typography
- color
- sizing
- spacing
- layout
- movement

---
<!-- _header: "" -->
<!-- _footer: "" -->
![bg width:1200](../images/xkcd-with-css.png)

<!-- XKCD comic -->

---
<!-- _header: "" -->
<!-- _footer: "" -->
![bg width:600](../images/xkcd-without-css.png)

<!-- XKCD comic without CSS -->
---

<!-- _header: Intro to CSS > What is CSS? -->

# Why is CSS separate from HTML?

World Wide Web Consortium (W3C) Mission:

- Web for All
- Web on Everything

Source: https://www.w3.org/Consortium/mission

<!-- HTML must be platform agnostic -->
<!-- Web runs on your phone, your laptop, your TV. Screen readers need to be able to read HTML. -->
<!-- HTML is just the content. -->

---

<!-- _header: Intro to CSS > What is CSS? -->

<!-- OK, so then why does un-styled HTML look styled on my browser? h1 vs. p -->
# Your Browser is Already Using CSS
## 

---
<!-- _header: Intro to CSS > What is CSS? -->

<!-- Your browser defines CSS -->
<!-- default presentation even if you don't add CSS -->
# Your Browser is Already Using CSS
## **Browser Default Styles**

<!--  SECTION 3: BOX MODEL  -------------------------------->

---
<!-- _backgroundImage: linear-gradient(to right, #4a00e0, #D000FF ); -->
<!-- _color: white -->
<!-- _header: "" -->
<!-- _footer: "" -->

# The Box Model

---
<!-- _header: Intro to CSS > Box Model -->
<!-- _footer: "source: http://info.cern.ch/hypertext/WWW/MarkUp/Connolly/MarkUp.html" -->

![bg width:1000](../images/html-page.png)

---
<!-- _header: Intro to CSS > Box Model -->
<!-- _footer: "source: http://info.cern.ch/hypertext/WWW/MarkUp/Connolly/MarkUp.html" -->

<!-- Every HTML Element in CSS has an invisible box around it. -->

![bg width:1000](../images/html-page-with-boxes.png)

---
<!-- _header: Intro to CSS > Box Model -->

<!-- Two general display types: -->
# Box Display Types

* ### **block**
* ### **inline**

---
<!-- _header: Intro to CSS > Box Model -->

<!-- BLOCK = new block will go to the next line -->

### **Block** Elements
examples: `div`, `p`, `h1`

![img](../images/display-block.png)

---
<!-- _header: Intro to CSS > Box Model -->

<!-- INLINE = new block will continue without moving to new line -->

### **Inline** Elements
examples:`a`, `span`

![img](../images/display-inline.png)

---
<!-- _header: Intro to CSS > Box Model -->
<!-- _class: textRight -->

<style>
    section.textRight ul {
        position: absolute;
        left: 50%;
        top: 300px;
    }
</style>

<!-- MARGIN = space around -->
<!-- BORDER = border around the outside of the object -->
<!-- PADDING = space between the content and its border; space inside -->
<!-- CONTENT = the dynamic content, such as the text in a paragraph, or the label on a button -->
# The Box Model

Anatomy of a Block Box in CSS

![img w:460 center](../images/box-model.png)

* Margin
* Border
* Padding
* Content

---
<!-- _header: Intro to CSS > Box Model -->

# Example

![img w:500](../images/box-model-example.png)

---

<!-- _header: Intro to CSS > Box Model -->

# Margin

![img w:600](../images/box-model-example-margin.png)

---

<!-- _header: Intro to CSS > Box Model -->

# Border

![img w:500](../images/box-model-example-border.png)

---

<!-- _header: Intro to CSS > Box Model -->

# Padding

![img w:600](../images/box-model-example-padding.png)

---
<!-- _header: Intro to CSS > Box Model -->

# Content

![img w:900](../images/box-model-example-content.png)

---
<!-- _header: Intro to CSS > Box Model -->

![bg w:800](../images/box-model.png)

---

<!--  SECTION 4: WRITING CSS  -------------------------------->

<!-- _backgroundImage: linear-gradient(to right, #4a00e0, #D000FF ); -->
<!-- _color: white -->
<!-- _header: "" -->
<!-- _footer: "" -->

# How to Write CSS

---
<!-- _header: Intro to CSS > Writing CSS -->

## CSS Rules
Define how a box (and its contents) should be presented

---
<!-- _header: Intro to CSS > Writing CSS > Rules -->

# Anatomy of a CSS Rule

<!-- CSS Rule - made of selector + declaration -->

```css
p { /* <---- SELECTOR */
    color: blue; /* <----- DECLARATION */
}
```

- **Selector** - which element(s) to apply styles to
* **Declaration** - colon separated:
    * **property** to set
    * **value** to set it to

---

<!-- _header: Intro to CSS > Writing CSS > Rules -->

# Anatomy of a CSS Rule

<!-- CSS Rule - made of selector + declaration -->

```css
h1, h2 { /* <---- SELECTOR */
    color: purple; /* <------- DECLARATION */
    font-weight: bold; /* <--- DECLARATION */
}
```

* **Multiple Selectors** - comma separated
* **Multiple Declarations** - semi-colon separated

---

<!-- _header: Intro to CSS > Writing CSS > Selectors -->

## Common Selectors

* Type: `p`
* Class: `.myClass`
* ID: `#myID`

---

<!-- _header: Intro to CSS > Writing CSS > Selectors -->
<!-- _class: typeSelectors -->

<style>
    section.typeSelectors h2 {
        background-color: purple;
        color: white;
    }
</style>

## Type Selectors

Select subjects by HTML element type.

### HTML
```html
<h2>Type Selectors</h2>
```

### CSS
```css
h2 {
    background-color: purple;
    color: white;
}
```


---

<!-- _header: Intro to CSS > Writing CSS > Selectors -->
<!-- _class: classSelectors -->

<style>
    section.classSelectors h2 {
        background-color: green;
        color: white;
    }
</style>

## Class Selectors

Select subjects by their `class` attribute.

### HTML
```html
<h2 class="greenText">Class Selectors</h2>
```

### CSS
```css
.greenText {
    background-color: green;
    color: white;
}
```

---
<!-- _header: Intro to CSS > Writing CSS > Selectors -->
<!-- _class: idSelectors -->

<style>
    section.idSelectors h2 {
        background-color: darkblue;
        color: white;
    }
</style>

## ID Selectors

Select subject by its `id` attribute.

### HTML
```html
<h2 id="uniqueHeader">ID Selectors</h2>
```

### CSS
```css
#uniqueHeader {
    color: white;
    background-color: darkblue;
}
```

---
<!-- _header: Intro to CSS > Writing CSS > Selectors -->

## Advanced Selectors
* Psuedo-classes: `a:hover`
* Psuedo-elements: `p::first-line`
* Attribute selectors: `a[href]` or `a[href="example.com"]`

---
<!-- _header: Intro to CSS > Writing CSS > Selectors -->

## Combining Selectors

* List selectors: `h1, p`
* Compound selector: `div.myClass` or `div#myDiv`
* Combinators:
    - Descendent: `div p`
    - Child: `div > p`
    - Sibling: `h1 ~ p` and `h1 + p`

See more in [MDN CSS Selectors Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors)

---
<!-- _header: Intro to CSS > Writing CSS > Declarations -->

# What can you do with CSS Declarations?

* Box Model - margin, border, padding, content
* Text styles
* Positioning & Layout
* Element-specific styles (lists, tables, etc)
* Animations

---

<!-- _header: Intro to CSS > Writing CSS > Declarations -->

# How do I learn all the properties available?

* Practice _(during today's lab!)_
* Browser Developer Tools
* Read the Docs: https://developer.mozilla.org/en-US/docs/Web/CSS/Reference

---

<!--  SECTION 5: ADDING CSS TO HTML  -------------------------------->

<!-- _backgroundImage: linear-gradient(to right, #4a00e0, #D000FF ); -->
<!-- _color: white -->
<!-- _header: "" -->
<!-- _footer: "" -->

# How to Add CSS to HTML
---
<!-- _header: Intro to CSS > Adding CSS to HTML -->

## Where CSS Can Be Defined

* Inline Styles
* Internal Stylesheets
* External Stylesheets

---
<!-- _header: Intro to CSS > Adding CSS to HTML -->

# Inline Styles

```html
<p style="color: purple;">Hello World</p>
```
### **Avoid if possible.**

---
<!-- _header: Intro to CSS > Adding CSS to HTML -->

# Internal Stylesheets

#### **./index.html**
```html
<style>
    p {
        color: purple;
    }
</style>

<p>Hello World</p>
```

---
<!-- _header: Intro to CSS > Adding CSS to HTML -->

# External Stylesheets

#### **./index.html**
```html
<link href="./style.css" rel="stylesheet" type="text/css"/>
<p>Hello World</p>
```

#### **./style.css**
```css
p {
    color: purple;
}
```

---
<!-- _header: Intro to CSS > Adding CSS to HTML -->

<!-- QUESTION: Why do you think it's preferable to use external style sheets? -->
# Why are **external stylesheets** preferred?

* Respect principles of HTML
* Easy to find
* Keep it DRY
* Performance

---
<!-- _header: Intro to CSS > Adding CSS to HTML -->

# How CSS is Loaded in the Browser

![img](../images/how-css-works-mozilla.svg)
source: https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/How_CSS_works

---

<!--  SECTION 6: THE CASCADE  -------------------------------->

<!-- _backgroundImage: linear-gradient(to right, #4a00e0, #D000FF ); -->
<!-- _color: white -->
<!-- _header: "" -->
<!-- _footer: "" -->

# Cascade

---

<!-- _header: Intro to CSS > The Cascade -->

# What happens if there are conflicting rules?

---

<!-- _header: Intro to CSS > The Cascade -->

#### **./styles.css**
```css
h1 {
    color: purple;
}
```

#### **./index.html**
```html
<link href="./style.css" rel="stylesheet" type="text/css"/>


<style>
    h1 {
        color: black;
    }
</style>

<h1 style="color: green;">What Color Am I?</h1> 
```

---

<!-- _header: Intro to CSS > The Cascade -->

#### **./index.html**
```html
<style>
    h1 {
        color: purple;
    }

    .header {
        color: green;
    }
</style>

<h1 class="header">What Color Am I?</h1> 
```

---

<!-- _header: Intro to CSS > The Cascade -->

<!-- I said we'd come back to CASCADING -->
# **Cascading** Style Sheets

---
<!-- _header: Intro to CSS > The Cascade -->

<!-- CSS uses the Cascade algorithm to determine which styles to apply-->
<!-- RELEVANCE: Does the rule apply to this element?  -->
<!-- ORIGIN & IMPORTANCE: Where is the rule coming from? (Browser defaults? External stylesheet?) Is it flagged with the `!important` keyword? -->
<!-- SPECIFICITY: Which rule is more specific? -->
<!-- ORDER: Which rule was declared more recently? -->

# The **Cascade** Algorithm

#### 1. Relevance

#### 2. Origin & Importance

#### 3. Specificity

#### 4. Order

---
<!-- _header: Intro to CSS > The Cascade -->

<!-- I recommend spending some time reading the MDN articles on Cascade to learn more about Relevance, Importance & Origin. -->
<!-- But as a Developer, the aspects of this cascade that will be most directly involved in the CSS code you write are Relevance, Specificity & Order-->
<!-- RELEVANCE = selectors -->
# The **Cascade** Algorithm

#### 1. **Relevance**

#### 2. Origin & Importance

#### 3. **Specificity**

#### 4. **Order**

---
<!-- _header: Intro to CSS > The Cascade -->

# Inline Styles > Other Developer Styles

<!-- separate from specificity & origin -->
<!-- inline  -->
#### **./styles.css**
```css
.purple {
    color: purple;
}
```

#### **./index.html**
```html
<h1 class="purple" style="color: green;">What Color Am I?</h1> 
```

---
<!-- _header: Intro to CSS > The Cascade > Specificity -->

# The Cascade > Specificity

---
<!-- _header: Intro to CSS > The Cascade > Specificity -->

<!-- Which of the rules is most specific? -->
# More Specific > Less Specific

1. Type selector
2. Class selector
3. ID selector

---
<!-- _header: Intro to CSS > The Cascade > Specificity-->
<!-- _class: orangeHeader -->
<style>
    section.orangeHeader h1 {
        color: darkorange;
    }
</style>

# What Color Am I?

#### **./index.html**
```html
<style>
    h1 {
        color: purple;
    }

    .header {
        color: darkorange;
    }
</style>

<h1 class="header">What Color Am I?</h1>
```

---
<!-- _header: Intro to CSS > The Cascade > Order -->

# The Cascade > Order

---
<!-- _header: Intro to CSS > The Cascade > Order -->
<!-- _class: redHeader -->
<style>
    section.redHeader h1 {
        color: red;
    }
</style>

<!-- Which rule was declared most recently? -->

# What Color Am I?

#### **./styles.css**
```css
h1 {
    color: blue;
}

h1 {
    color: red;
}
```
#### **./index.html**
```html
<h1>What Color Am I?</h1> 
```

---
<!-- _header: Intro to CSS > The Cascade > Order -->
<!-- _class: greenHeader -->
<style>
    section.greenHeader h1 {
        color: green;
    }
</style>

<!-- Which rule was declared most recently? -->
# What Color Am I?

#### **./styles.css**
```css
.purple {
    color: purple;
}
```
#### **./index.html**
```html
<link href="./style.css" rel="stylesheet" type="text/css"/>
<style>
    .purple {
        color: green;
    }
</style>
<h1 class="purple">What Color Am I?</h1> 
```

---
<!-- _header: Intro to CSS > The Cascade -->

# How do I know **why** something is styled the way it is?

---
<!-- _header: "" -->
<!-- _footer: "" -->

## **Browser Developer Tools**

![img](../images/browser-dev-tools.png)

---
<!-- _header: Intro to CSS > The Cascade -->

# Cascade: Further Reading

MDN Docs:
- [Cascade](https://developer.mozilla.org/en-US/docs/Web/CSS/Cascade
)
- [Specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity)

---

<!--  SECTION 7: OUTRO  -------------------------------->

<!-- _backgroundImage: linear-gradient(to right, #4a00e0, #D000FF ); -->
<!-- _color: white -->
<!-- _header: "" -->
<!-- _footer: "" -->

# Wrapping Up

---
<!-- _header: Intro to CSS > Wrapping Up -->

# Summary

* CSS = Cascading Style Sheets
* How CSS works
    * Box Model
* Basic CSS syntax
    * Rule = Selector(s) + Declaration(s)
* How to use CSS
    * External Stylesheets
* The Cascade

---
<!-- _header: Intro to CSS > Wrapping Up -->

# What's Next?

* ### **Intro to CSS Lab** <--- Later Today!
* ### **CSS Layouts** - tomorrow
* ### **CSS Animations** - next week

---
<!-- _header: Intro to CSS > Wrapping Up -->

# Resources

- MDN CSS Reference: https://developer.mozilla.org/en-US/docs/Web/CSS
- CSS-Tricks: https://css-tricks.com/
- _CSS is Weird_: https://hacks.mozilla.org/2019/10/why-is-css-so-weird/ (Video)
- _HTML & CSS_ by John Duckett (Book)

---

<!-- _backgroundImage: linear-gradient(to right, #4a00e0, #D000FF ); -->
<!-- _color: white -->
<!-- _header: "" -->
<!-- _footer: "" -->

# Let's Get Stylin'!