# CSS & HTML Revision Project

This project is a hands-on journey through modern HTML and CSS, covering layout, forms, entities, and more. Each folder demonstrates a core concept with live code and comments for revision.

---

## 1. Nested Iframes and Basic HTML Structure (`1/`)

**Files:**  
- `index.html`, `child.html`, `child2.html`, `styles.css`, `script.js`

**What you learn:**
- How to use iframes to nest web pages within each other.
- The difference between the main page, a child iframe, and a nested child iframe.
- How to use the `target` attribute in anchor tags:
  - `_parent`: Opens link in the parent frame.
  - `_top`: Opens link in the topmost frame.
  - `_blank`: Opens link in a new tab.
- Basic CSS for background and font styling.

**Key code & comments:**
```html
<!-- index.html -->
<h1>Main Page (Level 0)</h1>
<iframe src="child.html" width="400" height="200"></iframe>
```
```html
<!-- child.html -->
<h2>Child Page (Level 1, inside iframe)</h2>
<iframe src="child2.html" width="350" height="150"></iframe>
```
```html
<!-- child2.html -->
<a href="https://www.google.com" target="_parent">Go to Google (in parent)</a>
<a href="https://www.google.com" target="_top">Go to Google (in top)</a>
<a href="https://www.google.com" target="_blank">Go to Google (in new tab)</a>
```
```css
/* styles.css */
body {
    background-color: #f0f0f0;
    font-family: Arial, sans-serif;
}
```

---

## 2. Bookmarks Page, Headings, and Iframes (`2/`)

**Files:**  
- `index.html`, `bookmarkmanager.html`, `styles.css`, `script.js`

**What you learn:**
- How to use all heading tags (`h1` to `h6`) for semantic structure.
- How to use paragraphs for text content.
- How to use anchor tags with different `target` values for link behavior.
- How to embed external web pages using `iframe`.
- Basic CSS for background and text color.

**Key code & comments:**
```html
<!-- index.html -->
<h1>My Bookmarks - using h1</h1>
<h2>Main Bookmarks - using h2</h2>
...
<p>Lorem ipsum ...</p>
```
```html
<!-- bookmarkmanager.html -->
<!-- _blank is used to open the link in a new tab -->
<!-- _self is used to open the link in the same tab -->
<!-- _parent is used to open the link in the parent frame, only immediate parent frame -->
<!-- _top is used to open the link in the topmost frame, boss of all frames -->
<a href="https://www.google.com" target="_self ">Open Google</a>
...
<iframe src="https://www.example.com" width="400" height="300"></iframe>
```
```css
/* styles.css */
body {
    background-color: rgb(206, 133, 169)
}
h1 {
    color: rgb(160, 41, 122);
}
p {
    color: rgb(116, 183, 0);
}
```

---

## 3. HTML Forms (`3forms/`)

**Files:**  
- `index.html`

**What you learn:**
- How to create a complete HTML form with various input types.
- Use of `<form>`, `<input>`, `<label>`, `<textarea>`, `<select>`, and `<option>`.
- How to group form fields using `<div>`.
- How to associate labels with inputs using the `for` and `id` attributes (improves accessibility and usability).
- How to use radio buttons for gender selection.
- How to use a dropdown (`<select>`) for country selection.
- How to use a submit button to send form data.

**Key code & comments:**
```html
<form action="post">
    <!-- div puts in a new space for the input field -->
    <div>
        <label for="username">Enter your username</label>
        <input type="text" id="username" name="username" placeholder="Enter your username">
    </div>
    ...
    <div>
        <input type="radio" id="male" name="gender" value="male">
        <label for="male">Male</label>
        <input type="radio" id="female" name="gender" value="female">
        <label for="female">Female</label>
    </div>
    ...
    <div>
        <select name="country" id="country">
            <option value="india">India</option>
            <option value="usa">USA</option>
            ...
        </select>
    </div>
    ...
    <div>
        <input type="submit" value="Submit">
    </div>
</form>
```
- **Tip:** Always use labels for accessibility and better UX.

