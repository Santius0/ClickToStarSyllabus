# IDs and Classes

What we're building?

![Screenshot of completed step](screenshot04.png)

As our webpage grows, we're need to find ways to identify elements. To get our content to take up the entire screen, we have to add a lot `div` tags. Different `divs` will have different styles, how can we tell them apart?

With HTML and CSS, we can give elements an ID or a class. An ID is a unique identifier for an HTML element. A class is also an identifier, but it's not unique. An HTML element can have many classes. A class can be used by many HTML elements.

Let's think about our website. The `div` we have now will has the background. Well, that background only applies for our main content. We'll likely only have one main section on our page, so we can assign an ID to that div:

```html
<div id="main">
    <img src="images/marcus.jpg" alt="Picture of me" width="300px">
    <h1>Marcus Sanatan</h1>
    <p>Musings of a little coder in the Caribbean</p>
</div>
```

To add an ID, add an `id` attribute in the `div`. Let's also change the CSS so that the background is now only applied to the HTML element with the "main" ID:

```html
<style>
    /* Reset CSS properties
    This helps make our style more consistent across browsers */
    * {
        margin: 0;
        padding: 0;
        border: 0;
    }

    /* Tell browsers that we want to use the entire page */
    html,
    body {
        width: 100%;
        height: 100%;
    }

    #main {
        background-color: #11C9FF;
    }
</style>
```

Note the `#` before the name of the ID. When writing CSS, we have to identify IDs with an asterisk.

Let's add a new style for the `banner-image` class. We want to give it a border, and display the image as a circle instead of a rectangle. In your `style` tag, add this to bottom:

```css
/* The banner image is a lovely circle */
.banner-image {
    border: 10px solid #EAEAEA;
    border-radius: 50%;
}
```

Note the `.` before the name of the class. We must identify classes that way in our CSS code. In our first line we add a thick, grey border to our image. We then define a `border-radius`, a property that determines how much the corners of our borders curve. You can experiment with the values, `50%` works for me!

So far so good, but still lots of room for improvement. There's a lot of free space on our website. Why? Most browsers calculate how large our content is, and only shows us what it's taking up.. Let's learn how to use CSS so our content takes up the entire page.
