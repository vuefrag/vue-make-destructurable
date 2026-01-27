<p align="center">
  <img src="logo.svg" alt="vue-make-destructurable" width="180" />
</p>

<h1 align="center">vue-make-destructurable</h1>

<p align="center">A Vue 3 composition API utility that makes an object destructurable as both an object and an array simultaneously, allowing flexible consumption patterns like composables returning multiple values.</p>

<p align="center">
  <a href="https://www.npmjs.com/package/vue-make-destructurable"><img src="https://img.shields.io/npm/v/vue-make-destructurable.svg" alt="npm version" /></a>
  <a href="https://www.npmjs.com/package/vue-make-destructurable"><img src="https://img.shields.io/npm/dm/vue-make-destructurable.svg" alt="npm downloads" /></a>
  <a href="https://github.com/vuefrag/vue-make-destructurable/blob/main/LICENSE"><img src="https://img.shields.io/npm/l/vue-make-destructurable.svg" alt="license" /></a>
</p>

## Installation

```bash
npm install vue-make-destructurable
```

## Usage

```ts
import { makeDestructurable } from 'vue-make-destructurable';
```

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

> Extracted from [VueUse](https://vueuse.org/) for standalone use.

## License

MIT