---

## 4. Inline, Block, and Inline-Block Elements (`4inlineandblocks/`)

**Files:**  
- `index.html`, `styles.css`

**What you learn:**
- The difference between inline, block, and inline-block elements.
- **Inline elements:** Do not start on a new line and only take up as much width as needed (e.g., `span`, `a`, `img`, `input`, `label`, `button`, `select`, `textarea`).
- **Block elements:** Start on a new line and take up the full width of the parent (e.g., `p`, `h1`-`h6`, `div`, `section`, `article`, `header`, `footer`).
- **Inline-block elements:** Behave like inline elements but you can set width and height (e.g., `span` with `display: inline-block`).

**Key code & comments:**
```html
<!-- inline elements are elements that do not start on a new line and only take up as much width as needed -->
<!-- block elements are elements that start on a new line and take up the full width of the parent element -->
<!-- inline-block elements are elements that are both inline and block, u can set the width and height of inline-block elements -->
<p>This is a paragraph</p>
<a href="https://www.google.com">This is a link</a>
<span>This is a span</span>
<div>This is a div</div>
```
```css
/* Example from styles.css */
p, a, span, div {
    background-color: yellow;
    border: 2px solid black;
    padding: 10px;
    margin: 10px;
    width: 100px;
    height: 100px;
    display: inline-block; /* Makes all elements behave as inline-block for demo */
}
```
- **Tip:** Use `display: inline-block` to combine the best of both inline and block elements.

---

## 5. HTML Entities, `<code>`, and `<pre>` Tags (`5entitiscodetag/`)

**Files:**  
- `index.html`

**What you learn:**
- How to use HTML entities to display special characters like `<`, `>`, and `&` in content.
- How to use the `<code>` tag for inline code.
- How to use the `<pre>` tag (with `<code>`) to preserve formatting for code blocks.

**Key code & comments:**
```html
<!-- html entities are used to display special characters in html  like <, >, &, etc. -->
<!-- html entities are also known as html character references -->
<!-- basically to display tags in content, we use entities-->
<p>This is a &lt;p&gt; tag and is &lt;r&gt; than &lt;p&gt; tag</p>

<!-- also have code tag -->
<p>To print in Python, use <code>print("Hello, world!")</code>.</p>

<!-- pre preserves the formatting of code, used with larger code blocks-->
<pre><code>
def hello():
    print("Hello, world!")
</code></pre>
``` 

---

## 6. CSS Introduction and Basic Styling (`6cssintro/`)

**Files:**  
- `index.html`

**What you learn:**
- How to use basic CSS for styling HTML elements.
- Setting background color, font family, and margins for the page.
- Styling headings, paragraphs, and buttons.
- Using pseudo-classes like `:hover` for interactive effects.

**Key code & comments:**
```css
body {
    background: #f0f4f8;
    font-family: Arial, sans-serif;
    margin: 40px;
}
h1 {
    color: #2a7ae2;
    text-align: center;
}
.styled-btn {
    background: #2a7ae2;
    color: #fff;
    border-radius: 6px;
    transition: background 0.2s;
}
.styled-btn:hover {
    background: #185a9d;
}
```
- **Tip:** Use classes for reusable styles and pseudo-classes for interactivity.

---

## 7. Inline, Internal, and External CSS (`7inlineinternalexternalcss/`)

**Files:**  
- `index.html`, `styles.css`

**What you learn:**
- The three ways to add CSS to HTML:
  1. **Inline CSS:** Directly on the element (highest priority).
  2. **Internal CSS:** In a `<style>` block in the `<head>`.
  3. **External CSS:** In a separate `.css` file (lowest priority).
- **Priority order:** External < Internal < Inline.
- How CSS specificity and source order affect which styles are applied.

