# Boileplate for Tailwind CSS CDN

# Works with Live Preview

- [Live Preview](https://marketplace.visualstudio.com/items?itemName=ms-vscode.live-server)

- [Tailwind CSS intelliSense](https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss)

- Simple example to prototype and test new Tailwind CSS features.

## Recommended VS Code Settings

Configure VS Code Settings
Add the following settings to your `.vscode/settings.json` file in your project root:

This official extension enhances VS Code’s CSS support and resolves linting issues by properly recognizing Tailwind directives like @tailwind, @apply, @layer, and @config. Disable Warning Level in Error Lens: `"css.lint.unknownAtRules": "ignore",`

```json
{
  "css.lint.unknownAtRules": "ignore",

  "files.associations": {
    "*.html": "html"
  },
  "editor.quickSuggestions": {
    "strings": "on"
  },
  "tailwindCSS.includeLanguages": {
    "html": "html"
  }
}
```

and also add a file `tailwind.config.js` that allows VS Code to display Tailwind CSS classes in the editor.

```js
/** @type {import('tailwindcss').Config} */
export default {
  content: ["./index.html"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

This will enable HTML IntelliSense and Tailwind CSS support in your project.
