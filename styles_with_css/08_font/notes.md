# Font

What we say and how it's said is very important \- in life! On a website, how it looks matter as well. Fonts are an intricate part of web design. With CSS, we can change the font of our text to match the theme of our site.

Let's begin by downloading a special font for our website \- Dosis. You can get it here <https://www.fontsquirrel.com/fonts/dosis>. Save the file as `dosis.otf` and put it in a new `fonts` folder.

You directory should look like this:

```plaintext
|- fonts
    - dosis.otf
|- images
    - your-image.jpg
|- index.html
```

The following styles are to applied to one area of the our website, the text around the images. To keep things organised, we'll add a new `div` that encapsulates our `img`, `h1` and `p` tags. This `div` will have a new class \- banner. Change your HTML so it now has this:

```html
<div id="main">
    <div class="banner">
        <img class="banner-image" src="images/marcus.jpg" alt="Picture of me" width="300px">
        <h1>Marcus Sanatan</h1>
        <p>Musings of a little coder in the Caribbean</p>
    </div>
</div>
```

**Notice** how the text is no longer centre aligned. That's because our the `h1` and `p` tags were previously children of `#main`, making them flex items. Now they're children of `.banner`, and no longer flex items.

Let's quickly fix this. In your `style` tag, let's add a new class for "banner" and centre all of its text:

```css
.banner {
    text-align: center;
}
```

You just created a new CSS style for the banner class with the `text-align` property. As you expect, that property determines how the text is written in our `div`. In this case, our text grows from the centre.

Good work! Before we can use our new font we need to load it. In your `style` tag, add this bit of CSS code to load the Dosis font:

```css
/* Load custom fonts */
@font-face {
    font-family: Dosis;
    src: url('./fonts/dosis.otf');
}
```

The `@font-face` keyword is used to add a new font to our website. We need two pieces of information to load a font successfully:

* `font-family` \- is the name we'll use to reference this font later.
* `src` \- is the location of the font file. We can load fonts that we save locally, or fonts that are freely available online! You do need to put the location of the font in the `url()` function.

Let's actually use this new font of ours now. Add the following line to the `.banner` CSS styles:

```css
font-family: Dosis, Helvetica, sans-serif;
```

Now our page uses the Dosis font we loaded earlier! Much better. You'd notice that we added 3 fonts, why is that? Some fonts work with well with all browsers, others only work well in a few. To ensure that our website has some decent to dispaly, we add *fallback font options*.

Let's say for some reason our Dosis font can't be loaded or displayed. The website will then try the `Helvetica` font, a common one most browsers have. If a browser does not have Helvitica, it would try `sans-serif` \- a default font for the browsers.

While our font looks better, the colour really isn't fitting into what we want to build. Let's change the colour of all text in our banner `div`. Add this to `.banner`:

```css
color: #ffffff;
```

The `color` property (note the US spelling of the word) specifies the colour of text in an HTML element. As CSS cascades, it defines the colour of all sub-elements unless they define their own `color` property.

The value `#ffffff` is another way of saying `white`. Since we use 6 hexadecimal numbers for the our `background-color`, we use this way to define white to be consistent.

Part of choosing fonts is selecting the right size for them. This is our banner text, the main thing that a user sees when they go on our website. We want something massive that really hits them as they open it.

Let's add a couple of rules to make our text bigger. In your `style` tag, add the following:

```css
.banner h1 {
    font-size: 144px;
}

.banner p {
    font-size: 32px;
}
```

You've just written your first cascading style! By using `.banner h1`, we're telling our browser that we want to apply the styles to all `h1` tags that's contained within an HTML element with the `banner` class. We do the same for the `p` tags with `.banner p`.

We set the `font-size` property, which as you expect determines the size of the text. Larger values make for bigger font. When describing the font for the `h1` we say our text is 144 pixels big. A pixel is a single dot on our screen. That's why we have `px` at the end of the number.

Our main site looks awesome! Let's spruce it up a bit more with a footer.
