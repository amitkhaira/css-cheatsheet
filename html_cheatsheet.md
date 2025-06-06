# HTML Cheat Sheet

## Basic HTML Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page Title</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Content goes here -->
    <script src="script.js"></script>
</body>
</html>
```

## Head Elements

```html
<!-- Essential meta tags -->
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Page description">
<meta name="keywords" content="keyword1, keyword2">
<meta name="author" content="Author Name">

<!-- Title and favicon -->
<title>Page Title</title>
<link rel="icon" href="favicon.ico">

<!-- CSS and fonts -->
<link rel="stylesheet" href="styles.css">
<link rel="preconnect" href="https://fonts.googleapis.com">

<!-- JavaScript -->
<script src="script.js"></script>
<script src="script.js" defer></script>
<script src="script.js" async></script>

<!-- Open Graph (social media) -->
<meta property="og:title" content="Page Title">
<meta property="og:description" content="Page description">
<meta property="og:image" content="image.jpg">
```

## Text Elements

### Headings
```html
<h1>Main Heading</h1>
<h2>Sub Heading</h2>
<h3>Sub Sub Heading</h3>
<h4>Minor Heading</h4>
<h5>Small Heading</h5>
<h6>Smallest Heading</h6>
```

### Paragraphs & Text
```html
<p>Paragraph text</p>
<br>                    <!-- Line break -->
<hr>                    <!-- Horizontal rule -->
<pre>Preformatted text</pre>
<blockquote>Quote text</blockquote>
<code>Inline code</code>
<kbd>Keyboard input</kbd>
<samp>Sample output</samp>
<var>Variable</var>
```

### Text Formatting
```html
<strong>Strong text</strong>        <!-- Important -->
<b>Bold text</b>                   <!-- Visual only -->
<em>Emphasized text</em>           <!-- Important -->
<i>Italic text</i>                 <!-- Visual only -->
<u>Underlined text</u>
<s>Strikethrough text</s>
<mark>Highlighted text</mark>
<small>Small text</small>
<sub>Subscript</sub>
<sup>Superscript</sup>
```

## Lists

### Unordered List
```html
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>
```

### Ordered List
```html
<ol>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
</ol>

<ol type="A">           <!-- A, B, C -->
<ol type="I">           <!-- I, II, III -->
<ol start="5">          <!-- Start from 5 -->
```

### Description List
```html
<dl>
    <dt>Term 1</dt>
    <dd>Description 1</dd>
    <dt>Term 2</dt>
    <dd>Description 2</dd>
</dl>
```

## Links & Navigation

```html
<!-- Basic link -->
<a href="https://example.com">External Link</a>
<a href="/page.html">Internal Link</a>
<a href="#section">Anchor Link</a>
<a href="mailto:email@example.com">Email Link</a>
<a href="tel:+1234567890">Phone Link</a>

<!-- Link attributes -->
<a href="url" target="_blank">New Tab</a>
<a href="url" download>Download File</a>
<a href="url" rel="noopener noreferrer">Secure Link</a>

<!-- Navigation -->
<nav>
    <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/about">About</a></li>
        <li><a href="/contact">Contact</a></li>
    </ul>
</nav>
```

## Images & Media

### Images
```html
<img src="image.jpg" alt="Description" width="300" height="200">
<img src="image.jpg" alt="Description" loading="lazy">

<!-- Responsive images -->
<img src="small.jpg" 
     srcset="small.jpg 300w, medium.jpg 600w, large.jpg 900w"
     sizes="(max-width: 300px) 280px, (max-width: 600px) 580px, 880px"
     alt="Description">

<!-- Picture element -->
<picture>
    <source media="(min-width: 800px)" srcset="large.jpg">
    <source media="(min-width: 400px)" srcset="medium.jpg">
    <img src="small.jpg" alt="Description">
</picture>
```

### Audio & Video
```html
<!-- Audio -->
<audio controls>
    <source src="audio.mp3" type="audio/mpeg">
    <source src="audio.ogg" type="audio/ogg">
    Your browser does not support audio.
