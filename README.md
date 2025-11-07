
# css-tooltip-lite

Lightweight, customizable CSS-only tooltip system with theme variables and safe handling for missing tooltips.
No JavaScript required.

---

## Installation

**via npm**

```bash
npm install css-tooltip-lite
```

Import into your main CSS or JS:

```js
import 'css-tooltip-lite/dist/tooltip.css';
```

**via CDN**

```html
<link rel="stylesheet" href="https://unpkg.com/css-tooltip-lite/dist/tooltip.min.css" />
```

---

## Usage Example

```html
<div class="tooltip" data-title="Default right tooltip">Hover me</div>

<div class="tooltip top" data-title="Appears above">Hover me</div>
<div class="tooltip right" data-title="Appears right">Hover me</div>
<div class="tooltip bottom" data-title="Appears below">Hover me</div>
<div class="tooltip left" data-title="Appears left">Hover me</div>

<!-- Hidden cases -->
<div class="tooltip" data-title="">Empty title — hidden</div>
<div class="tooltip">No title — hidden</div>
```

Tooltips with empty or missing `data-title` are automatically hidden.

---

## Features

| Feature                               | Status | Notes                                 |
| ------------------------------------- | ------ | ------------------------------------- |
| Theming via CSS Variables             | Yes    | Can override globally in any CSS file |
| Fallback defaults                     | Yes    | Defined in `:root`                    |
| Handles missing or empty `data-title` | Yes    | Uses attribute filters                |
| Supports position variants            | Yes    | `.top`, `.bottom`, `.left`, `.right`  |
| Lightweight (~1KB minified)           | Yes    | No dependencies                       |
| Accessible (no flicker)               | Yes    | Uses `pointer-events: none`           |

---

## Customization

In your global stylesheet (e.g., `globals.css`):

```css
:root {
  --tooltip-bg: #1e1e1e;
  --tooltip-color: #fff;
  --tooltip-radius: 12px;
  --tooltip-shadow: 0 6px 16px rgba(0, 0, 0, 0.4);
}
```

The tooltip will automatically adapt these styles.

---

## License

MIT © [i-gourish](https://github.com/i-gourish)

