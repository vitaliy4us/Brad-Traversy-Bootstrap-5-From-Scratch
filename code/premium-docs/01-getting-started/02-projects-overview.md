# A Look At The Projects

Let's take a quick look at the 5 main projects for this course. This is github repository with all of the code for the projects. Each project was created with a boilerplate or a starter template that we're going to build from scratch. The reason for this is because we need to use Sass in order to customize and compile our own Bootstrap CSS. So we'll be installing Bootstrap and Sass using NPM and creating some NPM scripts. Now if you have no clue what I'm talking about and you've never use NPM or Sass before, don't worry because we're going to build that starter template or boilerplate from scratch and I'm going to explain everything. This is the repository for what I call the `BS5 Simple Starter`. We'll build this before we start using it for the 5 websites.

Now Let's take a look at the sites.

## Ebook Website

The first website is an informational website for an ebook. This particular ebook is about starting a blog called Blog Mastery, but of course, you could change that to whatever you want. We have a basic navigation bar and with all of our projects aside from one, we'll have a sticky navbar and add a little bit of JavaScript so that when we scroll down the navbar then has a background so that it's still readable.

We have a main header/hero section with an image, text and simple form. There's a background image and we're using an svg image to give this wave effect at the bottom. Then we have some icon areas. We''ll be using Font Awesome throughout all of our projects for icons.

We have a details area where we will implement a modal. Same thing with the other details area. We have some testimonials and then another area with an email form. We have some social media icons and a simple footer.

By the way, I used ChatGPT to generate all the text content. So I think it's better than having lorem ipsum, but some if it may not make much sense. Which is ok because the text content is not what we're focused on.

As far as inner pages, we're going to add a contact page. Now even though this course is mainly about learning Bootstrap, we're actually going to deploy this project to Vercel. Not only that, but we're going to make this form work by using another service called FormSpree. These are absolutely free to use and this course is not sponsored at all.

## Corso Website

The next project is called Corso and is mainly focused on selling or giving away training courses or seminars, things like that. We have the same navbar effect with the background. In the header, we're going to implement the JavaScript carousel widget. We're also going to add a background image and we'll have a linear gradient with an overlay so that it darkens the image and makes the text readable. There will be a few ways that I show you how we can add overlays.

Under that we have a register form and some text with bullet points. Then we have some more informational areas. Some numbered points. A course summary. Then we have an invitation box with another image and overlay. We have some takeaways using cards along with stacked font awesome icons. Then we have a small newsletter or subscribe area and a 3 column footer.

We'll be utilizing Bootstraps grid columns, but we'll also look at other ways of aligning elements.

## Portfolio Website

Next we have a portfolio website. Now I used all of my own information here, just to personalize it. Of course, you can put your own information. So here we have a full viewport hero area with a overlay. We're going to add a little custom JavaScript here to give us the typing effect when we come to the page. If you don't know any JavaScript, don't worry about it. It's not a lot and I will explain it as we go.

We have some social icons at the bottom and a button to bring us to the about area.

In the about section, I have an image of me and my son. Of course, you can make this whatever you want. You can also change the text up.

Then we have a profile area with some info and icons. On the right we have some skill progress bars. Now, I do think that these are a little pointless, but I also think they look cool and it gave us an opportunity to use the progress bars.

Now for the projects we're actually going to use a 3rd party script called Lightbox. It's similar to a modal except we can actually group the images together and scroll through them.

I put a section to send a shout out to styleshout as they provided the assets and overall design for this project. We have some services, some stats, a form and a footer.

We're also going to deploy this project to Netlify and make this form work with Netlify forms.

## Yavin Office Design Website

Next we have the Yavin website, which is a company that designs office spaces. We have a navbar with a background effect. The header area will have some background images that we will position absolute. We will be writing some custom CSS for that. In fact all of the projects will have a little bit of custom CSS and media queries.

Under that we have some statistics and again, we're going to write some custom JavaScript to make these count up when we come to the website.

We have some text areas. Some bullet points and font awesome icons. This get started button will go to an inner article page. Here we have an inner page header, a main image and then some formatted text underneath along with a few cards. I just wanted to give you an option for an inner page layout.

Back on the home page, we have an icon area for services. The details text areas will also have the positioned background images. We have a get quote button and then some projects. I didn't add a modal here because we do that in the next project, but you could if you want.

Then we're going to add a testimonial slider with the Bootstrap Carousel widget. So these are testimonials. Then we have a contact form and footer.

Another thing we're going to do is add this back to top button. This will have soe custom CSS as well as some JavaScript.

## Vera Software Solutions Website

The final project will be a website for a software company, but you could really make it about anything. It's a dark theme with some good contrast. I like the header image and then we have this orange line positioned on the left, which is an svg. We have these positioned throughout the page. We'll be using a 3rd party script called replaceme.js and this allows us to scroll multiple words in one area. So we can have these words alternate. So little things like this, I thought was a nice touch on top of just learning Bootstrap.

Then we have some partner images. The number of logos changes based on the screen size. There is a register form and then a solutions area with some card images and badges. In the expertise area, we'll add some larger icons.

The video area will be a big part of this one. We're going to have this animated button. So this will take quite a bit of custom CSS as Bootstrap doesn't really have animation capabilities. We'll be using CSS keyframes and pseudo selectors. Then when we click on it, it will open a video in a modal. We will have to add a bit of javaScript for this.

Then we have a pricing grid and some projects. Each project will open it's own modal. Below that we have another subscribe form and simple footer.

Alright, so those are the projects that we have in store. I also want to mention that we partnered with htmlrev.com and styleshout.com, which are are websites that offer pre-made themes. They allowed us to use the core designs and assets for these projects. So I just want to give them a shout out. All the html, css and javascript was done by me, but they provided the assets.

Alright, so now that you've seen the Bootstrap projects, let's start talking about exactly what Bootstrap is.
