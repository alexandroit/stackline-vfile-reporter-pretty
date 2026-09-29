# @stackline/vfile-reporter-pretty

> vfile utility to create a pretty report for a file.

[![npm version](https://img.shields.io/npm/v/@stackline/vfile-reporter-pretty.svg?style=flat-square)](https://www.npmjs.com/package/@stackline/vfile-reporter-pretty)
[![license](https://img.shields.io/npm/l/@stackline/vfile-reporter-pretty.svg?style=flat-square)](https://github.com/alexandroit/stackline-vfile-reporter-pretty)
[![GitHub repository](https://img.shields.io/badge/GitHub-alexandroit%2Fstackline-vfile-reporter-pretty-181717?style=flat-square&logo=github)](https://github.com/alexandroit/stackline-vfile-reporter-pretty)
[![Docs](https://img.shields.io/badge/docs-alexandro.net-0f766e?style=flat-square)](https://alexandro.net/docs/vanilla/vfile-reporter-pretty/)
[![Reddit community](https://img.shields.io/badge/community-r%2FStackline-ff4500?style=flat-square&logo=reddit&logoColor=white)](https://www.reddit.com/r/Stackline/)

**[Documentation](https://alexandro.net/docs/vanilla/vfile-reporter-pretty/)** | **[npm](https://www.npmjs.com/package/@stackline/vfile-reporter-pretty)** | **[Issues](https://github.com/alexandroit/stackline-vfile-reporter-pretty/issues)** | **[Repository](https://github.com/alexandroit/stackline-vfile-reporter-pretty)**

**Current package version:** `1.0.1`

---

## Why this package?

`@stackline/vfile-reporter-pretty` is the Stackline-maintained distribution of `vfile-reporter-pretty@6.1.1`. It is an independent continuation of [vfile-reporter-pretty](https://github.com/vfile/vfile-reporter-pretty); original authors and licenses remain credited below.

## Compatibility

| Item | Value |
| :--- | :--- |
| Package | `@stackline/vfile-reporter-pretty@1.0.1` |
| API target | `vfile-reporter-pretty@6.1.1` |
| Supported Node.js | `See supported framework requirements` |
| License | `MIT` |
| Module type | `module` |
| Main entry | `index.js` |
| Types | `index.d.ts` |
| Runtime dependencies | `vfile, vfile-to-eslint, eslint-formatter-pretty` |

## Installation

```bash
npm install @stackline/vfile-reporter-pretty
```

Preserve existing imports and plugin resolution with an npm alias:

```bash
npm install vfile-reporter-pretty@npm:@stackline/vfile-reporter-pretty
```

## Usage and API reference

### vfile-reporter-pretty


[vfile][] utility to create a pretty report.


## Contents

*   [What is this?](#what-is-this)
*   [When should I use this?](#when-should-i-use-this)
*   [Install](#install)
*   [Use](#use)
*   [API](#api)
    *   [`reporterPretty(files)`](#reporterprettyfiles)
*   [Types](#types)
*   [Compatibility](#compatibility)
*   [Contribute](#contribute)
*   [License](#license)

## What is this?

This package is like [`vfile-reporter`][vfile-reporter] but a bit prettier.

## When should I use this?

You can use this when you like
[`eslint-formatter-pretty`][eslint-formatter-pretty], use `vfile-reporter`
itself otherwise.

## Install

This package is [ESM only][esm].
In Node.js (version 14.14+ and 16.0+), install with [npm][]:

```sh
npm install @stackline/vfile-reporter-pretty
```

In Deno with [`esm.sh`][esmsh]:

```js
import {reporterPretty} from 'https://esm.sh/vfile-reporter-pretty@6'
```

In browsers with [`esm.sh`][esmsh]:

```html
<script type="module">
  import {reporterPretty} from 'https://esm.sh/vfile-reporter-pretty@6?bundle'
</script>
```

## Use

```js
import {VFile} from 'vfile'
import {reporterPretty} from '@stackline/vfile-reporter-pretty'

const file = new VFile({path: '~/example.md'})

file.message('`braavo` is misspelt; did you mean `bravo`?', {line: 1, column: 8})
file.info('This is perfect', {line: 2, column: 1})

try {
  file.fail('This is horrible', {line: 3, column: 5})
} catch (error) {}

console.log(reporterPretty([file]))
```

## API

This package exports the identifier [`reporterPretty`][api-reporter-pretty].
That identifier is also the default export.

### `reporterPretty(files)`

Create a pretty report from files.

###### Parameters

*   `files` ([`Array<VFile>`][vfile])
    — files to report

###### Returns

Report (`string`).

## Types

This package is fully typed with [TypeScript][].
It exports no additional types.

## Compatibility

Projects maintained by the unified collective are compatible with all maintained
versions of Node.js.
As of now, that is Node.js 14.14+ and 16.0+.
Our projects sometimes work with older versions, but this is not guaranteed.

## Contribute

See [`contributing.md`][contributing] in [`vfile/.github`][health] for ways to
get started.
See [`support.md`][support] for ways to get help.

This project has a [code of conduct][coc].
By interacting with this repository, organization, or community you agree to
abide by its terms.

## License

[MIT][license] © [Sindre Sorhus][author]



[build-badge]: https://github.com/vfile/vfile-reporter-pretty/workflows/main/badge.svg

[build]: https://github.com/vfile/vfile-reporter-pretty/actions

[coverage-badge]: https://img.shields.io/codecov/c/github/vfile/vfile-reporter-pretty.svg

[coverage]: https://codecov.io/github/vfile/vfile-reporter-pretty

[downloads-badge]: https://img.shields.io/npm/dm/vfile-reporter-pretty.svg

[downloads]: https://www.npmjs.com/package/vfile-reporter-pretty

[sponsors-badge]: https://opencollective.com/unified/sponsors/badge.svg

[backers-badge]: https://opencollective.com/unified/backers/badge.svg

[collective]: https://opencollective.com/unified

[chat-badge]: https://img.shields.io/badge/chat-discussions-success.svg

[chat]: https://github.com/vfile/vfile/discussions

[npm]: https://docs.npmjs.com/cli/install

[esm]: https://gist.github.com/sindresorhus/a39789f98801d908bbc7ff3ecc99d99c

[esmsh]: https://esm.sh

[typescript]: https://www.typescriptlang.org

[contributing]: https://github.com/vfile/.github/blob/main/contributing.md

[support]: https://github.com/vfile/.github/blob/main/support.md

[health]: https://github.com/vfile/.github

[coc]: https://github.com/vfile/.github/blob/main/code-of-conduct.md

[license]: license

[author]: https://sindresorhus.com

[screenshot]: screenshot.png

[vfile]: https://github.com/vfile/vfile

[vfile-reporter]: https://github.com/vfile/vfile-reporter

[eslint-formatter-pretty]: https://github.com/sindresorhus/eslint-formatter-pretty

[api-reporter-pretty]: #reporterprettyfiles

## Credits and original authors

- Original project: [vfile-reporter-pretty](https://github.com/vfile/vfile-reporter-pretty).
- Sindre Sorhus.
- Titus Wormer.
- Stackline maintenance: [Alexandro Paixao Marques](https://www.linkedin.com/in/aleinfo/) and [Stackline contributors](https://github.com/alexandroit).

Original copyright, license notices and contributor acknowledgements remain part of this distribution. Stackline maintenance does not replace authorship of the original work.

## Community and Links

- [Stackline website](https://alexandro.net/)
- [GitHub projects](https://github.com/alexandroit)
- [npm packages](https://www.npmjs.com/~alex360qc)
- [Reddit community — r/Stackline](https://www.reddit.com/r/Stackline/)
- [Maintainer LinkedIn](https://www.linkedin.com/in/aleinfo/)

Use this repository's issue tracker for reproducible bugs and feature requests. Join r/Stackline for examples, usage questions and release discussions.
