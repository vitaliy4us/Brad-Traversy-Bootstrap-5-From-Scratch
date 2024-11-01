# Typing Effect

In this video, we will add some JavaScript to create a typing effect for the main header. I want to stress that this is not a JavaScript course, so if you do not understand it, that's fine.

The first thing we will do is remove the text from the header "I am YOUR NAME". This will be added dynamically with JavaScript.

Now, open the `script.js` file. It should already be imported in the `index.html` file.

Add the following code:

```js
// Function to run the typing effect on page load
function runTypingEffect() {
  const text = 'I am Brad Traversy.';
  const typingElement = document.getElementById('typing-text');
  const typingDelay = 100; // Delay between each character (in milliseconds)

  typeText(text, typingElement, typingDelay);
}
```

I will explain briefly what we are doing here:

We are creating a function called `runTypingEffect` that will run when the page loads. Inside of this function, we are creating a variable called `text` that contains the text we want to type out. We are also creating a variable called `typingElement` that contains the element we want to type the text into. In this case, it is the `h1` element with the id of `typing-text`. Finally, we are creating a variable called `typingDelay` that contains the delay between each character. This is in milliseconds, so 1000 is 1 second.

We then run a function called `typeText` that we will create next. This function will take in the text, the element, and the delay as arguments.

Add this above the `runTypingEffect` function:

```js
// Function to simulate typing effect
function typeText(text, typingElement, delay) {
  for (let i = 0; i < text.length; i++) {
    setTimeout(() => {
      typingElement.textContent += text.charAt(i);
    }, delay * i);
  }
}
```

Here we are creating a function called `typeText` that takes in the text, the element, and the delay as arguments. We are then looping through the text and adding a delay to each character. This will simulate a typing effect.

Finally, we need to run the `runTypingEffect` function when the page loads. Add this to the bottom of the `script.js` file:

```js
// Run the typing effect when the DOM is loaded
document.addEventListener('DOMContentLoaded', runTypingEffect);
```

Now, if you save and reload the page, you should see the typing effect.
