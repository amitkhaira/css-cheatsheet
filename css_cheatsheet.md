# CSS Cheat Sheet

## Selectors

### Basic Selectors
```css
element     /* Tag selector */
.class      /* Class selector */
#id         /* ID selector */
*           /* Universal selector */
```

### Combinators
```css
div p       /* Descendant (space) */
div > p     /* Direct child */
div + p     /* Adjacent sibling */
div ~ p     /* General sibling */
```

### Attribute Selectors
```css
[attr]              /* Has attribute */
[attr="value"]      /* Exact match */
[attr*="value"]     /* Contains */
[attr^="value"]     /* Starts with */
[attr$="value"]     /* Ends with */
[attr~="value"]     /* Word match */
```

### Pseudo-classes
```css
:hover, :focus, :active
:first-child, :last-child, :nth-child(n)
:not(selector)
:before, :after
```

## Box Model
- **Content** → actual content (text, image)
- **Padding** → inside spacing
- **Border** → edge of the element
- **Margin** → space outside the element
```css
/* Box sizing */
box-sizing: content-box;  /* default */
box-sizing: border-box;   /* includes padding/border */

/* Spacing */
margin: top right bottom left;
margin: 10px;             /* all sides */
padding: 10px 20px;       /* vertical horizontal */

/* Border */
border: width style color;
border: 1px solid #000;
border-radius: 5px;
```

## Layout - Flexbox

```css
/* Container */
display: flex;
flex-direction: row | column | row-reverse | column-reverse;
justify-content: flex-start | center | flex-end | space-between | space-around;
align-items: flex-start | center | flex-end | stretch | baseline;
flex-wrap: nowrap | wrap | wrap-reverse;
gap: 10px;

/* Items */
flex: grow shrink basis;  /* eg:- flex-grow: 1; flex-shrink: 1; flex-basis: auto; */
flex: 1;                  /* shorthand for flex: 1 1 0% */
align-self: auto | flex-start | flex-end | center | baseline | stretch;
order: 1;
```

## Layout - CSS Grid

```css
/* Container */
display: grid;
grid-template-columns: 1fr 2fr 1fr;
grid-template-columns: repeat(3, 1fr);
grid-template-rows: 100px auto;
grid-gap: 10px;           /* or gap */
grid-template-areas: 
  "header header header"
  "sidebar main main"
  "footer footer footer";

/* Items */
grid-column: 1 / 3;       /* start / end */
grid-row: 1 / 2;
grid-area: header;
justify-self: start | center | end | stretch;
align-self: start | center | end | stretch;
```

## Positioning

```css
position: static;         /* default */
position: relative;       /* relative to normal position */
position: absolute;       /* relative to nearest positioned parent */
position: fixed;          /* relative to viewport */
position: sticky;         /* switches between relative and fixed */

/* Positioning properties */
top: 10px;
right: 10px;
bottom: 10px;
left: 10px;
z-index: 1;
```

## Typography

```css
/* Font properties */
font-family: "Arial", sans-serif;
font-size: 16px;
font-weight: normal | bold | 100-900;
font-style: normal | italic | oblique;
line-height: 1.5;
letter-spacing: 1px;
text-align: left | center | right | justify;
text-decoration: none | underline | line-through;
text-transform: none | uppercase | lowercase | capitalize;

/* Text overflow */
overflow: hidden;
text-overflow: ellipsis;
white-space: nowrap;
```

## Colors & Backgrounds

```css
/* Colors */
color: #ff0000;           /* hex */
color: rgb(255, 0, 0);    /* rgb */
color: rgba(255, 0, 0, 0.5); /* rgba */
color: hsl(0, 100%, 50%); /* hsl */

/* Backgrounds */
background-color: #fff;
background-image: url('image.jpg');
background-repeat: no-repeat | repeat | repeat-x | repeat-y;
background-position: center | top left | 50% 50%;
background-size: cover | contain | 100px 200px;
background-attachment: scroll | fixed;

/* Shorthand */
background: color image repeat position/size;
```

## Display & Visibility

```css
display: block;           /* block-level element */
display: inline;          /* inline element */
display: inline-block;    /* inline with block properties */
display: none;            /* completely hidden */
display: flex;            /* flexbox container */
display: grid;            /* grid container */

visibility: visible | hidden;  /* hidden but takes space */
opacity: 0-1;            /* transparency */
```

