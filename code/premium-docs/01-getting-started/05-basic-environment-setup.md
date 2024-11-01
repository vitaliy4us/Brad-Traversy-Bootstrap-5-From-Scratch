# Basic Environment Setup

In order to start using Bootstrap, you really don't need much. Here is the gist of what you will need for this course.

## Text Editor

Of course, you need a way to write code. I use and highly reccomend `VS Code`, however you can use whatever you would like. VS Code is extremely popular in the web dev world. It is easy to use, has excellent extensions and ecosystem, it is highly customizable and it is fast and intuitve. I will go over some of the extensions that I will be using in a minute.

## Node.js & NPM

Node.js is a JavaScript runtime and no, we are not building Node.js applications, however, we will be using `NPM`, which is the `Node Package Manager` and you need to download and install Node.js to use it. It is cross platform and simple to install. You can get it at https://nodejs.org. We'll be using NPM in the main 5 projects because we will install Bootstrap, Sass and Font Awesome with it.

## Git

Git is a version control manager and you should be using it to version your projects, meaning creating a repository and saving your code. This way it is backed up and you can roll back to any version that you want. The reason you need it for this course is because we are actually going to deploy two of the websites. One to Vercel and one to Netlify. Both platforms use Git and Github to deploy. You can download Git at https://git-scm.com or if you're using a Mac, you can use Homebrew.

## VS Code Extensions

There are a few extensions and settings that I am using that I think you could benefit from.

### Live Server

Live server is the most important here because this is what I will be using as a dev server. We don't want to just open our html files in the file system, you want some kind of development environment and Live Server is perfect because it is built into VS Code and as the name says, it live updates your project in the browser when you save your files. This way, you don't have to keep refreshing the browser everytime that you make a change.

### Prettier

Prettier is code formatter. It is great because it will format your lines of code automatically. So if something is out of order in indentation, once you save, it will be put in it's place and be auto-formatted. If you miss a semi-colon in CSS or JS, it will add it for you.

## Emmet

That is really it as far as extensions that I really recommend for this course. Emmet is an included feature in VS Code that I will be using a lot. In some editors, it needs to be installed, but in VS Code, it is included by default. It allows us to write HTML quicker.

If you want to add a class of let's say `display-1` to an `h1`, you can type:

```
h1.display-1
```

and hit `enter` or `tab` and it will output `<h1 class="display-1></h1>`

If you want a class of `d-flex` on a `div`, you can use `div.d-flex`, but if it is a div, you can leave it off completely like this:

```
.d-flex
```

This would be `<div class="d-flex"></div>`

If you want an id of 'main', you could do:

```
#main
```

or on a paragraph...

```
p#main
```

This would be `<div id="main"></div>` and `<p id="main"></p>`

You can combine and do:

```
button#button.btn.btn-primary
```

You will get `<button id="button" class="btn btn-primary">`

There is a lot more that you can do with Emmet, but this is really all I'm going to need for this course. I have a complete crash course on the Traversy Media YouTube channel if you're interested in learning more.

So now that I've gone over my basic environment, in the next lesson, we will look at and setup the sandbox.
