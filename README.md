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

### Favicons

Favicon files live in `assets/favicons/`. After installing the package, reference them from your HTML.

**Option 1: Copy to your public folder**

Add a postinstall or build script to copy favicons into your app’s public directory:

```json
{
  "scripts": {
    "postinstall": "cp -r node_modules/@metervara/metervara-styles/assets/favicons/* public/",
    "build": "cp -r node_modules/@metervara/metervara-styles/assets/favicons/* public/ && ..."
  }
}
```

**Option 2: Reference from node_modules (build tools)**

If your bundler serves or copies from `node_modules`, use:

```
node_modules/@metervara/metervara-styles/assets/favicons/
```

**Option 3: Vite**

Copy favicons into `public/` before build (e.g. in a `prebuild` script), or use [vite-plugin-static-copy](https://github.com/sapphi-red/vite-plugin-static-copy) to copy from `node_modules/@metervara/metervara-styles/assets/favicons` to your output.

**HTML usage**

```html
<head>
  <link rel="icon" href="/favicon.ico" sizes="any" />
  <link rel="icon" href="/favicon.svg" type="image/svg+xml" />
  <link rel="apple-touch-icon" href="/apple-touch-icon.png" />
</head>
```

Adjust the `href` paths to match where your build outputs the favicons (e.g. `/favicon.ico` if they’re in the root of your public folder).

