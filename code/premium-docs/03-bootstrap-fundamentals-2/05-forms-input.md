# Forms & Input

Forms and input are important not only because they allow users to interact with your website, but because by default they look horrible. Bootstrap makes them look good and provides a lot of functionality.

Let's create a basic login form with an email and password field as well as a remember me checkbox:

```html
<form>
  <div class="mb-3">
    <label for="email" class="form-label">Email address</label>
    <input type="email" class="form-control" id="email" />
    <div class="form-text">We'll never share your email with anyone else.</div>
  </div>
  <div class="mb-3">
    <label for="password" class="form-label">Password</label>
    <input type="password" class="form-control" id="password" />
  </div>
  <div class="mb-3 form-check">
    <input type="checkbox" class="form-check-input" id="remember" />
    <label class="form-check-label" for="remember">Remember Me</label>
  </div>
  <input type="submit" class="btn btn-primary" value="Submit" />
</form>
```

As you can see, we wrap our inputs and labels with a margin bottom class. This puts some space between the fields. The labels have a class of `form-label` and the inputs have a class of `form-control`. The checkbox has a class of `form-check-input` and the label for the checkbox has a class of `form-check-label`.

For the button, we used an input with the type of `submit`. We can still use all of the button classes on this.

## Select Fields

Let's look at some select fields. These should have the class of `form-select`. There are also multiple sizes that you can use.

```html
<form>
  <div class="mb-3">
    <select class="form-select">
      <option selected>Select a time to call</option>
      <option value="morning">Morning</option>
      <option value="afternoon">Afternoon</option>
      <option value="night">Night</option>
    </select>
  </div>
  <div class="mb-3">
    <select class="form-select form-select-lg">
      <option selected>Select a time to call</option>
      <option value="morning">Morning</option>
      <option value="afternoon">Afternoon</option>
      <option value="night">Night</option>
    </select>
  </div>
  <div class="mb-3">
    <select class="form-select form-select-sm">
      <option selected>Select a time to call</option>
      <option value="morning">Morning</option>
      <option value="afternoon">Afternoon</option>
      <option value="night">Night</option>
    </select>
  </div>
</form>
```

## Textarea

Textareas are very similar to inputs. They have a class of `form-control` and you can set the height with the `rows` attribute.

```html
<div class="mb-3">
  <label for="description" class="form-label">Example textarea</label>
  <textarea class="form-control" id="description" rows="3"></textarea>
</div>
```

## Switches

Switches work like checkboxes, but they look like switches. They have a class of `form-check form-switch`.

```html
<div class="form-check form-switch">
  <input
    class="form-check-input"
    type="checkbox"
    role="switch"
    id="switch-input"
  />
  <label class="form-check-label" for="switch-input"
    >Switch Checkbox Input</label
  >
</div>
```

## Inline Checkboxes & Radios

You can use the class of `form-check-inline` to make your checkboxes and radios inline.

```html
<div class="mb-3">
  <div class="form-check form-check-inline">
    <input class="form-check-input" type="checkbox" id="ch1" value="option1" />
    <label class="form-check-label" for="ch1">1</label>
  </div>
  <div class="form-check form-check-inline">
    <input class="form-check-input" type="checkbox" id="ch2" value="option2" />
    <label class="form-check-label" for="ch2">2</label>
  </div>
  <div class="form-check form-check-inline">
    <input
      class="form-check-input"
      type="checkbox"
      id="ch3"
      value="option3"
      disabled
    />
    <label class="form-check-label" for="ch3">3 (disabled)</label>
  </div>
</div>
```

## Button Toggle

You can use a button as a checkbox by using the class of `btn-check` on the button:

```html
<div class="mb-3">
  <input type="checkbox" class="btn-check" id="btn-check" autocomplete="off" />
  <label class="btn btn-primary" for="btn-check">Button toggle</label>
</div>
```

## Range

You can use the class of `form-range` to create a range slider.

```html
<div class="mb-3">
  <label for="range" class="form-label">Example range</label>
  <input type="range" class="form-range" id="range" />
</div>
```

You can also have steps that the range snaps to:

```html
<div class="mb-3">
  <label for="range2" class="form-label">Example range</label>
  <input
    type="range"
    class="form-range"
    min="0"
    max="5"
    step="0.5"
    id="range2"
  />
</div>
```

## Input Groups

You can also use input groups to add text or buttons to the left or right of your inputs. Let's add an @ symbol to the left of our input:

```html
<form>
  <div class="input-group mb-3">
    <span class="input-group-text">@</span>
    <input type="text" class="form-control" placeholder="Username" />
  </div>
</form>
```

Let's add some text to the right of the input:

```html
<form>
  <div class="input-group mb-3">
    <input
      type="text"
      class="form-control"
      placeholder="Recipient's username"
    />
    <span class="input-group-text">@example.com</span>
  </div>
</form>
```

Let's add a button to the right of the input:

```html
<form>
  <div class="input-group mb-3">
    <input type="text" class="form-control" placeholder="Enter your email" />
    <button class="btn btn-outline-secondary" type="button">Submit</button>
  </div>
</form>
```

As you can see, there are a lot of ways to style forms and inputs. In the next lesson, i want to look at form validation display.