</audio>

<!-- Video -->
<video width="320" height="240" controls>
    <source src="video.mp4" type="video/mp4">
    <source src="video.webm" type="video/webm">
    Your browser does not support video.
</video>

<!-- Embedded content -->
<iframe src="https://www.youtube.com/embed/VIDEO_ID" 
        width="560" height="315" frameborder="0">
</iframe>
```

## Tables

```html
<table>
    <caption>Table Caption</caption>
    <thead>
        <tr>
            <th>Header 1</th>
            <th>Header 2</th>
            <th>Header 3</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Data 1</td>
            <td>Data 2</td>
            <td>Data 3</td>
        </tr>
        <tr>
            <td colspan="2">Spans 2 columns</td>
            <td>Data 3</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td>Footer 1</td>
            <td>Footer 2</td>
            <td>Footer 3</td>
        </tr>
    </tfoot>
</table>
```

## Forms

### Basic Form
```html
<form action="/submit" method="POST">
    <!-- Text inputs -->
    <input type="text" name="username" placeholder="Username" required>
    <input type="email" name="email" placeholder="Email" required>
    <input type="password" name="password" placeholder="Password" required>
    <input type="tel" name="phone" placeholder="Phone">
    <input type="url" name="website" placeholder="Website">
    
    <!-- Other inputs -->
    <input type="number" name="age" min="1" max="100">
    <input type="date" name="birthdate">
    <input type="time" name="appointment">
    <input type="color" name="favorite-color">
    <input type="file" name="upload" accept="image/*">
    <input type="range" name="rating" min="1" max="10">
    
    <!-- Textarea -->
    <textarea name="message" rows="4" cols="50" placeholder="Message"></textarea>
    
    <!-- Select dropdown -->
    <select name="country">
        <option value="">Choose country</option>
        <option value="us">United States</option>
        <option value="uk">United Kingdom</option>
        <option value="ca">Canada</option>
    </select>
    
    <!-- Radio buttons -->
    <input type="radio" id="male" name="gender" value="male">
    <label for="male">Male</label>
    <input type="radio" id="female" name="gender" value="female">
    <label for="female">Female</label>
    
    <!-- Checkboxes -->
    <input type="checkbox" id="newsletter" name="newsletter" value="yes">
    <label for="newsletter">Subscribe to newsletter</label>
    
    <!-- Buttons -->
    <button type="submit">Submit</button>
    <button type="reset">Reset</button>
    <button type="button">Custom Button</button>
    <input type="submit" value="Submit Form">
</form>
```

### Form Attributes
```html
<!-- Input attributes -->
<input type="text" 
       name="username" 
       id="username"
       placeholder="Enter username"
       value="default value"
       required
       readonly
       disabled
       maxlength="20"
       pattern="[A-Za-z]{3,}"
       autocomplete="username">

<!-- Form validation -->
<input type="email" required>
<input type="url" required>
<input type="number" min="1" max="10" step="1">
<input type="text" pattern="[0-9]{3}-[0-9]{3}-[0-9]{4}">
```

## Semantic HTML5 Elements

### Page Structure
```html
<header>
    <nav>Navigation</nav>
</header>

<main>
    <article>
        <header>
            <h1>Article Title</h1>
            <time datetime="2023-01-01">January 1, 2023</time>
        </header>
        <section>
            <h2>Section Title</h2>
            <p>Content...</p>
        </section>
        <aside>
            <p>Related information</p>
        </aside>
        <footer>
            <p>Article footer</p>
        </footer>
    </article>
</main>

<footer>
    <p>&copy; 2023 Company Name</p>
</footer>
```

### Other Semantic Elements
```html
<figure>
    <img src="image.jpg" alt="Description">
    <figcaption>Image caption</figcaption>
</figure>

<details>
    <summary>Click to expand</summary>
    <p>Hidden content that can be shown/hidden</p>
</details>

<dialog open>
    <p>This is a dialog box</p>
    <button>Close</button>
