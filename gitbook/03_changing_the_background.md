# Changing the Background

What we're building?

![Screenshot of completed step](screenshot03.png)

Our page is pretty bland on many levels. Let's start sprucing it up with some colour. We can easily add CSS to HTML elements with their style attribute.

```html
<body>
    <div style="background-color: #11C9FF;">
        <img src="images/marcus.jpg" alt="Picture of me" width="300px">
        <h1>Marcus Sanatan</h1>
        <p>Musings of a little coder in the Caribbean</p>
    </div>
</body>
```

We encased all of our content with a `div` tag. As we'll be adding headers and footers later, it's a good idea to add divisions to your content as you develop your website.

We then added the `style` attribute to our div. We can use CSS within in HTML with that attribute. Our first attribute is `background-color`, which as the name suggests sets the background colour!

**Note:** CSS uses American spelling of words. When coding drop the 'u', use 'z' instead of 's' and be mindful of any other nuances between the US spelling and the UK spelling we use.

Hmm... there's some white space around our content. It's strange because we didn't add any whitespace there. Then who added it? Our browser did! Our browser thinks that a bit of whitespace is sensible for our content, and that's correct. The problem is that every browser makes that guess differently, sometimes it looks good and other times it doesn't look good.

It's a good practice to remove that white space, and any other styles the browser puts by default. This is called a *CSS Reset*. It helps make our site look the same across different browsers.

Let's do a basic CSS Reset by removing the whitespace in our HTML's `body`:

```html
<body style="margin: 0; padding: 0;">
```

Now our whitespace is gone!
