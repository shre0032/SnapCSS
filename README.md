# SnapCSS

A lightweight CSS framework built with Sass. Clean, simple, and easy to customize.

## What is SnapCSS?

SnapCSS is a small CSS framework that provides basic styling for HTML elements and utility classes for common tasks. It's built with Sass, so you can customize colors, spacing, and other variables to match your project.

[Visit Live Site](https://shre0032.github.io/SnapCSS/)

## Installation

1. Download or clone this repository
2. Make sure you have Sass installed:
   ```bash
   npm install -g sass
   ```
3. Link the compiled CSS in your HTML:
   ```html
   <link rel="stylesheet" href="path/to/css/snapcss.css">
   ```

## Usage

### Basic HTML Elements

SnapCSS automatically styles standard HTML elements. Just write normal HTML and it will look good by default.

```html
<h1>This heading is already styled</h1>
<p>Paragraphs have proper spacing and line height.</p>
<button class="btn-primary">Buttons look clean</button>
```

### Buttons

Available button classes:
- `.btn-primary` - Blue button
- `.btn-secondary` - Purple button
- `.btn-success` - Green button
- `.btn-danger` - Red button
- `.btn-warning` - Orange button
- `.btn-info` - Cyan button

Outline versions: `.btn-outline-primary`, `.btn-outline-secondary`, etc.

Button sizes: Add `.btn-sm` or `.btn-lg` for different sizes.

```html
<button class="btn-primary">Primary Button</button>
<button class="btn-outline-danger btn-lg">Large Outline</button>
```

### Forms

Forms are styled automatically. Add validation classes for colored states:
- `.input-success` - Green border
- `.input-error` - Red border
- `.input-warning` - Orange border

```html
<div class="form-group">
    <label for="email">Email</label>
    <input type="email" id="email" placeholder="you@example.com">
    <span class="form-text">Helper text goes here.</span>
</div>
```

### Tables

Tables work out of the box. Add these classes for variations:
- `.table-striped` - Alternating row colors
- `.table-bordered` - Borders on all cells
- `.table-hover` - Highlight row on hover
- `.table-compact` - Less padding

```html
<table class="table-striped table-hover">
    <thead>
        <tr>
            <th>Name</th>
            <th>Email</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>John</td>
            <td>john@example.com</td>
        </tr>
    </tbody>
</table>
```

### Utility Classes

**Colors:**
- `.bg-primary`, `.bg-success`, `.bg-danger`, etc. - Background colors
- `.text-primary`, `.text-success`, `.text-danger`, etc. - Text colors
- `.border-primary`, `.border-danger`, etc. - Border colors

**Spacing:**
- `.m-4`, `.mt-2`, `.mb-6`, etc. - Margins (0-20)
- `.p-4`, `.px-3`, `.py-5`, etc. - Padding (0-20)
- `.mx-auto` - Center elements horizontally

**Borders:**
- `.border` - Add border
- `.rounded`, `.rounded-lg`, `.rounded-full` - Border radius
- `.border-dashed`, `.border-dotted` - Border styles

**Layout:**
- `.d-flex`, `.d-block`, `.d-none` - Display properties
- `.justify-center`, `.justify-between` - Flexbox justify
- `.align-center`, `.align-start` - Flexbox align
- `.gap-3`, `.gap-4` - Flexbox gap

**Text:**
- `.text-left`, `.text-center`, `.text-right` - Text alignment
- `.font-bold`, `.font-semibold`, `.font-light` - Font weights
- `.text-sm`, `.text-lg`, `.text-2xl` - Font sizes

**Shadows:**
- `.shadow`, `.shadow-md`, `.shadow-lg` - Box shadows

**Container:**
- `.container` - Responsive centered container with max-width
- `.container-fluid` - Full-width container with padding

```html
<div class="bg-primary text-white p-4 rounded-lg shadow-md">
    <h3 class="font-bold mb-2">Card Title</h3>
    <p class="text-sm">Card content goes here.</p>
</div>
```

## Customization

All framework variables are in `src/_variables.scss`. Change these to customize the framework:

### Colors
```scss
$primary: #3b82f6;      // Change primary color
$secondary: #8b5cf6;    // Change secondary color
$success: #10b981;      // Change success color
// ... and more
```

### Spacing
```scss
$space-4: 1rem;         // Base spacing unit
$space-6: 1.5rem;       // Larger spacing
// ... and more
```

### Typography
```scss
$font-primary: 'Segoe UI', sans-serif;  // Main font
$text-base: 1rem;                       // Base font size
$weight-bold: 700;                      // Bold weight
// ... and more
```

### Border Radius
```scss
$radius-md: 0.375rem;   // Medium radius
$radius-lg: 0.5rem;     // Large radius
// ... and more
```

After changing variables, recompile:
```bash
npm run sass:build
```

## Development

To work on the framework:

1. Watch for changes (auto-compiles on save):
   ```bash
   npm run sass:watch
   ```

2. Build for production (compressed):
   ```bash
   npm run sass:build
   ```

The compiled CSS is in the `css/` folder.

## File Structure

```
snapcss/
├── css/
│   ├── snapcss.css          # Compiled CSS
│   └── snapcss.css.map      # Source map
├── src/
│   ├── base/
│   │   ├── _reset.scss      # CSS reset
│   │   └── _typography.scss # Text styling
│   ├── components/
│   │   ├── _buttons.scss    # Button styles
│   │   ├── _forms.scss      # Form styles
│   │   └── _tables.scss     # Table styles
│   ├── utilities/
│   │   ├── _colors.scss     # Color utilities
│   │   ├── _spacing.scss    # Margin/padding utilities
│   │   └── _borders.scss    # Border utilities
│   ├── _variables.scss      # All variables
│   └── main.scss            # Main import file
├── index.html               # Demo page
└── package.json             # NPM config
└── README.md                # README file
```

## Browser Support

Works in all modern browsers. No IE support.

## License

MIT
