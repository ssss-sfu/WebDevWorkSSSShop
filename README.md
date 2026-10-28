# WebDevWorkSSSShop

## Welcome to the world of web dev 😍

Websites are often built using three languages:

1.  **HTML**: The structure of the website.
2.  **CSS**: The design and layout of the website.
3.  **JavaScript**: The "brains" of the website.

For example, on YouTube:

-   HTML adds content like links, videos, images, and text.
-   CSS arranges everything on the page and styles it with colors,
    fonts, and spacing.
-   JavaScript makes things interactive, like when the user presses
    play, pause, or next.

In this workshop, we'll go through the basics of HTML and CSS!

## How to use this template

1.  Download the files as a ZIP file or clone the repository to your
    computer.
    -   Click the green **Code** button, then select **Download ZIP**.
2.  Edit the HTML and CSS files to personalize your website with your
    own content, colors, fonts, and layout.
    -   Update the relevant links and images in the HTML to point to
        your own websites, social media profiles, and image files.
    -   Replace the placeholder text and images with your own content.
3.  Open `index.html` in your browser to preview your changes as you
    work.
    -   The **Live Preview** or **Live Server** extensions in VS Code
        can help you view your website while you work.

------------------------------------------------------------------------

# HTML (HyperText Markup Language)

HTML provides the structure and content of a webpage.

## HTML skeleton

A typical HTML page looks like this:

``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>My Page</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>
    <h1>Hello, world!</h1>
</body>
</html>
```

-   `<!DOCTYPE html>` tells the browser that we're using HTML5.
-   `<html lang="en">` wraps all the HTML on the page and tells the
    browser that the page is written in English.
-   `<head>` contains information about the webpage, like its title,
    fonts, and links to CSS files.
-   `<body>` contains the content that appears on the webpage, like
    headings, paragraphs, images, and links.
-   `<title>` sets the title shown in the browser tab.

> \[!NOTE\] The browser reads the HTML to figure out what content to
> display and how the elements are organized.

## Anatomy of an element

HTML elements usually have an opening tag, content, and a closing tag.
They can also have attributes that provide extra information.

``` html
<h1 class="title">Hello World!</h1>
```

  | Term | Part | Explanation |
|-------|------|-------------|
| Opening tag | `<h1>` | Marks the start of the heading element. |
| Attribute | `class="title"` | Gives the element a class name that we can [style with CSS](#css-cascading-style-sheets) later. |
| Content | `Hello World!` | The content that appears on the page. |
| Closing tag | `</h1>` | Marks the end of the heading element. |

## Common HTML elements

Here are some basic elements you'll use when building your website:

-   `<p></p>`: A paragraph. Most text goes between these tags.
-   `<h1></h1>`: A heading. There are multiple heading levels, from `h1`
    to `h6`.
-   `<a></a>`: A link.
    -   The text users see goes between the tags.
    -   The destination is stored in the `href` attribute.

    ``` html
    <a href="https://sfussss.org/">SSSS Website</a>
    ```
-   `<strong></strong>`: Makes the content inside bold, usually
    indicating that it is important.
-   `<div></div>`: A general-purpose container that becomes especially
    useful when combined with CSS.

### Lists

-   `<ul></ul>`: An **unordered list**, usually shown with bullet
    points.
-   `<ol></ol>`: An **ordered list**, usually shown with numbers.
-   `<li></li>`: A list item. List items should be nested inside a
    `<ul>` or `<ol>`.

Example:

``` html
<!-- Bullet point list of Seb's groceries -->
<h1>Seb's Grocery List</h1>
<ul>
    <li>SSSSalad</li>
    <li>Dressssing</li>
    <li>SSSStrawberry</li>
</ul>
```

### Images

The `<img>` element displays an image. It is a void element, which means
it does not need a closing tag.

-   `src=""` specifies the path or URL of the image you want to display.
-   `alt=""` provides alternative text that describes the image for
    accessibility. It can also appear if the image cannot load.

``` html
<img src="images/seb.jpg" alt="SSSSebastian the SSSSnake">
```

### Semantic HTML elements

`<main>`, `<nav>`, `<article>`, and `<footer>` are semantic HTML
elements that act as containers for content.

HTML treats them similarly in terms of layout by default, but each
element has a different meaning that describes the purpose of its
content. Using them makes your code easier to read and understand for
both developers and assistive technologies.

-   `<main>`: Contains the main content of the page.
-   `<nav>`: Contains navigation links.
-   `<article>`: Contains independent content, such as a blog post.
-   `<footer>`: Contains footer information, such as contact details or
    copyright information.

### Nesting elements

You can nest elements by placing one HTML element inside another. This
helps you group related content and control how it is structured.

**Example 1: Nesting elements in an article**

``` html
<article class="work-experience-item">
    <h2>Software Developer Intern</h2>
    <p>ABC Company | May 2026 – August 2026</p>
    <p>Developed web applications using HTML, CSS, and JavaScript.</p>
