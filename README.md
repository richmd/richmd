# Richmd (Legacy package)
![NPM](https://img.shields.io/npm/l/richmd)
![npm](https://img.shields.io/npm/v/richmd)
![npm](https://img.shields.io/npm/dw/richmd)


# WARNING: `richmd` is now in maintenance mode.

With the release of the latest Richmd v3, this package has entered maintenance mode.

Migration is simple and straightforward.

## Migrating from v2 to v3

Install `@richmd/js`:

```sh
$ pnpm add @richmd/js
```

Update your imports as follows:

```diff
-import { richmd } from 'richmd'
-import 'richmd/richmd.css'
+import { richmd } from '@richmd/js'
+import "@richmd/js/dist/richmd.css";
```

## Upcoming Schedule

- From **2025/03/23**: All methods in this package will be deprecated and development will end.
- By **June 2025**: This repository will be archived and the npm package will be marked as deprecated.


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
