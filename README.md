# 🔎 Baseline Linter for VSCode

A **Visual Studio Code extension** that helps web developers adopt **modern web features** with confidence.
It scans your **JavaScript/TypeScript, CSS, and HTML code** for modern APIs and selectors, checks them against [Baseline](https://web.dev/baseline/) and browser compatibility data, and gives **inline feedback, reports, and a searchable dashboard** inside VSCode.

---

## ✨ Features

- **Inline Diagnostics**

  - Detect modern web features.
  - Show support warnings/errors directly in your editor.

- **Baseline Integration**

  - Checks if features are part of **Baseline**.

- **Browserslist Support**

  - Reads your project’s `.browserslist` config.
  - Warns if feature isn’t supported in your target browsers.

- **Hover Tooltips**

  - Hover on a feature → see Baseline status, browser versions, and MDN link.

- **Command: Generate Report**

  - Summarize compatibility issues in a VSCode panel.

- **Feature Search**

  - Built-in panel powered by [webstatus.dev](https://webstatus.dev).
  - Developers can search for any web feature and check support instantly.

- **Project Dashboard**
  - Analyze the whole codebase.
  - Show compatibility breakdown (safe, partial, unsafe).

### 🔮 Planned Features

- Quick Fix suggestions (polyfills or fallbacks).
- Polyfill/package recommendations.
- GitHub Action or CLI integration.
- Save results as JSON/Markdown for CI/CD or documentation.

---

## 🛠 Tech Stack

- **VSCode API** → diagnostics, hovers, commands, panels.
- **Parsers**

  - [`PostCSS`](https://postcss.org/) → CSS selectors & properties.
  - [`Babel Parser`](https://babel.dev/) → JS/TS AST traversal.
  - [`htmlparser2`](https://www.npmjs.com/package/htmlparser2) → HTML elements/attributes.

- **Data Sources**

  - [`web-features`](https://www.npmjs.com/package/web-features) → canonical feature definitions.
  - [`caniuse-lite`](https://www.npmjs.com/package/caniuse-lite) → browser support data.
  - [`browserslist`](https://github.com/browserslist/browserslist) → target browser configs.
  - [`webstatus.dev`](https://webstatus.dev) → searchable feature database (dashboard).

---

## 🚀 How It Works

1. Parse your code (CSS, JS/TS, HTML) using AST parsers.
2. Match features against `web-features` dataset.
3. Cross-check feature support with `caniuse-lite` + your `browserslist`.
4. Show inline diagnostics, hover tooltips, and summary reports.
5. Use the dashboard panel to search for feature support interactively.

---

# 📚 Documentation Powered by DeepWiki

Want to dive deeper into how the extension works, or learn more about a specific feature?

### 👉 Ask DeepWiki – our documentation is fully interactive and powered by DeepWiki.

<div align="center"><a href="https://deepwiki.com/Mangesh636/baseline-linter"><img src="./public/deep-wiki.png" alt="Ask DeepWiki"></a></div>
