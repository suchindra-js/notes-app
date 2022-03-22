# Notes App

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)

## Overview

### The challenge

Users should be able to:

- Create a new note
- Update the note and view the note as an HTML page
- Delete the note

### Links

- Live Site URL: [https://amazing-goldstine-de06ba.netlify.app/](https://amazing-goldstine-de06ba.netlify.app/)

## My process

### Built with

- Semantic HTML5 markup
- Flexbox
- CSS Grid
- [React](https://reactjs.org/) - JS library
- [Create React App](https://create-react-app.dev/) - Project Initialization
- [React-mde](https://github.com/andrerpena/react-mde) - Markdown Editor
- [Showdown](https://github.com/showdownjs/showdown) - Markdown to HTML converter
- [Split.js](https://github.com/nathancahill/split/tree/master/packages/splitjs) - Split content

### What I learned

##### Lazy State Initialization

By calling a function inside the useState hook, the value is only initialized in the first render and gets disregarded in subsequent renders. Therefore, the page is more optimized since it's not running unnecessary state initialization.

```js
const [notes, setNotes] = React.useState(
  () => JSON.parse(localStorage.getItem("notes")) || []
);
```