</dialog>

<progress value="50" max="100">50%</progress>
<meter value="6" min="0" max="10">6 out of 10</meter>
```

## Common Attributes

### Global Attributes
```html
<!-- Universal attributes for all elements -->
id="unique-identifier"
class="css-class-name"
style="color: red; font-size: 16px;"
title="Tooltip text"
lang="en"
dir="ltr"               <!-- Text direction: ltr, rtl -->
contenteditable="true"
draggable="true"
hidden
tabindex="1"            <!-- Tab order -->
data-custom="value"     <!-- Custom data attributes -->
```

### ARIA Attributes (Accessibility)
```html
aria-label="Descriptive label"
aria-describedby="element-id"
aria-hidden="true"
aria-expanded="false"
role="button"
```

## Special Characters (HTML Entities)

```html
&lt;        <!-- < -->
&gt;        <!-- > -->
&amp;       <!-- & -->
&quot;      <!-- " -->
&apos;      <!-- ' -->
&nbsp;      <!-- Non-breaking space -->
&copy;      <!-- © -->
&reg;       <!-- ® -->
&trade;     <!-- ™ -->
&mdash;     <!-- — -->
&ndash;     <!-- – -->
&hellip;    <!-- … -->
```

## Comments and Debugging

```html
<!-- This is a comment -->
<!-- 
Multi-line
comment
-->

<!-- Conditional comments (legacy IE) -->
<!--[if IE]>
    <p>This content is only for Internet Explorer</p>
<![endif]-->
```

## Best Practices

### Accessibility
```html
<!-- Always use alt text for images -->
<img src="image.jpg" alt="Descriptive text">

<!-- Associate labels with form inputs -->
<label for="username">Username:</label>
<input type="text" id="username" name="username">

<!-- Use semantic HTML -->
<nav>, <main>, <article>, <section>, <aside>, <header>, <footer>

<!-- Provide skip links -->
<a href="#main-content" class="skip-link">Skip to main content</a>
```

### SEO Optimization
```html
<!-- Use proper heading hierarchy -->
<h1>Main title (only one per page)</h1>
<h2>Section titles</h2>
<h3>Subsection titles</h3>

<!-- Meta description -->
<meta name="description" content="Page description (150-160 characters)">

<!-- Structured data -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Company Name"
}
</script>
```

### Performance
```html
<!-- Lazy loading -->
<img src="image.jpg" alt="Description" loading="lazy">

<!-- Preload critical resources -->
<link rel="preload" href="critical.css" as="style">
<link rel="preload" href="font.woff2" as="font" type="font/woff2" crossorigin>

<!-- Async/defer scripts -->
<script src="script.js" async></script>
<script src="script.js" defer></script>
```

## HTML5 Input Types

```html
<input type="text">         <!-- Default text input -->
<input type="email">        <!-- Email validation -->
<input type="password">     <!-- Hidden text -->
<input type="number">       <!-- Numeric input -->
<input type="tel">          <!-- Telephone number -->
<input type="url">          <!-- URL validation -->
<input type="search">       <!-- Search box -->
<input type="date">         <!-- Date picker -->
<input type="time">         <!-- Time picker -->
<input type="datetime-local"> <!-- Date and time -->
<input type="month">        <!-- Month picker -->
<input type="week">         <!-- Week picker -->
<input type="color">        <!-- Color picker -->
<input type="range">        <!-- Slider -->
<input type="file">         <!-- File upload -->
<input type="hidden">       <!-- Hidden field -->
<input type="checkbox">     <!-- Checkbox -->
<input type="radio">        <!-- Radio button -->
<input type="submit">       <!-- Submit button -->
<input type="reset">        <!-- Reset button -->
<input type="button">       <!-- Generic button -->
```

## Div & Span (Generic Containers)

```html
<!-- Block-level container -->
<div class="container">
    <p>Block content</p>
</div>

<!-- Inline container -->
<p>This is <span class="highlight">highlighted text</span> in a paragraph.</p>
```

## Document Sections & Grouping

```html
<!-- Thematic break -->
<hr>

