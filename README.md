# Look-Inside

Look-Inside is an interactive frontend learning project built with **HTML5**, **CSS3**, and **inline JavaScript**.

It allows users to click any webpage component and instantly inspect:

* The HTML tag used
* The component category
* The primary CSS selector
* Related CSS selectors
* Description of each related CSS selector
* Actual CSS code used for each selector

This project is designed to help beginners understand how HTML structure and CSS styling work together in a real webpage.

---

## Project Overview

Look-Inside works like a mini frontend inspector.

Instead of opening browser DevTools, users can click visible components on the page and see a clean popup explaining the selected element and its related CSS.

For example, clicking a table shows related selectors such as:

```text
.table-wrapper
table
thead
tbody
tr
th
td
```

Each selector includes a short explanation and the actual CSS code used in the project.

---

## Features

* Modern responsive webpage
* Header and footer
* Navbar-based page switching
* Multiple theme options

  * Light
  * Dark
  * Blue
  * Green
* Form section with:

  * Text input
  * Email input
  * Date input
  * Submit button
* Table section with:

  * Search input
  * Responsive table wrapper
  * Table headers and rows
* Floating popup inspector
* Click-based component inspection
* Related CSS selector explanations
* CSS code preview inside the popup
* Responsive design for desktop and mobile
* No external frameworks
* No separate JavaScript file

---

## Tech Stack

* HTML5
* CSS3
* Vanilla JavaScript

---

## Project Structure

```text
CodeLens-HTML/
│
├── index.html
├── style.css
└── README.md
```

---

## How It Works

Each inspectable HTML element contains custom data attributes.

Example:

```html
<button
  class="btn inspectable"
  data-tag="button"
  data-css-class="btn"
  data-category="Button Component"
  data-related-css="btn,page"
>
  Get Started
</button>
```

When the user clicks this button, JavaScript reads the custom attributes and opens a floating popup.

The popup displays:

```text
HTML Tag: <button>
Category: Button Component
Primary CSS Selector: .btn
Related CSS Selectors:
- .btn
- .page
```

Each related selector includes its description and the actual CSS code used.

---

## Main Concepts Used

### HTML Concepts

* Semantic HTML
* Header
* Navigation
* Main content
* Sections
* Articles
* Forms
* Inputs
* Buttons
* Tables
* Footer
* Custom data attributes

### CSS Concepts

* CSS variables
* Flexbox
* CSS Grid
* Responsive design
* Media queries
* Theme switching
* Hover effects
* Popup styling
* Table responsiveness
* Code preview styling

### JavaScript Concepts

* DOM selection
* Event listeners
* Dataset access
* Dynamic popup rendering
* Element positioning
* Keyboard event handling
* Dynamic list generation

---

## Theme System

The project uses CSS variables for theme management.

Example:

```css
:root {
  --bg: #f4f7fb;
  --surface: #ffffff;
  --text: #1f2937;
  --primary: #111827;
  --accent: #2563eb;
}
```

Themes are switched using hidden radio inputs and the CSS `:has()` selector.

Example:

```css
body:has(#theme-dark:checked) {
  --bg: #0f172a;
  --surface: #1e293b;
  --text: #f8fafc;
}
```

---

## Component Inspector

The floating inspector popup appears near the clicked component.

It shows:

* Component name
* HTML tag
* Component category
* Short HTML description
* Primary CSS selector
* Related CSS selectors
* CSS selector descriptions
* CSS code snippets

This makes the project useful for learning HTML and CSS visually.

---

## Responsive Design

The layout works across different screen sizes.

On smaller screens, the popup becomes fixed at the bottom of the screen for better mobile usability.

```css
@media (max-width: 700px) {
  .floating-inspector {
    position: fixed;
    left: 12px !important;
    right: 12px;
    bottom: 12px;
    width: auto;
  }
}
```

---

## How to Run

Clone the repository:

```bash
git clone https://github.com/your-username/codelens-html.git
```

Open the project folder:

```bash
cd codelens-html
```

Open `index.html` in your browser.

No installation is required.

---

## How to Customize

### Add a New Inspectable Component

Add the `inspectable` class and data attributes:

```html
<div
  class="card inspectable"
  data-tag="div"
  data-css-class="card"
  data-category="Card Component"
  data-related-css="card,p,btn"
>
  Card Content
</div>
```

### Add CSS Documentation

Inside the JavaScript section, update:

```js
const cssDocs = {
  card: "Styles the card with padding, border, background, and rounded corners."
};
```

### Add CSS Code Preview

Inside the JavaScript section, update:

```js
const cssCode = {
  card: `.card {
  padding: 1rem;
  border-radius: 1rem;
  background: var(--surface);
}`
};
```

### Add Selector Label

Inside the JavaScript section, update:

```js
const cssSelectorLabels = {
  card: ".card"
};
```

---

## Use Cases

This project is useful for:

* HTML and CSS beginners
* Frontend learning practice
* Portfolio projects
* Teaching HTML/CSS concepts
* Understanding component structure
* Practicing responsive UI
* Demonstrating DOM interaction with JavaScript

---

## Future Improvements

* Add active navbar highlight
* Add real table search filtering
* Add copy code button
* Add syntax highlighting
* Add localStorage theme persistence
* Add more components
* Add accessibility inspection
* Add CSS property-level explanation
* Add downloadable documentation
* Convert into a React version

---

## Author

Created by **Anirudh** as a frontend learning and portfolio project.

---

## License

This project is open-source and available under the MIT License.
