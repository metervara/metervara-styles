# metervara-styles

Shared CSS tokens, themes and cursors for Metervara projects.

## Installation

Install as a git dependency:

```json
{
  "dependencies": {
    "@metervara/metervara-styles": "git+https://github.com/metervara/metervara-styles.git#v1.0.0"
  }
}
```

Then import the main stylesheet in your project:

```css
@import "@metervara/metervara-styles/css/index.css";
```

## Usage

### Theme

Activate the Metervara theme by adding `data-theme="metervara"` to your HTML element:

```html
<html data-theme="metervara">
```

Control light/dark mode with `data-theme-mode`:

```html
<!-- Default: follows system preference -->
<html data-theme="metervara">

<!-- Force light mode -->
<html data-theme="metervara" data-theme-mode="light">

<!-- Force dark mode -->
<html data-theme="metervara" data-theme-mode="dark">
```

You can also override the mode on specific elements:

```html
<section data-theme-mode="dark">
  <!-- This section uses dark mode regardless of parent -->
</section>
```

### Cursors

Activate custom Metervara cursors with `data-cursor="metervara"`:

```html
<html data-cursor="metervara">
```

Enable custom cursor behavior within a container using `data-cursor-scope`:

```html
<body data-cursor-scope>
  <!-- Custom cursors will apply to links, buttons, text inputs, etc. -->
</body>
```

