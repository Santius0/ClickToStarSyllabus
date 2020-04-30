# External CSS File

Let's create our new music page! First, create a new folder called `music`. Now inside that folder, create a new `index.html`. We can have one `index.html` file in each folder.

We won't put the song content as yet. For now, let's just see the header and footer that we had on the main page. Add this to the HTML file:

```html
<!DOCTYPE html>
<html>

<head>
    <title>Music - Marcus Sanatan</title>
</head>

<body>
    <div class="container">
        <header>
            <nav class="navbar">
                <div class="nav-home">
                    <a href="/" class="button home-button">Home</a>
                </div>
                <div class="nav-links">
                    <a href="/music/" class="button">Music</a>
                    <a href="https://www.facebook.com/msanatan" class="button" target="_blank">Facebook</a>
                </div>
            </nav>
        </header>
        <div id="main">
        </div>
        <footer>
            <div class="footer-wrapper">
                <p>&copy; Marcus Sanatan 2020 | <a href="mailto:me@msanatan.com">me@msanatan.com</a></p>
            </div>
        </footer>
    </div>
</body>

</html>
```

We have the more or less the same content, but it looks awfully plain does it? That's because we don't have the styles copied across.

We can copy and paste the styles, but we probably shouldn't. What we if we change our background colour from blue to green? We'll have to change it in 2 places. Now if our website had 5 pages, would you remember to change each one? It gets tedious when we have to copy and paste styles. At this point, we can put our styles in their own file.

Let's try it out:

1. Copy and paste all the CSS rules in the `style` tag from the main `index.html` (not in the music folder)
1. Create a new folder called `css`
1. In the `css` folder, create a new file called `styles.css`
1. Paste the CSS rules in `styles.css`
1. Delete the `style` tag in `index.html`
1. Now add the following `link` tag at the end of the `head` section:

```html
<link rel="stylesheet" href="css/style.css">
```

The `link` tag tells HTML to load a new file. In our case we're loading our CSS file we just created. We use `rel` to say what kind of file we're loading. Like with `a` tags, we use `href` to specify where the file is.

Our main website looks the same! Now let's add these styles to our Music page. In `music/index.html` add the following `link` tag at the end of `head`:

```html
<link rel="stylesheet" href="../css/style.css">
```

Note the `..` at the beginning of the path. That's how to say "the previous folder" in HTML. So that `href` tells the computer: go to the previous folder -> then go to the `css` folder -> and load `style.css`.

Our music page has the header and footer, awesome! Let's move on to the next section and add our favourite songs to the page.