**Key code & comments:**
```html
<!-- Inline CSS: -->
<h1 style="color: #e23a2a;">This is an Inline Styled Heading</h1>
<!-- Internal CSS: -->
<style>
  p { color: #2a7ae2; }
</style>
<!-- External CSS: -->
<link rel="stylesheet" href="styles.css">
```
```css
.external-btn {
    background: #2a7ae2;
    color: #fff;
}
```
- **Tip:** Use external CSS for maintainability, internal for page-specific tweaks, and inline only for quick overrides.

---

## 8. CSS Selectors (`8cssselectors/`)

**Files:**  
- `index.html`, `styles.css`

**What you learn:**
- **Basic selectors:** element, class (`.class`), and ID (`#id`).
- **Relationship selectors:** descendant (`A B`), child (`A > B`), adjacent sibling (`A + B`), general sibling (`A ~ B`).
- **Attribute selectors:** `[attr=value]`, `[attr^=val]`, `[attr*=val]`.
- **Pseudo-classes:** `:hover`, `:first-child`, `:last-child`, `:nth-child()`, etc.
- **Pseudo-elements:** `::first-line`, `::first-letter`, `::before`, `::after`.
- **Combining selectors** for advanced targeting.

**Key code & comments:**
```css
/* Element selector */
h2 { color: #2a7ae2; }
/* Class selector */
.special { background-color: #e3f0fc; }
/* ID selector */
#unique { border-left: 4px solid #2a7ae2; }
/* Descendant selector */
.parent p { margin: 10px 0; }
/* Child selector */
.parent > p { border-bottom: 2px solid #2a7ae2; }
/* Attribute selector */
input[type="text"] { border: 2px solid #2a7ae2; }
/* Pseudo-class */
button:hover { background-color: #2a7ae2; }
/* Pseudo-element */
.first-line::first-letter { font-size: 2em; }
```
- **Tip:** Mastering selectors is key to powerful, maintainable CSS.

---

## 9. CSS Box Model (`9boxmodel/`)

**Files:**  
- `index.html`

**What you learn:**
- The CSS box model: content, padding, border, and margin.
- The effect of `box-sizing: border-box;` (includes padding and border in width/height).
- The difference between margin (outside the box) and padding (inside the box).
- **Margin collapsing:** When two vertical margins meet, only the larger one is used.

**Key code & comments:**
```css
.box {
    border: 5px solid black;
    box-sizing: border-box; /* Includes padding and border in width/height */
}
.box1 {
    background-color: aqua;
    width: 200px;
    height: 100px;
    margin: 20px;
}
.box2 {
    background-color: yellow;
    padding: 20px;
    margin: 20px;
}
```
- **Tip:** Use `box-sizing: border-box;` for predictable layouts.

---

## 10. Fonts and Colors in CSS (`10fontsandcolors/`)

**Files:**  
- `index.html`, `colors.html`, `fonts.png`

**What you learn:**
- How to set font families, including web fonts and fallbacks.
- How to style text: size, weight, style, line height, alignment, transformation, and decoration.
- How to handle text overflow with `ellipsis` and `clip`.
- How to use different color formats: keywords, hex, rgb, rgba, hsl.
- How to underline, color, and thicken text decorations.

**Key code & comments:**
```css
h1 {
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}
p {
    font-family: "Manrope", sans-serif;
    font-size: 30px;
    line-height: 1.5;
}
.lorem1 {
    color: blue;
    text-overflow: ellipsis;
    overflow: hidden;
    white-space: nowrap;
}
.lorem2 {
    color: green;
    text-overflow: clip;
    overflow: hidden;
    white-space: nowrap;
}
h2 {
    text-transform: capitalize;
    text-decoration: underline;
    text-decoration-color: red;
    text-decoration-thickness: 10px;
}
```
```css
/* colors.html */
h1 {
    /* color: red; */
    /* color: #ff5733; */
    /* color: rgb(red, green, blue) */
    /* color: hsl(hue, saturation, lightness) */
    color: hsl(210, 100%, 50%); /* A shade of blue */
}
```
- **Tip:** Use web fonts for unique typography and experiment with color formats for flexibility.

