# WebDevWorkSSSShop

## welcome to the world of web dev 😍

Websites are often built using 3 languages:

1. **HTML** (the structure of the website)
2. **CSS** (the design and layout of the website)
3. **JavaScript** (the "brains" of the website)

For example, on YouTube:
- HTML would be used to add content like links, videos, images, and text.
- CSS would be used to arrange everything on the page and style it with colors, fonts, and spacing.
- JavaScript would be used to make things interactive, like when the user presses play, pause, or next.
    
In this workshop, we'll be going through the basics of HTML and CSS!

### How to use this template!

1. Download the files as a ZIP file or clone the repository to your computer.
    - Click the green code button > Download ZIP at the bottom
2. Edit the HTML and CSS files to personalize your website with your own content, colors, fonts, and layout.
   - Update all the relevant links and images in the HTML to point to your own websites, social media profiles, and image files.
   - Replace the placeholder text and images with your own content.
3. Open *index.html* in your browser to preview your changes as you work!
   - use the `Live Preview` or `Live Server` extensions on VSCode to help you view your website while you work

### HTML (HyperText Markup Language)

#### Anatomy of an Element

```html
<h1 class="title">Hello World!</h1>
```

| Term        | Part            | Explanation     |
| ----------- | --------------- | --------------- |
| opening tag | `<h1>`          | Marks the start of the heading 1 element          |
| attribute   | `class="title"` | Additional value for a element, here, we give a class name to [style with CSS](#csscascadingstylesheets) later |
| content     | `Hello World`   | The main content that appears on the page         |
| closing tag | `</h1>`         | Marks the end of the heading 1 element            |

There are a lot of different elements, here are some of the basic ones:

- `<p></p>`: Paragraph, pretty much all your text goes in-between these
- `<h1></h1>`: Heading
    - There're multiple heading levels, from the biggest (`h1`) to smallest (`h6`)
- `<a></a>`: Links
    - The front-facing text goes into the content, in-between the tags
    - The link is stored as a `href` attribute:
        - `<a href="https://sfussss.org/">SSSS Website</a> 
- `<strong></strong>`: These make the content inside **bold**
- `<div></div>`: These don't do much alone, but they become very useful when you combine them with CSS

- Lists
    - `<ul></ul>` - **U**nordered **L**ist element (Bullet point)
    - `<ol></ol>` - **O**rdered **L**ist element (Numbered)
    - `<li></li>`: List item element, you have to nest these inside either of the two list elements above, see below for a demo

```html
<!-- Bullet point list of Seb's Groceries -->
<h1>Seb's Grocery List</h1>
<ul>
  <li>SSSSalad</li>
  <li>Dressssing</li>
  <li>SSSStrawberry</li>
</ul>
```

- Images
    - `<img src="" alt=""/>` is an exception and only has an opening tag, no closing tag
    - `src=""` specifies the path or URL of the image you want to display.
    - `alt=""` provides alternative text that describes the image for accessibility. It also appears if the image cannot load.

`<article>, <main>, <nav>, <footer>` are all semantic HTML elements that act as containers for content.
- HTML treats them similarly in terms of layout by default, but each element has a different meaning that describes the purpose of its content.
- Using these elements makes your code easier to read and understand for both developers and assistive technologies.
- Examples:
    - `<main>`: Contains the main content of the page.
    - `<nav>`: Contains navigation links.
    - `<article>`: Contains independent content, such as a blog post.
    - `<footer>`: Contains footer information, such as contact details or copyright information.

Just like any other programming language, HTML also have comments:

```html
<!-- This is a comment in HTML -->
```

#### HTML Skeleton

```html
<!DOCTYPE html>
<html lang="en">
<head>
    ...
    <title>My Page</title>
    ...
</head>

<body>
    <h1>Hello, world!</h1>
</body>

</html>
```

- `<!DOCTYPE html>` → tells the browser that we're using HTML5.
- `<html lang="en"></html>` → wraps all the HTML on the page and tells the browser that the page is written in English.
- `<head></head>` → contains information about the webpage, like its title, fonts, and links to CSS files.
- `<body></body>` → contains the content that appears on the webpage, like headings, paragraphs, images, and links.
- `<title></title>` → sets the title shown in the browser tab.

> [!NOTE]  
> The browser reads the HTML to figure out what content to display and how the elements are organized.
    

#### Nesting Elements

You can nest elements by placing one HTML element inside another. This helps you group related content and control how it is structured.

Example 1: Nesting elements in an article
```html
<article class="work-experience-item">
    <h2>Software Developer Intern</h2>
    <p>ABC Company | May 2026 – August 2026</p>
    <p>Developed web applications using HTML, CSS, and JavaScript.</p>
</article>
```

- `<article>` groups all the information about one work experience entry.
- `class="work-experience-item"` gives the element a class that you can target with CSS to style all your work experience entries consistently.
- The `<h2>` and`<p>` elements are nested inside the `<article>` element.

Example 2: Making an image clickable

You can nest an `<img>` element inside an `<a>` element to make an image clickable. Clicking the image will take the user to the link specified by href.

```html
<a href="https://www.google.com">
    <img src="images/cat.jpg" alt="A cat sitting on a chair">
</a>
```

- `<a href="">` creates a link to another page or website.
- `<img src="">` displays the image.
- Nesting the `<img>` inside the `<a>` makes the image itself clickable.
Tip: The opening and closing tags must be properly nested. Close the inner element before closing the outer element.

### CSS (Cascading Style Sheets)

CSS is used to style HTML elements by changing things like their colors, fonts, sizes, and spacing.

```css
h1 {
    color: #24a98b;
}
```

|Term|Part|Explanation  |
|----|----|-------------|
|selector |`h1`      |selects all `<h1>` elements on the page|
|property |`color`   |specifies what property we want to change|
|value    |`#24a98b` |sets the text color to a shade of green|

#### More into selectors

Selectors don't anyways need to be a single element, you can use classes to apply your style across different elements.

Recall:

```html
<h1 class="title">Hello World!</h1>
```

We can style this by "selecting" the `title` class:

```css
/* Both of these do the same thing to the html above! */

/* For class attributes, we use the period (.) */
.class {
    color: #24a98b;
}

h1 {
    color: #24a98b;
}
```

> [!TIP]
> You can apply multiple classes to a single HTML element, for instance:
> ```html
> <h1 class="class-1 class-2 class-3">SSSSo many classsses! - Seb</h1>
> ```

---

As you go through and edit `index.html`, you may notice HTML attributes named `id`, these are kind of similar to classes,
but you can only have one `id` per element. You would use these for the header or footer, whereas classes are used for
things that show more often, like a project item.

For example:

```html
<p id="intro" class="main">Some may say that the SSSS actually stands for the Seb Seb Seb Society...</p>
```

```css
/* for id attributes, we use a hashtag (#) */
#id {
    color: #00ff00;
}

/* ids override classes if an element has both */
/* Our paragraph text would still be green (#00ff00) */
/* However, the background colour of our paragraph would be dark grey (#303030) since nothing is overriding it */
.main {
    color: #000000;
    background-color: #303030;
}
```

---

Believe it or not, you can be *even more specific*, for example:

- `p.main`
    - Only apply to `<p>` elements that have the `main` class
- `article.project-item > h3`
    - Only apply to `<h3>` elements that are nested inside the `<article>` element that has the `project-item` class

#### The Box Model

Every HTML element can be thought of as a box. The CSS box model describes the different layers that make up that box:

- Content → the actual text or image inside the element.   
- Padding → the space between the content and the border.
- Border → the outline around the element.
- Margin → the space outside the border, separating the element from other elements.
    
![Nested boxes, from outermost to innermost; margin, border, padding, content](box-model.png)

### CSS Sizing Units

CSS units control the size of elements, text, spacing, and containers.

| Unit | Description | Example |
|---|---|---|
| `px` | Fixed CSS pixel size | `width: 300px;` |
| `%` | Relative to the parent element's size, depending on the property | `width: 80%;` |
| `em` | Relative to the element's font size (or inherited font size, depending on the property) | `padding: 1em;` |
| `rem` | Relative to the root (`html`) font size, usually 16px by default | `font-size: 2rem;` |
| `vw` | 1% of the viewport width | `width: 100vw;` |
| `vh` | 1% of the viewport height | `height: 100vh;` |

Example:
```css
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

Which unit should you use?
- `px`: Precise sizes, such as borders and small icons.
- `%`: Responsive widths relative to a parent element.
- `em` and `rem`: Text sizes and spacing that scale with font size.
- `vw` and `vh`: Sizes based on the browser window.

**Tip:** Use `%`, `rem`, and viewport units to help create responsive websites that adapt to different screen sizes.

#### Changing Fonts

1. Choose a font from [Google Fonts](https://fonts.google.com/).
2. Select the font style you want to use and copy the HTML `<link>` code from the font's page.
3. Add the `<link>` code inside the `<head>` section of your HTML file.
4. Use the font's name in your CSS with the `font-family` property.
    
Example:

Add this inside your HTML `<head>`:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com"crossorigin>
<link href="https://fonts.googleapis.com/css2family=Robotodisplay=swap" rel="stylesheet">
```

Then use the font in your CSS:

```css
body {
    font-family: 'Roboto', sans-serif;
}
```

#### Color Palettes

- Use [Coolors](https://coolors.co/) to find color palettes that work well together.
- Copy the hex codes for the colors you want to use (for example, `#24a98b`).
- To make it easier to change colors across your website, you can store them in CSS variables and reuse them throughout your styles.
    
Example:

```css
/* CSS Variables */
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

- `:root`: defines variables that can be used throughout the stylesheet.
- `--primary-color`: the name of a variable that stores a color.
- `var(--primary-color)`: uses the color stored in that variable.

If you want to try a different color palette later, you can simply change the values in `:root` instead of updating every CSS rule individually.

## Things to look into after the workshop!!

- **Favicons** → add a small icon that appears in the browser tab next to your website's title.
- **Changing up the style of your website!** → experiment with different fonts, colors, layouts, animations, and hover effects to add your own style to the website!
- **Adding more pages**→ create additional *separate* pages for things like an About Me section, projects, hobbies, or a contact page, and link them together using navigation links.
- **Adding a light or dark mode** → let users switch between light and dark themes.
- **Deploying your website** → publish your website online so other people can visit it using a link!
