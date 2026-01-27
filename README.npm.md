<p align="center">
  <img src="logo.svg" alt="vue-make-destructurable" width="180" />
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

Make isomorphic destructurable for object and array at the same time. See [this blog](https://antfu.me/posts/destructuring-with-object-or-array/) for more details.

TypeScript Example:

```ts
import { makeDestructurable } from 'vue-make-destructurable'

const foo = { name: 'foo' }
const bar = 1024

const obj = makeDestructurable(
  { foo, bar } as const,
  [foo, bar] as const,
)
```

Usage:

```ts
let { foo, bar } = obj
let [foo, bar] = obj
```

## License

MIT

Extracted from [VueUse](https://vueuse.org/) for standalone use.