---

## 11. CSS Specificity and Cascade (`11specificityandcascade/`)

**Files:**  
- `index.html`, `image.png`

**What you learn:**
- How CSS decides which rule "wins" when multiple rules target the same element.
- **Specificity hierarchy:**  
  - Inline style (`style=""`) > ID selector (`#id`) > Class/Attribute selector (`.class`, `[attr]`) > Element selector (`h1`) > Universal selector (`*`)
  - `!important` overrides all.
- **Cascade:** If specificity is equal, the last rule in the CSS wins.
- **Practical tip:** Inspect the element and comment out styles to see which color is applied as specificity changes.

**Key code & comments:**
```css
* { color: black; }                /* Universal selector: lowest specificity */
h1 { color: green; }               /* Element selector */
.special { color: blue; }          /* Class selector */
.special[data-highlight] { color: blue; } /* Class + attribute: higher specificity */
[data-highlight] { color: orange; }/* Attribute selector */
h1.special { color: teal; }        /* Element + class: higher specificity */
#unique { color: purple; }         /* ID selector: highest (except inline) */
```
```html
<h1 id="unique" class="special" data-highlight style="color: red;">
  Specificity: Inline > ID > Class/Attribute > Element
</h1>
```
- **Tip:** Use the browser inspector to experiment with specificity and cascade.

---

## 12. CSS Sizing Units (`12cssSizingUnits/`)

**Files:**  
- `index.html`, `centreddiv.html`, `styles.css`

**What you learn:**
- The most common CSS sizing units:
  - `px`: Absolute pixels.
  - `em`: Relative to the element's font-size.
  - `rem`: Relative to the root (`html`) font-size.
  - `%`: Relative to the parent element.
  - `vw`/`vh`: Relative to viewport width/height.
  - `auto`: Browser decides size.
- How to mix units for flexible layouts.
- How `em` and `rem` behave in nested contexts.

**Key code & comments:**
```html
<!-- px is absolute -->
<div class="box px-box">width: 200px; height: 50px;</div>
<!-- em is relative to element's font-size -->
<div class="box em-box">width: 15em; font-size: 20px;</div>
<!-- rem is relative to root font-size -->
<div class="box rem-box">width: 20rem; font-size: 18px;</div>
<!-- % is relative to parent -->
<div class="parent-percent"><div class="box percent-box">width: 60% (of parent)</div></div>
<!-- vw/vh are relative to viewport -->
<div class="box vw-box">width: 40vw; height: 10vh;</div>
<!-- auto lets browser decide -->
<div class="box auto-box">width: auto; height: auto;</div>
```
- **Tip:** Use `rem` for consistent sizing, `em` for scalable components, and `%`/`vw`/`vh` for responsive layouts.

---

## 13. CSS Display Property (`13cssdisplayproperty/`)

**Files:**  
- `index.html`, `styles.css`

**What you learn:**
- The difference between `block`, `inline`, and `inline-block` elements.
- How to change an element's display type.
- The difference between `visibility: hidden` (takes up space) and `display: none` (removed from layout).
- Short intros to Flexbox and Grid for layout.

**Key code & comments:**
```html
<!-- Block vs Inline -->
<div class="block-demo">Block element (div)</div>
<span class="inline-demo">Inline element (span)</span>
<!-- Inline-block allows width/height -->
<span class="inline-block-vs">Inline-block (width, padding-top)</span>
<!-- Visibility vs Display: none -->
<div class="visible-demo">Visible (default)</div>
<div class="hidden-demo">Visibility: hidden (takes up space)</div>
<div class="none-demo">Display: none (gone from layout)</div>
<!-- Flex and Grid demos -->
<div class="flex-demo"><div>Flex 1</div><div>Flex 2</div><div>Flex 3</div></div>
<div class="grid-demo"><div>Grid 1</div><div>Grid 2</div><div>Grid 3</div><div>Grid 4</div></div>
```
- **Tip:** Use `inline-block` for inline elements with width/height, and `flex`/`grid` for modern layouts.

