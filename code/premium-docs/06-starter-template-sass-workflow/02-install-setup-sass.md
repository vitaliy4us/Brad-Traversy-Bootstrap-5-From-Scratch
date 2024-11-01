# Install & Setup Sass

There are many ways to compile Sass/scss files into CSS. What we will be doing is creating a development environment that will include the `Sass` package. In order to do this, we will need to use `NPM` to install the `Sass` package. We can also install Bootstrap with `NPM`. So I just want to talk about NPM real quick for those of you that are new to this sort of thing.

## What Is NPM?

The `Node Package Manager` is a tool for installing packages via the command line. Packages could be anything including a library, framework or just a simple helper. There are over 1.5 million packages in the [npmjs](https://www.npmjs.com/) registry.

You need to install `Node.js` on your system in order to use NPM. You can download Node at https://nodejs.org. Node is a JavaScript runtime. It allows you to run JavaScript code outside of the browser. NPM is a tool that comes with Node.js.

I want to stress that you do not need to know JavaScript to use NPM. We are not building a Node.js application. We are just using NPM to install packages that will help us with our Sass workflow.

## Create A Project Folder

Create a folder called `bs5-simple-starter` and open it in your code editor. This is where we will be working. You also want to open a terminal. If you are using VS Code, you can open a terminal by going to `Terminal` > `New Terminal`.

## `package.json` file

Every Node.js project has a file called `package.json`. This is a manifest file that includes some basic info about your project like the name, version, description, but it also includes all of the packages that you install.

The first thing that you want to do in every Node project is initialize your `package.json` file. You can do that with the following command:

```bash
npm init
```

You will get asked a bunch of questions. You can just hit enter through all of them. This will create a `package.json` file in your project folder.

You can also skip all of the questions by running `npm init -y`.

## Installing Packages

We can install packages with `npm install packagename`. Run the following to install the `Sass` package:

```bash
npm install sass
```

This will install the `Sass` package and add it to our `package.json` file. You should see a folder called `node_modules` in your project folder. This is where all of the packages that you install will go. There will always be a lot of folders in here because it doesn't only include the dependencies that you install, but also the dependencies of those dependencies.

## Add a .gitignore file

When you push this code to GitHub, you do not want to include the `node_modules` folder. It is not needed because anyone can install the packages that they need by running `npm install`.

The file `.gitignore` is used to declare which files should not be commited to the repo.

Create a file in the root of your project folder called `.gitignore` and add the following line:

```bash
node_modules
```

Now when you push your code to GitHub, the `node_modules` folder will not be included.

## Custom JS File

There will be times where we need to add some custom JavaScript. So create a file called `js` in the root and create a file in it called `script.js`. Just leave it empty.


## Using The Sass Package

Now that we have the Sass package installed in our local environment, let's set it up to compile Sass.

### initialize `package.json`

The first thing that we want to do is initialize our `package.json` file. You can do that with the following command:

```bash
npm init
```

Just hit enter through all of the questions. This will create a `package.json` file in your project folder.

**Tip**: You can skip all of the questions by running `npm init -y`.

## Sass Workflow

Create a folder called `scss` in your project folder. This is where we will put all of our Sass files. Create a file called `styles.scss` in the `scss` folder.

Add the following code to `scss/styles.scss`:

```scss
$primary-color: #333;

body {
  background-color: $primary-color;
}
```

As you can see, this is not valid CSS. It is Sass.

What we need to happen is for the Sass to be compiled into CSS. Since we installed the sass package locally in our project, we can not run a global command to use it. We need to create what is called an `npm script`.

Open up your `package.json` file and add the following code:

```json
"scripts": {
    "sass:build": "sass scss:css"
  },
```

Now, in your terminal, you can run the following command:

```bash
npm run sass:build
```

This will compile the Sass in the `scss` folder into CSS in the `css` folder. If you open the `css` folder, you should see a file called `styles.css` with this code:

```css
body {
  background-color: #333;
}
```

As you can see, this is valid CSS.

So now create an `index.html` file in your project folder and add the following code:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="css/styles.css" />
    <title>Bootstrap 5 Simple Starter</title>
  </head>
  <body>
    <h1>Bootstrap 5 Simple Starter</h1>
  </body>
</html>
```

Open the html page with the Live Server extension if you are using VS Code.

You should see the dark background. Your Sass has been compiled.

## Watching For Changes

If we keep this as is, we will have to run the `npm run sass:build` command every time we make a change to our Sass. This is not ideal. We want to be able to make a change to our Sass and have it automatically compile to CSS.

Add another script to your package.json.

```json
  "scripts": {
    "sass:build": "sass --no-source-map scss:css",
    "sass:watch": "sass --no-source-map --watch scss:css"
  },
```

Also, add the flag `--no-source-map` to the `sass:build` and the `sass:watch` script so that source maps are not generated.

Now, run the following command in your terminal:

```bash
npm run sass:watch
```

Now any changes that you make will automatically be compiled to CSS. This will be our workflow for all of our projects. You run the watch command to compile Sass and Live Server to view the changes in the browser.

Delete the code from the `scss/styles.scss` file. The `style.css` file should be empty.

Stop the watch command with `ctrl + c`.

Now we are ready to install Bootstrap and customize it. We will do that in the next lesson.
