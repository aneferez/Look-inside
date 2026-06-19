  CodeLens HTML

CodeLens HTML is an interactive learning tool built with modern HTML5, CSS3, and minimal inline JavaScript.

It allows users to explore how web interfaces are constructed by clicking on page components and instantly viewing:

* HTML tags used
* CSS classes applied
* Detailed explanations for each HTML element
* Detailed CSS explanations covering:

  * **What**
  * **Why**
  * **When**
  * **How**

The project is designed to help beginners understand the relationship between HTML structure and CSS styling through hands-on interaction.

---

   Features

* Responsive modern user interface
* Semantic HTML5 structure
* CSS-only page navigation using radio buttons
* Multiple theme options

  * Light
  * Dark
  * Blue
  * Green
* Interactive component inspector
* Real-time HTML and CSS explanations
* Educational CSS documentation using the WHAT / WHY / WHEN / HOW methodology
* Form controls with native HTML validation
* Responsive tables
* Mobile-friendly layout
* No external frameworks or libraries

---

   Demo Features

    Navigation

* Home
* Form
* Table
* About CSS

    Components Covered

* Header
* Navbar
* Footer
* Buttons
* Forms
* Text inputs
* Email inputs
* Date controls
* Search inputs
* Tables
* Cards
* Images
* Typography elements
* Layout containers

---

   Technology Stack

* HTML5
* CSS3
* JavaScript (inline only)

    CSS Concepts Used

* CSS Variables
* CSS Grid
* Flexbox
* Media Queries
* Pseudo Classes
* `:has()` selector
* Responsive Design
* Custom Themes

    HTML Concepts Used

* Semantic HTML
* Forms
* Tables
* Accessibility Attributes
* Responsive Images

---

   Project Structure

```text
CodeLens-HTML/
│
├── index.html
├── style.css
└── README.md
```

---

   How It Works

Every inspectable element contains metadata using custom data attributes.

Example:

```html
<button
  class="btn inspectable"
  data-tag="button"
  data-css-class="btn">
  Get Started
</button>
```

When a user clicks an element, JavaScript reads these attributes and displays documentation inside the inspector panel.

Example output:

```text
TAG: <button>

WHAT:
Creates a clickable action control.

WHY:
Allows users to trigger actions.

WHEN:
Use for actions such as submit, save, or navigation.

HOW:
Works with click events or form submissions.
```

---

   Getting Started

    Clone the Repository

```bash
git clone https://github.com/your-username/codelens-html.git
```

    Open the Project

```bash
cd codelens-html
```

Open `index.html` in your browser.

No installation or build process is required.

---

   Customization

    Add New Themes

Create a new theme block inside `style.css`:

```css
body:has( theme-purple:checked) {
  --bg:  f5f3ff;
  --surface:  ffffff;
  --text:  312e81;
  --primary:  6d28d9;
  --accent:  8b5cf6;
}
```

    Add New Components

Add the `inspectable` class and metadata:

```html
<div
  class="card inspectable"
  data-tag="div"
  data-css-class="card">
</div>
```

Then update the documentation objects inside `index.html`:

* `htmlDocs`
* `cssDocs`

---

   Learning Goals

This project helps developers understand:

* HTML semantics
* CSS architecture
* Component-based design
* Responsive layouts
* Theme systems
* DOM interaction
* Documentation-driven development

---

   Future Enhancements

* Searchable component documentation
* Syntax-highlighted code previews
* Export documentation as PDF
* Theme persistence using Local Storage
* CSS property inspector
* Accessibility audit mode
* Component filtering
* Keyboard navigation support

---

   Contributing

Contributions, ideas, and improvements are welcome.

1. Fork the repository
2. Create a feature branch

```bash
git checkout -b feature/new-feature
```

3. Commit your changes

```bash
git commit -m "Add new feature"
```

4. Push to your branch

```bash
git push origin feature/new-feature
```

5. Open a Pull Request

---

   License

This project is licensed under the MIT License.

---

   Author

Built with curiosity and a passion for teaching frontend development.