---

## 14. Box Shadows and Outlines (`14boxShadowsOutlines/`)

**Files:**  
- `index.html`, `styles.css`

**What you learn:**
- How to use `box-shadow` for shadow effects (including colored, multiple, and inset shadows).
- How to use `outline` for drawing lines around elements (outside the border).
- How to use `outline-style`, `outline-color`, and `outline-offset` for custom outlines.

**Key code & comments:**
```html
<!-- Box Shadow Examples -->
<div class="box shadow-basic">Basic Shadow</div>
<div class="box shadow-colored">Colored Shadow</div>
<div class="box shadow-multiple">Multiple Shadows</div>
<div class="box shadow-inset">Inset Shadow</div>
<!-- Outline Examples -->
<div class="box outline-basic">Basic Outline</div>
<div class="box outline-dashed">Dashed Outline</div>
<div class="box outline-offset">Outline Offset</div>
```
- **Tip:** Use `box-shadow` for depth and `outline` for accessibility (focus indication).

---

## 15. List Styling in CSS (`15liststyling/`)

**Files:**  
- `index.html`

**What you learn:**
- How to style lists using `list-style`, `list-style-type`, and `list-style-position`.
- How to make list items horizontal with `display: inline-block`.
- How to add custom spacing and borders to list items.

**Key code & comments:**
```css
nav ul li {
    list-style: disc;              /* Default bullet point */
    list-style-position: inside;   /* Bullet inside the box */
    border: 2px solid black;
    padding: 10px;
    display: inline-block;         /* Makes list items horizontal */
    margin-right: 10px;            /* Adds space between items */
}
```
- **Tip:** Use `list-style-type: none;` for custom icons or navigation menus.

---

## 16. CSS Position Property (`16cssposition/`)

**Files:**  
- `index.html`, `abs-vs-rel.html`, `abs-vs-rel.css`, `image.png`

**What you learn:**
- The different CSS position values: `static`, `relative`, `absolute`, `fixed`, and `sticky`.
- **Relative:** Moves the element relative to its normal position, but it still takes up space.
- **Absolute:** Removes the element from the normal flow and positions it relative to the nearest positioned ancestor (or the viewport if none).
- **Fixed:** Positions the element relative to the viewport; it stays in place when scrolling.
- **Z-index:** Controls stacking order of positioned elements.
- **Practical demo:**  
  - `abs-vs-rel.html` visually compares relative and absolute positioning.

**Key code & comments:**
```css
.box1 {
  background-color: lightblue;
  position: absolute;
  top: 0px; /* 0px from the top of the viewport */
}
.box3 {
  background-color: lightgreen;
  /* position: fixed; */
  /* position: absolute; */
}
```
```html
<!-- Relative vs Absolute demo -->
<div class="rel-box child" style="position: relative; top: 20px; left: 20px;">
  Child (position: relative; top: 20px; left: 20px)
</div>
<div class="abs-box child" style="position: absolute; top: 20px; left: 20px;">
  Child (position: absolute; top: 20px; left: 20px)
</div>
```
- **Tip:** Use `relative` for nudging elements, `absolute` for overlays, and `fixed` for sticky headers/footers.

---

## 17. CSS Card Component (`17csscard/`)

**Files:**  
- `index.html`, `styles.css`, `image.png`

**What you learn:**
- How to build a modern card UI component using CSS.
- Using `flexbox` for horizontal layout of list items.
- Styling images, lists, titles, and buttons for a clean card design.
- Using `box-shadow`, `border-radius`, and spacing for visual appeal.

**Key code & comments:**
```css
.card {
  width: 25vw;
  background: #fff;
  border-radius: 16px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  padding: 16px;
}
.card-list {
  display: flex;
  flex-direction: row;
  gap: 20px;
}
.card-list li {
  list-style: none;
  border: 1px solid gray;
  border-radius: 20px;
  padding: 8px 12px;
}
.btn {
  background: #2a7ae2;
  color: #fff;
  border-radius: 6px;
  transition: background 0.2s;
}
```
- **Tip:** Cards are a reusable UI pattern for displaying grouped content.

