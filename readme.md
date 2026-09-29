# @stackline/unist-util-inspect

> unist utility to inspect nodes.

[![npm version](https://img.shields.io/npm/v/@stackline/unist-util-inspect.svg?style=flat-square)](https://www.npmjs.com/package/@stackline/unist-util-inspect)
[![license](https://img.shields.io/npm/l/@stackline/unist-util-inspect.svg?style=flat-square)](https://github.com/alexandroit/stackline-unist-util-inspect)
[![GitHub repository](https://img.shields.io/badge/GitHub-repository-181717?style=flat-square&logo=github)](https://github.com/alexandroit/stackline-unist-util-inspect)
[![Docs](https://img.shields.io/badge/docs-alexandro.net-0f766e?style=flat-square)](https://alexandro.net/docs/vanilla/unist-util-inspect/)
[![Reddit community](https://img.shields.io/badge/community-r%2FStackline-ff4500?style=flat-square&logo=reddit&logoColor=white)](https://www.reddit.com/r/Stackline/)

**[Documentation](https://alexandro.net/docs/vanilla/unist-util-inspect/)** | **[npm](https://www.npmjs.com/package/@stackline/unist-util-inspect)** | **[Issues](https://github.com/alexandroit/stackline-unist-util-inspect/issues)** | **[Repository](https://github.com/alexandroit/stackline-unist-util-inspect)**

**Current package version:** `1.0.2`

---

## Why this package?

`@stackline/unist-util-inspect` is the Stackline-maintained distribution of `unist-util-inspect@7.0.2`. It is an independent continuation of [unist-util-inspect](https://github.com/syntax-tree/unist-util-inspect); original authors and licenses remain credited below.

## Compatibility

| Item | Value |
| :--- | :--- |
| Package | `@stackline/unist-util-inspect@1.0.2` |
| API target | `unist-util-inspect@7.0.2` |
| Supported Node.js | `See supported framework requirements` |
| License | `MIT` |
| Module type | `module` |
| Main entry | `index.js` |
| Types | `index.d.ts` |
| Runtime dependencies | `@types/unist` |

## Installation

```bash
npm install @stackline/unist-util-inspect
```

Preserve existing imports and plugin resolution with an npm alias:

```bash
npm install unist-util-inspect@npm:@stackline/unist-util-inspect
```

## Usage and API reference

### unist-util-inspect


[unist][] utility to inspect trees.

## Contents

*   [What is this?](#what-is-this)
*   [When should I use this?](#when-should-i-use-this)
*   [Install](#install)
*   [Use](#use)
*   [API](#api)
    *   [`inspect(tree[, options])`](#inspecttree-options)
    *   [`inspectColor(tree[, options])`](#inspectcolortree-options)
    *   [`inspectNoColor(tree[, options])`](#inspectnocolortree-options)
    *   [`Options`](#options)
*   [Types](#types)
*   [Compatibility](#compatibility)
*   [Contribute](#contribute)
*   [License](#license)

## What is this?

This is a utility pretty prints the tree.

## When should I use this?

This utility pretty prints the tree in a format that is made custom for unist
trees, which is terser than the often verbose and repetitive JSON,
to more easily spot bugs and see what’s going on in the tree.

## Install

This package is [ESM only][esm].
In Node.js (version 14.14+ and 16.0+), install with [npm][]:

```sh
npm install @stackline/unist-util-inspect
```

In Deno with [`esm.sh`][esmsh]:

```js
import {inspect} from 'https://esm.sh/unist-util-inspect@7'
```

In browsers with [`esm.sh`][esmsh]:

```html
<script type="module">
  import {inspect} from 'https://esm.sh/unist-util-inspect@7?bundle'
</script>
```

## Use

```js
import {u} from 'unist-builder'
import {inspect} from '@stackline/unist-util-inspect'

const tree = u('root', [
  u('literal', '1'),
  u('parent', [
    u('void', {id: 'a'}),
    u('literal', '2'),
    u('node', {id: 'b'}, [])
  ])
])

console.log(inspect(tree))
```

Yields:

```text
root[2]
├─0 literal "1"
└─1 parent[3]
    ├─0 void
    │     id: "a"
    ├─1 literal "2"
    └─2 node[0]
          id: "b"
```

## API

This package exports the identifiers [`inspect`][api-inspect],
[`inspectColor`][api-inspectcolor], and [`inspectNoColor`][api-inspectnocolor].
There is no default export.

### `inspect(tree[, options])`

Inspect a tree, with color in Node, without color in browsers.

###### Parameters

*   `tree` ([`Node`][node])
    — tree to inspect
*   `options` ([`Options`][api-options], optional)
    — configuration

###### Returns

Pretty printed `tree` (`string`).

### `inspectColor(tree[, options])`

Inspect a tree, with color.
Otherwise same as [`inspect`][api-inspect].

### `inspectNoColor(tree[, options])`

Inspect a tree, without color.
Otherwise same as [`inspect`][api-inspect].

### `Options`

Configuration (TypeScript type).

###### Fields

*   `showPositions` (`boolean`, default: `true`)
    — whether to include positional information

## Types

This package is fully typed with [TypeScript][].
It exports the additional type [`Options`][api-options].

## Compatibility

Projects maintained by the unified collective are compatible with all maintained
versions of Node.js.
As of now, that is Node.js 14.14+ and 16.0+.
Our projects sometimes work with older versions, but this is not guaranteed.

## Contribute

See [`contributing.md`][contributing] in [`syntax-tree/.github`][health] for
ways to get started.
See [`support.md`][support] for ways to get help.

This project has a [code of conduct][coc].
By interacting with this repository, organization, or community you agree to
abide by its terms.

## License

[MIT][license] © [Titus Wormer][author]



[build-badge]: https://github.com/syntax-tree/unist-util-inspect/workflows/main/badge.svg

[build]: https://github.com/syntax-tree/unist-util-inspect/actions

[coverage-badge]: https://img.shields.io/codecov/c/github/syntax-tree/unist-util-inspect.svg

[coverage]: https://codecov.io/github/syntax-tree/unist-util-inspect

[downloads-badge]: https://img.shields.io/npm/dm/unist-util-inspect.svg

[downloads]: https://www.npmjs.com/package/unist-util-inspect

[size-badge]: https://img.shields.io/bundlephobia/minzip/unist-util-inspect.svg

[size]: https://bundlephobia.com/result?p=unist-util-inspect

[sponsors-badge]: https://opencollective.com/unified/sponsors/badge.svg

[backers-badge]: https://opencollective.com/unified/backers/badge.svg

[collective]: https://opencollective.com/unified

[chat-badge]: https://img.shields.io/badge/chat-discussions-success.svg

[chat]: https://github.com/syntax-tree/unist/discussions

[npm]: https://docs.npmjs.com/cli/install

[esm]: https://gist.github.com/sindresorhus/a39789f98801d908bbc7ff3ecc99d99c

[esmsh]: https://esm.sh

[typescript]: https://www.typescriptlang.org

[license]: license

[author]: https://wooorm.com

[health]: https://github.com/syntax-tree/.github

[contributing]: https://github.com/syntax-tree/.github/blob/main/contributing.md

[support]: https://github.com/syntax-tree/.github/blob/main/support.md

[coc]: https://github.com/syntax-tree/.github/blob/main/code-of-conduct.md

[unist]: https://github.com/syntax-tree/unist

[node]: https://github.com/syntax-tree/unist#node

[api-inspect]: #inspecttree-options

[api-inspectcolor]: #inspectcolortree-options

[api-inspectnocolor]: #inspectnocolortree-options

[api-options]: #options

## Credits and original authors

- Original project: [unist-util-inspect](https://github.com/syntax-tree/unist-util-inspect).
- Titus Wormer.
- Copyright (c) 2014-2015 Titus Wormer <tituswormer@gmail.com>.
- Stackline maintenance: [Alexandro Paixao Marques](https://www.linkedin.com/in/aleinfo/) and [Stackline contributors](https://github.com/alexandroit).

Original copyright, license notices and contributor acknowledgements remain part of this distribution. Stackline maintenance does not replace authorship of the original work.

## Community and Links

- [Stackline website](https://alexandro.net/)
- [GitHub projects](https://github.com/alexandroit)
- [npm packages](https://www.npmjs.com/~alex360qc)
- [Reddit community — r/Stackline](https://www.reddit.com/r/Stackline/)
- [Maintainer LinkedIn](https://www.linkedin.com/in/aleinfo/)

Use this repository's issue tracker for reproducible bugs and feature requests. Join r/Stackline for examples, usage questions and release discussions.