<!-- Address information -->
<address>
    Contact: <a href="mailto:email@example.com">email@example.com</a><br>
    Phone: <a href="tel:+1234567890">123-456-7890</a>
</address>

<!-- Quotations -->
<blockquote cite="https://source.com">
    <p>Long quotation text here...</p>
</blockquote>

<q cite="https://source.com">Short inline quote</q>

<!-- Citations -->
<cite>Book Title</cite>
<abbr title="HyperText Markup Language">HTML</abbr>
<dfn>Definition term</dfn>
```

## Interactive Elements

```html
<!-- Summary/Details -->
<details>
    <summary>FAQ Question</summary>
    <p>Answer to the question...</p>
</details>

<!-- Dialog/Modal -->
<dialog id="modal">
    <form method="dialog">
        <p>Modal content</p>
        <button value="cancel">Cancel</button>
        <button value="confirm">Confirm</button>
    </form>
</dialog>

<!-- Menu -->
<menu>
    <li><button type="button">Action 1</button></li>
    <li><button type="button">Action 2</button></li>
</menu>
```

## Embedded Content

```html
<!-- Canvas for graphics -->
<canvas id="myCanvas" width="200" height="100">
    Fallback content for browsers that don't support canvas
</canvas>

<!-- SVG graphics -->
<svg width="100" height="100">
    <circle cx="50" cy="50" r="40" stroke="black" stroke-width="3" fill="red" />
</svg>

<!-- Math equations -->
<math>
    <mi>x</mi>
    <mo>=</mo>
    <mi>y</mi>
</math>

<!-- Object embed -->
<object data="document.pdf" type="application/pdf" width="500" height="300">
    <p>Alternative content if PDF cannot be displayed</p>
</object>

<!-- Generic embed -->
<embed src="content.swf" type="application/x-shockwave-flash" width="400" height="300">
```

## Ruby Annotations (for East Asian typography)

```html
<ruby>
    漢 <rt>kan</rt>
    字 <rt>ji</rt>
</ruby>
```

## Data & Time Elements

```html
<!-- Time and dates -->
<time datetime="2023-12-25">December 25, 2023</time>
<time datetime="2023-12-25T09:00">9:00 AM on Christmas</time>
<time datetime="P1D">1 day</time>

<!-- Machine-readable data -->
<data value="12345">Product Code: ABC-123</data>
```

## Common HTML Patterns

### Card Layout
```html
<article class="card">
    <header>
        <h2>Card Title</h2>
        <time datetime="2023-01-01">Jan 1, 2023</time>
    </header>
    <img src="image.jpg" alt="Card image">
    <div class="card-content">
        <p>Card description...</p>
        <a href="/read-more" class="btn">Read More</a>
    </div>
</article>
```

### Hero Section
```html
<section class="hero">
    <div class="hero-content">
        <h1>Main Headline</h1>
        <p>Subheading or description</p>
        <a href="#cta" class="btn btn-primary">Call to Action</a>
    </div>
</section>
```

### Breadcrumb Navigation
```html
<nav aria-label="Breadcrumb">
    <ol class="breadcrumb">
        <li><a href="/">Home</a></li>
        <li><a href="/category">Category</a></li>
        <li aria-current="page">Current Page</li>
    </ol>
</nav>
```

## Validation & Standards

### HTML5 Document Validation
- Use [W3C Markup Validator](https://validator.w3.org/)
- Ensure proper nesting of elements
- Close all tags (except void elements)
- Use lowercase for element and attribute names
- Quote all attribute values

### Common Mistakes to Avoid
```html
<!-- ❌ Wrong -->
<p><div>Block inside inline</div></p>
<img src="image.jpg">              <!-- Missing alt -->
<a href="#">Link</a>               <!-- Empty href -->

<!-- ✅ Correct -->
<div><p>Proper nesting</p></div>
<img src="image.jpg" alt="Description">
<button type="button">Button text</button>
```