---

## 18. CSS Media Queries (`18mediaquery/`)

**Files:**  
- `index.html`

**What you learn:**
- How to use media queries to make your site responsive.
- Applying different styles based on screen width (e.g., for mobile vs desktop).
- Using `@media only screen and (max-width: 955px)` to change layout and colors on smaller screens.
- Example: Changing background color and stacking boxes vertically on small screens.

**Key code & comments:**
```css
@media only screen and (max-width: 955px){
  body { background-color: green; }
  .boxes { flex-direction: column; }
}
.boxes { display: flex; }
.box { width: 344px; height: 344px; background-color: steelblue; }
```
- **Tip:** Use media queries for mobile-first, responsive design.

---

## 19. Float, Clear, and Clearfix in CSS (`19floatclearcss/`)

**Files:**  
- `index.html`, `styles.css`

**What you learn:**
- How to use `float: left` and `float: right` to wrap text and elements.
- The `clear` property to prevent elements from wrapping around floated elements.
- The "clearfix" technique to make parent containers expand to contain floated children.
- Visual demos of float, clear, and clearfix.

**Key code & comments:**
```css
.float-left { float: left; }
.float-right { float: right; }
.clear-both { clear: both; }
.clearfix::after {
  content: "";
  display: table;
  clear: both;
}
```
- **Tip:** Floats are mostly for text/image wrapping; use Flexbox/Grid for layout, but know floats for legacy code.

---

## 20. CSS Grid Layout (`20cssgrid/`)

**Files:**  
- `grid.html`, `index.html`, `image.png`

**What you learn:**
- How to use CSS Grid for advanced, two-dimensional layouts.
- Defining grid columns with `fr` units (fractional space).
- Using `grid-template-areas` for semantic, named layout regions.
- Assigning grid items to areas with `grid-area`.
- Using `repeat()` and `minmax()` for flexible, responsive grids.

**Key code & comments:**
```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-areas:
    "nav nav nav"
    "side article article"
    "footer footer footer";
}
.item-1 { grid-area: nav; }
.item-2 { grid-area: side; }
.item-3 { grid-area: article; }
.item-4 { grid-area: footer; }
```
- **Tip:** CSS Grid is the most powerful layout system for complex, responsive designs.

---

## 21. CSS Transforms (`21csstransforms/`)

**Files:**  
- `index.html`

**What you learn:**
- How to use the `transform` property to manipulate elements in 2D and 3D space.
- **Common transforms:**
  - `rotate(40deg)`, `rotate(0.25turn)`: Rotates the element.
  - `rotateX(40deg)`: 3D rotation around the X-axis (tilt effect).
  - `scaleY(1.6)`: Scales the element vertically.
- **Tip:** You can chain multiple transforms for complex effects.

**Key code & comments:**
```css
.box {
  transform: rotate(0.25turn); /* 90 degrees */
  transform: rotateX(40deg);   /* 3D tilt */
  /* transform: scaleY(1.6);   scale about y axis */
}
```
- **Use case:** Transforms are great for interactive UIs, cards, and 3D effects.

---

## 22. CSS Transitions (`22csstransition/`)

**Files:**  
- `index.html`

**What you learn:**
- How to animate property changes smoothly using transitions.
- **Key properties:**
  - `transition-property`: Which property to animate (e.g., `transform` or `all`).
  - `transition-duration`: How long the transition takes.
  - `transition-timing-function`: The speed curve (e.g., `ease-in-out`).
  - `transition-delay`: Wait before starting the transition.
- **How it works:**  
  Transitions only animate when a property changes after the initial render (e.g., on hover or via JS).