</article>
```

-   `<article>` groups all the information about one work experience
    entry.
-   `class="work-experience-item"` gives the element a class that you
    can target with CSS to style work experience entries consistently.
-   The `<h2>` and `<p>` elements are nested inside the `<article>`
    element.

**Example 2: Making an image clickable**

You can nest an `<img>` element inside an `<a>` element to make an image
clickable. Clicking the image takes the user to the link specified by
`href`.

``` html
<a href="https://sfussss.org">
    <img src="images/seb.jpg" alt="SSSSebastian the SSSSnake">
</a>
```

-   `<a href="">` creates a link to another page or website.
-   `<img src="">` displays the image.
-   Nesting the `<img>` inside the `<a>` makes the image itself
    clickable.

> \[!TIP\] Make sure your elements are properly nested. Close the inner
> element before closing the outer element.

### HTML comments

You can add comments to HTML to leave notes for yourself or other
developers. Comments don't appear on the webpage.

``` html
<!-- This is a comment in HTML -->
```

------------------------------------------------------------------------

# CSS (Cascading Style Sheets)

CSS is used to style HTML elements by changing things like their colors,
fonts, sizes, spacing, and layout.

## Ways to Add CSS

There are three ways to add CSS to your HTML:

1.  Inline CSS -> Add CSS directly to an HTML element using the style
    attribute.

``` html
<p style="color: pink;">Hello, world!</p>
```

2.  Internal CSS -> Write CSS inside a `<style>` tag in the HTML
    document, usually in the `<head>`.

``` html
<head>
  <style>
    p {
      color: pink;
    }
  </style>
</head>
```

3.  External CSS -> Write CSS in a separate .css file and link it to
    your HTML. This is the recommended approach for keeping your code
    organized!

``` html
<head>
  <link rel="stylesheet" href="style.css">
</head>
```

### We will be using External CSS for our websites today!

To add CSS, create a separate `style.css` file and link it inside the
`<head>` of your HTML file:

``` html
<link rel="stylesheet" href="style.css">
```

Then, write your CSS in `style.css`:

``` css
h1 {
    color: #24a98b;
}
```

| Term | Part | Explanation |
|------|------|-------------|
| Selector | `h1` | Selects all `<h1>` elements on the page. |
| Property | `color` | Specifies what we want to change. |
| Value | `#24a98b` | Sets the text color to a shade of green. |

## CSS selectors

Selectors let you choose which HTML elements to style. You can select
elements by their tag, class, ID, or relationship to other elements.

### Element selectors

Select all elements of a particular type.

``` css
h1 {
    color: #24a98b;
}
```

### Class selectors

Classes let you apply the same styles to multiple elements, even if they
are different types of elements.

For example, this HTML gives both elements the `title` class:

``` html
<h1 class="title">Hello World!</h1>
<p class="title">Welcome to my website!</p>
```

We can select both elements using `.title`:

``` css
.title {
    color: #24a98b;
}
```

> \[!TIP\] You can apply multiple classes to a single HTML element by
> separating them with spaces.
>
> ``` html
> <h1 class="title highlight large">Hello World!</h1>
> ```
>
> Each class can be used to apply different styles to the same element.

### ID selectors

IDs are similar to classes, but each ID should be unique within a page.
They are useful for identifying a specific element.

``` html
<p id="intro" class="main">
    Welcome to my website!
</p>
```

Use `#` to select an ID:

``` css
#intro {
    color: #00ff00;
}
```

### Combining selectors

You can combine selectors to target elements more precisely.

``` css
/* Selects only <p> elements with the "main" class */
p.main {
    color: #24a98b;
}

/* Selects <h3> elements directly inside an article with the "project-item" class */
article.project-item > h3 {
    color: #b5838d;
}
```

### What happens when styles conflict?

CSS uses specificity to decide which rule wins when multiple rules
target the same element and property. IDs are generally more specific
than classes, and classes are more specific than element selectors. If
specificity is equal, the rule that comes later usually wins.

### CSS Comments
Comments in CSS are written like this:
```css
/* Seb Loves SoSy!!! */
```

## The CSS box model

Every HTML element can be thought of as a box. The CSS box model
describes the different layers that make up that box.

-   **Content:** The actual text, image, or other content inside the
    element.
-   **Padding:** The space between the content and the border.
-   **Border:** The outline surrounding the padding and content.
-   **Margin:** The space outside the border that separates the element
    from other elements.

![CSS box model showing margin, border, padding, and
content](box-model.png)

Example:

``` css
.card {
    padding: 20px;
    border: 2px solid black;
    margin: 16px;
}
```

-   `padding: 20px` adds space inside the border.
-   `border: 2px solid black` adds a 2px black border.
-   `margin: 16px` adds space outside the border.

### Using the browser Inspector

You can inspect and experiment with CSS directly in your browser without
changing your files.

1.  Right-click an element on your website.
2.  Select **Inspect**.
3.  Find its CSS rules in the Styles panel.
4.  Try changing properties like `color`, `padding`, or `margin`.
5.  See how the changes affect your website.

Changes made in the Inspector are temporary. Update your CSS file to
keep them!

## CSS sizing units

CSS units control the size of elements, text, spacing, and containers.
Some units use fixed sizes, while others adjust based on the parent
element or browser window.

