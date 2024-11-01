# What Is Sass?

Up to this point, we have just been using the default Bootstrap CSS. This means the same colors, font-sizes, shadows, border radius, etc. This can be a problem if you don't want all of your websites and applications to look the same, or at least, very similar. There are some sites that you go to and you just know right of the bat that they use Bootstrap. I am going to show you how to customize your layouts and we do that with a technology called `Sass`.

I want to stress that you don't really need to know much Sass to use it for what we are doing. We are basically just taking the Bootstrap Sass files and changing some variables to customize it and then re-compiling the Bootstrap CSS file. However, I want to just quickly go over what Sass is.

## CSS Preprocessor

Sass is what we call a CSS preprocessor or precompiler. It's an extension of CSS that adds new features that are not included in native CSS. I will go over those in a minute, but the way that Sass works is we create a file with either a `.sass` or `.scss` extension. `scss` is more common. Those files then have to be compiled to regular CSS. I'll talk more about that in a minute, but let's look at some of the features Sass offers.

- **Variables**: CSS now has custom properties, which are similar to variables, but the Sass syntax is much easier
- **Nesting**: You can nest styles in eachother. Here is an example:

```scss
.header {
  background: black;
  color: white;

  h1 {
    color: red;
  }
}
```

So this would make only the `h1` tags within the header red. You can have unlimited layers of nesting.

- **Mixins**: Mixins allow you to define reusable sets of CSS declarations. They are similar to functions as they also take in paramaters.
- **Import**: Sass provides the `@import` syntax that splits your stylesheets into smaller chunks. This is what allows us to include the bootstrap sass files into our own. It is also different than the standard CSS imports because in those cases, the server is actually making multiple calls to the server. With Sass, it just includes the imported files and makes one large CSS file.
- **Inheritance**: You can use the `@extend` directive to share styles from one selector to the other.
- **Operators**: Sass includes a set of mathematical operators, such as +, -, \*, /, which can be used to perform calculations on CSS values
- **Conditional statements**: Sass provides conditional statements like @if, @else if, and @else that allow you to apply different styles based on specific conditions.
- **Modularity and reusability**: With Sass, you can break your stylesheets into smaller, modular parts, making it easier to manage and reuse styles across multiple projects.

## Compiling Sass

In order to use Sass and in order for us to customize Bootstrap, we need to download it's source files, which are Sass files. Then we can override variables for things like colors, font sizes and just about anythin else.

There are many ways to compile Sass. Here are some popular options:

- Task managers (eg.Gulp & Grunt)
- Sass packages / command line tools (eg. sass, node-sass)
- Desktop applications like (eg. Koala)
- IDE & editor extensions (eg. Live Sass Compiler)
- Build tools (eg. Webpack, Parcel)

We will be using the `sass` package via `NPM (Node Package Manager)` This will allow us to run a command and build our CSS from our `.scss` files as well as a command to constantly watch our `.scss` files and compile them into CSS.

I will show you how to do this in the next lesson.
