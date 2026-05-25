# astro-aside

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
![GitHub all releases](https://img.shields.io/github/downloads/rgglez/astro-aside/total)
![GitHub issues](https://img.shields.io/github/issues/rgglez/astro-aside)
![GitHub commit activity](https://img.shields.io/github/commit-activity/y/rgglez/astro-aside)
[![GitHub release](https://img.shields.io/github/release/rgglez/astro-aside.svg)](https://github.com/rgglez/astro-aside/releases/)
![GitHub stars](https://img.shields.io/github/stars/rgglez/astro-aside?style=social)
![GitHub forks](https://img.shields.io/github/forks/rgglez/astro-aside?style=social)

Astro aside/callout component with five variants: `note`, `tip`, `caution`, `warning`, and `danger`.

## Installation

```bash
npm install @rgglez/astro-aside
```

## Usage

```mdx
import Aside from "@rgglez/astro-aside";

<Aside type="note">
  This is a note.
</Aside>

<Aside type="tip" title="Pro tip">
  Custom title overrides the default label.
</Aside>
```

## Props

| Prop    | Type                                               | Default  | Description                          |
|---------|---------------------------------------------------|----------|--------------------------------------|
| `type`  | `"note" \| "tip" \| "caution" \| "warning" \| "danger"` | `"note"` | Visual variant                       |
| `title` | `string`                                          | —        | Overrides the default variant label  |

## Variants

| Type      | Color  |
|-----------|--------|
| `note`    | Blue   |
| `tip`     | Green  |
| `caution` | Amber  |
| `warning` | Amber  |
| `danger`  | Red    |

## Requirements

This component uses [Tailwind CSS](https://tailwindcss.com/) utility classes for all styling. **Tailwind CSS must be configured in your project** for the component to render correctly. Without it the aside will have no colors, background, or border.

If you are using Tailwind v4, make sure the package source is included in your content scan so the utility classes are not purged:

```js
// tailwind.config.js (v3)
module.exports = {
  content: [
    // ...
    "./node_modules/@rgglez/astro-aside/src/**/*.astro",
  ],
};
```

```css
/* global.css (v4) */
@source "../node_modules/@rgglez/astro-aside/src";
```

## Development

| Target | Description |
|--------|-------------|
| `make tags` | List git tags sorted by semver (descending) |
| `make patch` | Bump PATCH version in `package.json`, commit, tag, and push |
| `make publish` | Publish current version to npm |

Typical release flow: `make patch` → `make publish`.

## License

Copyright (C) 2026 Rodolfo González González.

Licensed under the [Apache v2.0](https://www.apache.org/licenses/LICENSE-2.0.txt) license. Read the [LICENSE](LICENSE) file.
