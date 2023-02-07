---
title: Opinionated Reveal.js
<!-- .slide: data-visibility="uncounted"-->
---

<!-- .slide: data-state="layout-title no-fragment"  -->

# RayVeal

## Opinionated Reveal.js

A markdown first presentation framework.<br> Based on [reveal.js](https://revealjs.com/) with preinstalled plugins,<br>a dash of Bootstrap and sweet extras.

<p class="btn-group" role="group" aria-label="Basic example">
<a class="btn btn-lg btn-warning text-dark" href="https://github.com/planetoftheweb/rayveal">Github Repo</a>
<a class="btn btn-lg btn-light text-dark" href="https://rayveal.tech">Demo</a>
</p>

<p class="small mt-4"><span class="badge bg-light text-dark mr-1 ml-2">&larr; &rarr;</span> navigate
<span class="badge bg-light text-dark mr-1 ml-2">t</span>toolbar
<span class="badge bg-light text-dark mr-1 ml-2">m</span>menu
<span class="badge bg-light text-dark mr-1 ml-2">esc</span>overview</p>

---

<!-- .slide: data-state="layout-title" data-transition="zoom" class="bg-dark"-->

# Unique Features

---

# 100% Markdown

- Assumes you use markdown to create slides. The `index.html` file points to a markdown file in `docs/slides/demo.md`.
- It does whatever [reveal.js](https://revealjs.com/) can.

---

# Persistent Toolbar Navigation

The persistent navigation bar at the bottom is on every page. It will disappear after 5 seconds. You can also toggle it by hitting the `t` key. Look for the following code on `docs/index.html`

```html
<footer class="footer">
  <div class="persistent">
    <strong>Slides:</strong>
    <a href="https://bit.ly/thenext50">bit.ly/thenext50</a> &bull;
    <strong>Contact:</strong>
    <a href="https://www.linkedin.com/in/planetoftheweb">LinkedIn</a> |
    <a href="https://www.linkedin.com/learning/instructors/ray-villalobos">courses</a>
    | <a href="https://twitter.com/planetoftheweb">@planetoftheweb</a> |
    <a href="https://github.com/planetoftheweb">github</a>
  </div>
  <div class="smaller">Use arrows to navigate, esc for overview</div>
</footer>
```

---

# Multiple Documents

It assumes you want to write **multiple** markdown files within the same project, just add a file in the `docs/slides` folder.

<small>Press the `m` key to show [sidebar menu](https://github.com/denehyg/reveal.js-menu). You can _use_ it to jump to different slideshows. This list is created using the gulp build process, which generates an `index.json` file for you as you add more markdown files to the `docs/slides` folder.</small>

---

# Author Notes

You can't see them, but they're there. Speaker notes lets you create notes that only you see. Press the `s` key to view **presenter mode**. You create them by using a `> >`

> >

Author notes are similar to markdown blockquotes, but you use double greater than signs. They won't appear on your slides, so I personally use them as reading notes, but there's a presentation mode that allows you to see them in your slides.

---

# Fragments

1. Are on by 'default'
1. You can write HTML lists

(If you don't want them)

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Style Samples

---

# Using Icons <a class="btn btn-primary btn-lg text-white" href="https://www.linkedin.com/learning/instructors/ray-villalobos"><i class="bi bi-linkedin"></i></a> <a class="btn btn-success btn-lg text-white" href="https://github.com/planetoftheweb"><i class="bi bi-github"></i></a>

- Look at the title
- I added some icons from [bootstrap icons](https://icons.getbootstrap.com/)

---

# Inline Color Styles

- [Bootstrap](https://getbootstrap.com)-like colors for bg, text, buttons, code.<br>Notice the two extra bootstrap colors available.
- **Code**: `default` <code class="code-primary">primary</code> <code class="code-success">success</code> <code class="code-info">info</code><br> <code class="code-warning">warning</code> <code class="code-danger">danger</code> <code class="code-royal">royal</code> <code class="code-exciting">exciting</code><br>editable
- <a class="tip" href="#">`tooltips`<span>Overlay explanations, clickable</span></a> available on rollover.

---

# Here's some code

```js [1|5-7]
const electron = require('electron')
const BrowserWindow = electron.BrowserWindow
const app = electron.app

app.on('ready', function () {
  const appWindow
  appWindow = new BrowserWindow()
  appWindow.loadURL('https://raybo.org')
})
```

- Colorized with [highlight.js](https://highlightjs.org/), editable by default
- Language, line numbers, animation `js [1|5-7]`

---

# Embedded Code

Here's a sample of an embeded CodePen. Use an iframe.<br>The iframe can take up the full screen.

<div class="embed-responsive embed-responsive-21by9">
<iframe class="embed-responsive-item" scrolling='no'  title='Bootstrap 4' data-src='//codepen.io/planetoftheweb/embed/bgdOzX/?height=300&theme-id=27192&default-tab=html,result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true'>See the Pen <a href='https://codepen.io/planetoftheweb/pen/bgdOzX/'>Bootstrap 4</a> by Ray Villalobos (<a href='https://codepen.io/planetoftheweb'>@planetoftheweb</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>
</div>
> > You can also use a full screen iframe. If you make it optionally interactive, it's hard for it to lose focus (like making the above codepen editable), so use with care. Here's the special code for that.

`.slide: data-background-iframe="" data-background-interactive="true"`

---

# Tables

Here's what a table looks like.<br>Use the <a href="https://www.tablesgenerator.com/markdown_tables">tables generator</a> to help you write the markdown.

|                  | Extra small <small>< 768px</small> | Small <small> &ge; 768px</small> | Medium <small>&ge; 992px</small> | Large <small>&ge; 1200px</small> |
| ---------------- | ---------------------------------- | -------------------------------- | -------------------------------- | -------------------------------- |
| **Container**    | Auto                               | 750px                            | 970px                            | 1170px                           |
| **Size**         | .col-xs-                           | .col-sm-                         | .col-md-                         | .col-lg-                         |
| **Column width** | Auto                               | ~62px                            | ~81px                            | ~97px                            |

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Layouts

This is a title layout, the default background color is what you saw on the first page. This one uses a custom gray background instead. You can use [Bootstrap](https://getbootstrap.com) background colors if you wish.

They use special tags (see below).<br>Keep going for some additional layouts.

<small>&lt;!-- .slide: data-state="layout-title" --&gt;</small>

<div class="slide-link"><a href="https://bit.ly/35hPnR1"><i class="fab fa-slideshare"></i> bit.ly/35hPnR1</a></div>

---

<!-- .slide: data-state="layout-has-icon" -->

# <i class="bi bi-building"></i> Has Icon

- Template with an icon
- Preloading [font-awesome](https://icons.getbootstrap.com/) <small>by Dave Gandy</small>
- You can use icons from that library anywhere
- This layout aligns it to the heading

<small>&lt;!-- .slide: data-state="layout-has-icon" --&gt;</small>

---

<!-- .slide: data-state="layout-circles" -->

# Circles

Quick small text inside circles

- one
- two
- three
- four
- five
- just list<br>items

<small>&lt;!-- .slide: data-state="layout-circles" --&gt;</small>

---

<!-- .slide: data-state="layout-background-image" data-background-image="images/photo.jpg" -->

# Background with an image<!-- .element: class="animate__animated animate__backInDown  animate__fast " -->

<p  class="animate__animated animate__backInUp animate__slow">
And some text, small shadow, fancy animation...
</p>

<small>&lt;!-- .slide: data-state="layout-background-image" data-background-image="images/photo.jpg" --&gt;</small>

---

<!-- .slide: data-state="layout-mostly-image" data-background-image="images/photo.jpg" -->

# Mostly Image

The quick brown fox jumps over the lazy dog. The quick brown fox jumps over the lazy dog.

<small>&lt;!-- .slide: data-state="layout-mostly-image" data-background-image="images/photo.jpg" --&gt;
</small>

- Photo takes up 60%
- Slide full width
- Responsive fonts

---

# Background Video

<!-- .slide: data-state="layout-background-video" data-background-video="images/video.mp4" -->

<small>&lt;!-- .slide: data-state="layout-background-video" data-background-video="images/video.mp4" --&gt;</small>

---

<!-- .slide: data-state="layout-quote" class="bg-dark" -->

<blockquote class="animate__animated animate__backInDown">
 <i class="fa fa-quote-left text-secondary " aria-hidden="true"></i>
Amazingly few<br>
discotheques provide<br>
jukeboxes
 <i class="fa fa-quote-right text-secondary" aria-hidden="true"></i> 
  <footer class="fragment">--Animate with <a href="https://animate.style/" class="text-warning">animate.style</a></footer>
</blockquote>

<small>&lt;!-- .slide: data-state="layout-quote" class="bg-dark" --&gt;</small>

---

<!-- .slide: data-state="layout-code-list" -->

# Inline Code in Lists

Automatically colorize on second level lists

- `sample`
  - NUM: `one` `two` `three`
  - NUM: `four` `five` `six`
  - NUM: `seven` `eight` `nine`
  - NUM: `ten` `eleven` `twelve`
  - NUM: `thirteen` `fourteen` `fifteen`

<small>&lt;!-- .slide: data-state="layout-code-list" --&gt;</small>

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Bootstrap Components

---

# Bootstrap Cards

<p class="fragment">Use cards with reveal fragment and fragment animation classes.</p>

<div class="card-group">
  <div class="card fragment fade-in-then-semi-out" style="width: 8em">
    <img data-src="images/photo.jpg" class="card-img-top img-fluid" alt="Sample Image">
    <div class="card-body">
      <h3 class="card-title">Card Title</h3>
      <p class="card-text">Quick example text to build on the card title and make up the bulk of the card's content.</p>
      <a href="#" class="btn btn-primary mt-3 text-white">Go somewhere</a>
    </div>
  </div>
  <div class="card fragment fade-in-then-semi-out" style="width: 8em">
    <img data-src="images/photo.jpg" class="card-img-top  img-fluid" alt="Sample Image">
    <div class="card-body">
      <h3 class="card-title">Card Title</h3>
      <p class="card-text">Quick example text to build on the card title and make up the bulk of the card's content.</p>
      <a href="#" class="btn btn-primary mt-3 text-white">Go somewhere</a>
    </div>
  </div>
  <div class="card fragment fade-in-then-semi-out" style="width: 8em">
    <img data-src="images/photo.jpg" class="card-img-top  img-fluid" alt="Sample Image">
    <div class="card-body">
      <h3 class="card-title">Card Title</h3>
      <p class="card-text">Quick example text to build on the card title and make up the bulk of the card's content.</p>
      <a href="#" class="btn btn-primary mt-3 text-white">Go somewhere</a>
    </div>
  </div>
</div>

---

# Stages of a project

List groups are another nice component.<br>Why not use [emojis](https://github.com/SebastianAigner/twemoji-amazing) in your presentation? (search [here](https://emojipedia.org/))

<!-- .element class="fragment" style="font-size: .8em" -->

<ul class="list-group mt-3">
  <li class="list-group-item fragment fade-right">
  <i class="twa twa-beaming-face-with-smiling-eyes"></i>  Enthusiasm</li>
  <li class="list-group-item fragment fade-right">
  <i class="twa twa-disappointed-face"></i> Disillusionment</li>
  <li class="list-group-item fragment fade-right">
  <i class="twa twa-face-screaming-in-fear"></i> Panic</li>
  <li class="list-group-item fragment fade-right">
    <i class="twa twa-pensive-face"></i> Search for the guilty
  </li>
  <li class="list-group-item fragment fade-right">
    <i class="twa twa-pleading-face"></i> Punishment of the innocent
  </li>
  <li class="list-group-item fragment fade-in-then-semi-out">
    <i class="twa twa-raising-hands"></i> Praise for non-participants
  </li>
</ul>

---

# Alerts

  <div class="alert alert-danger fragment w-50">
    <h2 class="alert-heading">Danger Will Robinson</h2>
    <p>You can also easily use other components and classes like alerts as needed in your layouts.</p>
  </div>

  <p class="alert alert-success fragment w-50">
    The alert contextual colors will also work here, so go nuts with these styles.
  </p>

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Installation

---

# Installing

1. Grab/Fork from [repo](http://github.com/planetoftheweb/rayveal)
1. `docs` folder has presentation
1. `docs/slides/demo.md` subfolder has sample markdown
1. `slides/index.json` has a list of presentations (optional, auto-generated by npm start)

---

# Running locally

1. Run `$ npm install` from your terminal
1. Edit `docs/slides/demo.md` or add `*.md files`
1. Run `$ npm start` from your terminal
1. Generates the `docs/slides/index.json` file (index)
1. Creates a live reload server
