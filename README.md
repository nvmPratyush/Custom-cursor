# Coustem Cursor

## Introduction
It's custom cursor that makes your mouse pointer more fun and personalized in your website

## Installation
### CDN
For prototyping or learning purposes, you can use the latest version with:

```js
<script src="https://cdn.jsdelivr.net/npm/kursor"></script>
```
For production, we recommend linking to a specific version number and build to avoid unexpected breakage from newer versions:

```js
<script src="https://cdn.jsdelivr.net/npm/kursor@0.0.14/dist/kursor.js"></script>
```
You can browse the source of the NPM package at https://www.jsdelivr.com/package/npm/kursor.

Kursor is also available on [unpkg](https://unpkg.com/kursor@0.1.6/dist/kursor.js) and cdnjs (cdnjs takes some time to sync so the latest release may not be available yet).

### NPM
NPM is the recommended installation method when building large scale applications with Kursor. It pairs nicely with module bundlers such as Webpack or Browserify

# latest stable
```cmd
$ npm install kursor
```
# Explanation of Different Builds
In the dist/ directory of the NPM package you will find many different builds of kursor.js. Here’s an overview of the difference between them:

| UMD                 |                 |
| ------------------- | --------------- |
| Full                | kursor.js       |
| Full (production)   | kursor.min.js   |

## Getting Started
The easiest way to try out Kursor.js is using the [JSFiddle Hello World example](https://jsfiddle.net/luisdanielroviracontreras/01xsk2fq/9/). Feel free to open it in another tab and follow along as we go through some basic examples. Or, you can create an index.html file and include Kursor with:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="https://unpkg.com/kursor/dist/kursor.css">
</head>
<body>
    <div id="app">
        <p>hello Kursor.js</p>
    </div>
</body>
    <script src="https://unpkg.com/kursor"></script>
    <script>
        new kursor({
            type: 1
        })
    </script>
</html>
```

## configuration
Kursor.js is a very simple library to configure, when instantiating the global variable kursor as a parameter we pass the options to create the cursor (mouse)

### type
Change the theme of the kursor, as value is of type Number and at the moment there are only 5 types of cursors

```js
new Kursor({
  type: 1 /* 1 | 2 | 3 | 4 | 5 */
})
```

### el
By default Kursor is implemented inside the <body>, but if you only need the cursor(mouse) inside a specific element you can use the property (el)

As a value you need a String with the name of the id or the class an example would be something like this

```html
<div class="myBox"></div>
```
```js
new Kursor({
  el: '.myBox'
})
```
### removeDefaultCursor
Remove the user's default cursor with exceptions in the input elements and some others

```js
new Kursor({
  removeDefaultCursor: true
})
```
### color
Change the color of the theme to the one provided, changing all its modalities to that color as (`hover`,`mousedown`)

```js
new Kursor({
  color: 'rgba(200,145,54)'
})

// OR

new Kursor({
  color: '#476582'
})
```
## Types
The property that changes the cursor is type and at the moment we only have 5 types of cursors

## Contributing
Contributions to enhance or expand the project are welcome. Feel free to fork the repository, make changes, and submit pull requests.

## License
This project is open-sourced under the [Apache 2.0 License](LICENSE).