**Key code & comments:**
```css
.box {
  transition-property: transform;
  transition-duration: 3s;
  transition-timing-function: ease-in-out;
  transition-delay: 1s;
}
.translate {
  transform: translateX(10vw) translateY(10vh);
}
```
- **Tip:** Use transitions for smooth UI feedback, like button hovers or menu reveals.

---

## 23. CSS Animations (`23cssanimations/`)

**Files:**  
- `index.html`

**What you learn:**
- How to create complex, multi-step animations using keyframes.
- **Key properties:**
  - `animation-name`, `animation-duration`, `animation-timing-function`, `animation-delay`, `animation-iteration-count`, `animation-direction`, `animation-fill-mode`.
- **Keyframes:** Define the animation steps.
- **Example:** Move a box smoothly across the screen.

**Key code & comments:**
```css
@keyframes shubhkaAnimation {
  from { }
  to { transform: translate(1000px); }
}
.box {
  animation: shubhkaAnimation 3s ease-in-out;
}
```
- **Tip:** Use keyframes for looping, multi-step, or attention-grabbing effects.

---

## 24. Realistic CSS Bounce Animation (`24cssbounceanime/`)

**Files:**  
- `index.html`

**What you learn:**
- How to create a realistic bouncing ball effect using advanced keyframes.
- **Techniques:**
  - Multiple keyframe steps for smooth, parabolic arcs.
  - Animate both X (horizontal) and Y (vertical) for a true trajectory.
  - Add squash and stretch with `scaleY` and `scaleX` for realism.
  - Use `animation-iteration-count: infinite` for continuous bouncing.

**Key code & comments:**
```css
@keyframes bounceAnimation {
  0%   { transform: translateX(0) translateY(0) scaleY(1) scaleX(1);}
  10%  { transform: translateX(100px) translateY(-300px) scaleY(0.8) scaleX(1.2);}
  20%  { transform: translateX(200px) translateY(0) scaleY(1.2) scaleX(0.8);}
  /* ...more steps for multiple bounces... */
  100% { transform: translateX(1000px) translateY(0) scaleY(1) scaleX(1);}
}
.box {
  animation: bounceAnimation 3s linear infinite;
}
```
- **Tip:** Combine transforms and keyframes for lifelike, physics-inspired motion.

---

## 25. CSS Object-fit and Position (`25cssobjectfitandpos/`)

**Files:**  
- `index.html`

**What you learn:**
- How to control how images and other replaced elements fit inside their containers using `object-fit`.
- **Common values:**
  - `cover`: Fills the box, cropping if needed (maintains aspect ratio).
  - `contain`: Fits the image inside the box, may leave empty space (maintains aspect ratio).
  - `fill`: Stretches the image to fill the box (may distort).
  - `none`: Keeps the original size.
  - `scale-down`: Scales down to fit if too large.
- **object-position:** Controls the alignment of the image within the box.

**Key code & comments:**
```css
img {
  width: 400px;
  height: 500px;
  object-fit: cover; /* or contain, fill, none, scale-down */
  /* cover: fills box, may crop; contain: fits, may leave space; fill: stretches; none: original size; scale-down: shrink to fit */
}
```
- **Tip:** Use `object-fit: cover` for hero images and galleries, `contain` for logos and icons.

---

### The Classic: How do you center a div in CSS?

> "How do you center a div in CSS?" — Every developer, ever.

**Here are some ways (and the meme lives on):**

#### 1. Horizontally with margin auto (fixed width) 
```css
div {
  width: 300px;
  margin: 0 auto;
}
```

#### 2. Flexbox (center both horizontally and vertically)
```css
.parent {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh; /* or any height */
}
```

#### 3. Grid (center both ways)
```css
.parent {
  display: grid;
  place-items: center;
  height: 100vh;
}
```

#### 4. Absolute positioning (old school)
```css
div {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

#### 5. Text-align (for inline/inline-block)
```css
.parent {
  text-align: center;
}
div {
  display: inline-block;
}
```

> **Moral:** There are many ways to center a div in CSS. The real meme is remembering which one to use!

---



