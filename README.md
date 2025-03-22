# Richmd (Legacy package)
![NPM](https://img.shields.io/npm/l/richmd)
![npm](https://img.shields.io/npm/v/richmd)
![npm](https://img.shields.io/npm/dw/richmd)

# INFO: Future Development Roadmap for Richmd

## Introduction
Thank you for using Richmd up to this point. We've been developing it for about five years now, and we're thrilled to have received more stars than we initially expected.

That said, the frontend trends and the overall programming landscape have changed significantly with the advent of AI.
As a result, we’ve found it necessary to reconsider the future direction of Richmd’s development.

We feel there are significant challenges particularly around CSS implementation, and we now need to account for a wider range of use cases in its design.
Therefore, we would like to share with you the development plans for Richmd moving forward.

## Architecture Overhaul of `richmd`, `richmd-react`, and `richmd-vue`
We had been experimentally releasing `richmd-react` and `richmd-vue` as supporting packages for Richmd, but we have now decided to rebuild these from the ground up and officially release them as part of a major version.

Moving forward, the package names will be changed as follows:

- `richmd` -> `@richmd/core`
- `richmd-react` -> `@richmd/react`
- `richmd-vue` -> `@richmd/vue`

**From now on, HTML conversion will be moved to `@richmd/react` and `@richmd/vue`, and use of these packages will become mandatory.**

## Deprecation of `richmd()`
Until now, the `richmd()` method has been used for rendering, but moving forward, direct use of `richmd()` will be deprecated.

In the future, Richmd will only provide `parseTree()`.

## Discontinuation of richmd.css and Migration to Tailwind CSS
One major decision in this update is to discontinue the use of traditional CSS imports and migrate to Tailwind CSS.
The current CSS import method applies styles globally, leading to a critical issue of style pollution in other components.

With the rise of AI-driven development, Tailwind CSS usage has increased significantly, and just recently styled-components has effectively reached end-of-life, which we see as a sign of the shifting landscape.

Going forward, Richmd will implement styling using Tailwind CSS.

## Rebuilding Package Builds Using Vite
Until now, we had a simple setup where builds were done using the `tsc` command,
but from now on, we’ll manage `@richmd/core`, `@richmd/react`, and `@richmd/vue` in a unified way, and rebuild the build process using Vite.

## In Closing
With future developments, Richmd is set to evolve significantly.
Thank you for reading to the end.
We appreciate your continued support for Richmd.

---
# Using Richmd (Legacy package)

## What is Richmd?
Richmd is a tool for making Rich contents Markdown language.

![Richmd](./docs/images/preview.png)

## Installation

```bash
# use npm
$ npm install richmd

# use yarn
$ yarn add richmd
```

## Usage
- [Usage for React](./docs/usage-react.md)
- [Usage for Vue](./docs/usage-vue.md)
- [Usage Webpack](./docs/Setup-webpack.md)

### Retrieve Abstract Syntax Tree (AST) Data
You can retrieve Abstract Syntax Tree (AST) data using the `parseTree` method.
This is useful for customizing code generation on your own.

```js
import { parseTree } from 'richmd';

const text = `# aaaa
## aaaaa

**aaaaaa**
`

const ast = parseTree(text);
```


## Markdown Syntax
Please read [Richmd Markdown Syntax Documentation](./docs/md-syntax.md).

### Supported Syntax
- strong
- italic
- image
- link
- headings
- horizontal rule
- blockquote
- unordeed list
- ordered list
- strikethrough
- code block
- checkbox list
- table
- TeX syntax (using [KaTeX](https://katex.org/))
- Color Inline Block
- Dropdown details
- Video(HTML5 Video Tag)
- Custom HTML Tag

## License
MIT

## Thank you :pray:
- [Markdown-tree-parser](https://github.com/ysugimoto/markdown-tree-parser)
  - Richmd's Markdown parser was created using the code in markdown-tree-parser as a reference.
- [KaTeX](https://github.com/KaTeX/KaTeX)
- [highlight.js](https://github.com/highlightjs/highlight.js/)