## Shadows
```css
box-shadow: 2px 2px 5px rgba(0,0,0,0.2);
text-shadow: 1px 1px 2px #000;
```

## Sizing

```css
/* Width & Height */
width: 100px | 50% | auto;
height: 100px | 50vh | auto;
min-width: 200px;
max-width: 500px;
min-height: 100px;
max-height: 300px;

/* Overflow */
overflow: visible | hidden | scroll | auto;
overflow-x: hidden;
overflow-y: scroll;
```

## Transitions & Animations

```css
/* Transitions */
transition: property duration timing-function delay;
transition: all 0.3s ease-in-out;
transition-property: color, background-color;
transition-duration: 0.3s;
transition-timing-function: ease | linear | ease-in | ease-out;

/* Animations */
@keyframes slideIn {
  from { transform: translateX(-100%); }
  to { transform: translateX(0); }
}

animation: name duration timing-function delay iteration-count direction;
animation: slideIn 0.5s ease-in-out;
```

## Transforms

```css
/* 2D Transforms */
transform: translate(50px, 100px);
transform: rotate(45deg);
transform: scale(1.5);
transform: skew(30deg, 20deg);

/* 3D Transforms */
transform: translateZ(50px);
transform: rotateX(45deg) rotateY(45deg);
transform: perspective(1000px);

/* Transform origin */
transform-origin: center | top left | 50% 50%;
```

## Responsive Design

```css
/* Media queries */
@media screen and (max-width: 768px) {
  /* Mobile styles */
}

@media screen and (min-width: 769px) and (max-width: 1024px) {
  /* Tablet styles */
}

/* Common breakpoints */
/* Mobile: 320px - 768px */
/* Tablet: 768px - 1024px */
/* Desktop: 1024px+ */

/* Responsive units */
rem     /* relative to root font-size */
em      /* relative to parent font-size */
vh      /* viewport height (1vh = 1% of viewport height) */
vw      /* viewport width (1vw = 1% of viewport width) */
%       /* percentage of parent */
```

## Common Patterns

### Centering
```css
/* Horizontal centering */
margin: 0 auto;           /* block elements */
text-align: center;       /* inline elements */

/* Vertical centering */
display: flex;
align-items: center;
justify-content: center;

/* Absolute centering */
position: absolute;
top: 50%;
left: 50%;
transform: translate(-50%, -50%);
```

### Clearfix
```css
.clearfix::after {
  content: "";
  display: table;
  clear: both;
}
```

### Hide elements
```css
display: none;            /* completely removed */
visibility: hidden;       /* hidden but takes space */
opacity: 0;              /* transparent but clickable */
position: absolute;       /* remove from flow */
left: -9999px;
```
## Cursor
```css
cursor: pointer | default | move | not-allowed;
```

---

## Important Utilities
```css
object-fit: cover | contain;
pointer-events: none;
user-select: none;
white-space: nowrap | pre-wrap;
word-break: break-word;
```

## CSS Variables

```css
/* Define variables */
:root {
  --primary-color: #3498db;
  --font-size: 16px;
  --margin: 10px;
}

/* Use variables */
.element {
  color: var(--primary-color);
  font-size: var(--font-size);
  margin: var(--margin);
}

/* With fallback */
color: var(--primary-color, #000);
```

## Important CSS Properties Quick Reference

```css
/* Display & Layout */
display, position, float, clear, overflow
top, right, bottom, left, z-index
width, height, margin, padding, border

/* Typography */
font-family, font-size, font-weight, line-height
color, text-align, text-decoration, text-transform

/* Visual */
background, border, border-radius, box-shadow
opacity, visibility, cursor

/* Flexbox */
justify-content, align-items, flex-direction, flex-wrap

/* Grid */
grid-template-columns, grid-template-rows, grid-gap

/* Responsive */
@media, rem, em, vh, vw, %
```

## CSS Specificity (Low to High)
1. Universal selector (*)
2. Type selectors (div, p)
3. Class selectors (.class)
4. ID selectors (#id)
5. Inline styles (style="")
6. !important

## Browser Compatibility
- Use vendor prefixes for newer properties: `-webkit-`, `-moz-`, `-ms-`
- Check [caniuse.com](https://caniuse.com) for browser support
- Use CSS reset or normalize.css for consistent defaults
