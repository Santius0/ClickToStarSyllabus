# Better CSS Reset

While we're here, let's do a better CSS Reset. The browsers don't just add random whitespace to our `body`, but to the `html` tag and other ones we haven't even used as yet!

Our better reset will elimate those spaces once and for all. Change your `style` tag so it has this:

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
    html, body {
        width: 100%;
        height: 100%;
    }

    div {
        background-color: #11C9FF;
    }
</style>
```

Let's go over the new things we're seeing. First, it's the text in `/* */`. These are comments in CSS. They don't change how the website looks or behaves. They're text written by humans to help us understand what's going on.

Our first new style is for `*`. We've never used a `*` tag in our website... what does it do? Well, `*` stands for everything i.e. all possible tags. In this case, we're tell our browser to remove all margins, padding and borders from all our elements.

We then tell our browser to ensure that the `html` tag and the `body` tag use the entire width and height available on the page.
