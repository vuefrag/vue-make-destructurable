<p align="center">
  <img src="banner.svg" alt="vue-make-destructurable" width="100%" />
</p>

<h1 align="center">vue-make-destructurable</h1>

<p align="center"></p>

<p align="center">
  <a href="https://www.npmjs.com/package/vue-make-destructurable"><img src="https://img.shields.io/npm/v/vue-make-destructurable.svg" alt="npm version" /></a>
  <a href="https://www.npmjs.com/package/vue-make-destructurable"><img src="https://img.shields.io/npm/dm/vue-make-destructurable.svg" alt="npm downloads" /></a>
</p>

## Installation

```bash
npm install vue-make-destructurable
```

## Usage

```ts
import { makeDestructurable } from '@vueuse/core'

const foo = { name: 'foo' }
const bar = 1024

const obj = makeDestructurable(
  { foo, bar } as const,
  [foo, bar] as const,
)
```

## License

MIT

Extracted from [VueUse](https://vueuse.org/) for standalone use.
