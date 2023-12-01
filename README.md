# E-Moji Web Component

💫 A web component for rendering accessible emojis.

## Overview

This web component takes an emoji text node and wraps it with accessible markup:

- ♿ Follows a11y best practices
- 🏷️ Handles `aria-label` with `label` attribute
- 🌠 Sets `aria-role` to image

[Live demo](https://seanmcp.github.io/e-moji-web-component)

## Installation

Download the [`e-moji.js`](e-moji.js) file and add it to your project, then define the custom element in your JavaScript file:

```js
import EMoji from "./path/to/e-moji.js";

customElements.define(...EMoji);
```

By default, the tag name is `e-moji`. If you would like to use a different tag name, you can import the web-component class directly and use your own:

```js
import { EMoji } from "./path/to/e-moji.js";

customElements.define("your-custom-tag-name", EMoji);
```

## Usage

Wrap the web component around an emoji and optionally add a `label` attribute:

```html
<e-moji label="smiling">😄</e-moji>
<br />
<e-moji>🤐</e-moji>
```

Which will render:

```html
<span role="img" aria-label="smiling">😄</span>
<br />
<span role="img" aria-hidden="true">🤐</span>
```

## License

MIT
