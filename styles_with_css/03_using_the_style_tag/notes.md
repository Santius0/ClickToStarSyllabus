# Using the style Tag

Let's be honest, our code is starting to look a bit ugly already. Inline styles are good for quick fixes, but are seldom used in real websites. It's better to have CSS separate from HTML code to make changes easy to make.

Instead of adding a `style` **attribute** with our CSS to each HTML element, we can add a `style` **tag** in our `head` tag that will contain all our styles. Therefore, when we want to adjust a style for all tags, we only need to look at one place.

First, let's remove the in-line CSS we had before:

```html
<body>
    <div>
        <img src="images/marcus.jpg" alt="Picture of me" width="300px">
        <h1>Marcus Sanatan</h1>
        <p>Musings of a little coder in the Caribbean</p>
    </div>
</body>
```

Now, in our `head` tag, let's re-add the CSS in one `style` tag:

```html
<head>
    <title>Marcus Sanatan</title>
    <style>
        body {
            margin: 0;
            padding: 0;
        }

        div {
            background-color: #11C9FF;
        }
    </style>
</head>
```

Awesome! Our website is the same but as CSS grows it's much easier to change.