| Unit | Description | Example |
|------|-------------|---------|
| `px` | A fixed CSS pixel size | `width: 300px;` |
| `%` | Relative to another size, often the parent element | `width: 80%;` |
| `em` | Relative to the relevant font size | `padding: 1em;` |
| `rem` | Relative to the root (`html`) font size | `font-size: 2rem;` |
| `vw` | 1% of the viewport width | `width: 100vw;` |
| `vh` | 1% of the viewport height | `height: 100vh;` |Example:

``` css
.container {
    width: 80%;
    max-width: 1000px;
    padding: 1rem;
}

h1 {
    font-size: 2rem;
}

.hero {
    min-height: 100vh;
}
```

**Which unit should you use?**

-   `px`: Precise sizes, such as borders and small icons.
-   `%`: Responsive sizing relative to a parent element.
-   `em` and `rem`: Text sizes and spacing that scale with font size.
-   `vw` and `vh`: Sizes based on the browser viewport.

> \[!TIP\] Use relative units to help your website adapt to different
> screen sizes. You can also use `min-width`, `max-width`, `min-height`,
> and `max-height` to control an element's dimensions.

## Changing fonts

You can use custom fonts to give your website a more personalized look.

1.  Choose a font from [Google Fonts](https://fonts.google.com/).
2.  Select the font style you want and copy the provided `<link>` code.
3.  Add the code inside the `<head>` section of your HTML file.
4.  Use the font's name in your CSS with `font-family`.

For example, to use Roboto, add the following inside your HTML `<head>`:

``` html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Roboto&display=swap" rel="stylesheet">
```

Then use it in your CSS:

``` css
body {
    font-family: 'Roboto', sans-serif;
}
```

The `sans-serif` part provides a fallback font in case Roboto cannot be
loaded.

## Color palettes and CSS variables

Choosing a color palette can help make your website look more
consistent.

-   Use [Coolors](https://coolors.co/) to find color palettes that work
    well together.
-   Copy the hex codes for the colors you want, such as `#24a98b`.
-   Store frequently used colors in CSS variables so you can reuse them
    throughout your stylesheet.

Example:

``` css
/* Define reusable CSS variables */
:root {
    --primary-color: #24a98b;
    --background-color: #f5f5f5;
    --text-color: #333333;
}

h1 {
    color: var(--primary-color);
}

body {
    background-color: var(--background-color);
    color: var(--text-color);
}
```

-   `:root` defines variables that can be accessed throughout the
    stylesheet.
-   `--primary-color` is a custom variable that stores a color.
-   `var(--primary-color)` retrieves the value stored in that variable.

If you want to try a different color palette later, you can change the
values in `:root` instead of updating every CSS rule individually.

## Responsive web design

Responsive web design means making your website look good on different
screen sizes, including phones, tablets, and desktops.

### Media queries

Media queries let you apply different CSS styles depending on conditions
such as the viewport width.

``` css
.container {
    width: 80%;
    margin: 0 auto;
}

/* Apply these styles on smaller screens */
@media (max-width: 600px) {
    .container {
        width: 95%;
    }
}
```

When the viewport is 600px wide or smaller, the container takes up 95%
of its parent's width instead of 80%.

### Using `clamp()`

The `clamp()` function lets you set a minimum, preferred, and maximum
value for a CSS property. The value adjusts when the available space
changes, without going below the minimum or above the maximum.

``` css
h1 {
    font-size: clamp(1.5rem, 4vw, 3rem);
}
```

-   **Minimum (`1.5rem`):** The smallest the text can be.
-   **Preferred (`4vw`):** The value that adjusts with the viewport
    width.
-   **Maximum (`3rem`):** The largest the text can be.

This is useful for creating responsive text and spacing without needing
as many media queries.

### More CSS stuff to look into!

Once you're comfortable with the basics of CSS, here are some useful topics to explore to make your websites more interactive and visually appealing!

- **Flexbox:** Arrange and align elements in a row or column, making it easier to create flexible layouts.
- **CSS Grid:** Create two-dimensional layouts with rows and columns, great for organizing sections of a webpage.
- **Transitions:** Add smooth visual changes when an element's style changes, such as a button changing color when you hover over it.
- **Animations:** Create more complex movements and visual effects using `@keyframes`, such as a loading spinner or a bouncing element.
- **Pseudo-classes:** Style elements based on their state, such as `:hover`, `:focus`, and `:active`.

These are all used in our starter code and great next steps for experimenting with CSS!

------------------------------------------------------------------------

## Things to look into after the workshop!

-   **Favicons** → Add a small icon that appears in the browser tab next
    to your website's title.
-   **Changing up your website's style** → Experiment with different
    fonts, colors, layouts, animations, and hover effects to add your
    own style to the website!
-   **Adding more pages** → Create additional, separate pages for things
    like an About Me section, projects, hobbies, or a contact page, and
    link them together using navigation links.
-   **Adding a light or dark mode** → Let users switch between light and
    dark themes.
-   **Deploying your website** → Publish your website online so other
    people can visit it using a link!

