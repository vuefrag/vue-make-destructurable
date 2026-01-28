<p align="center">
  <img src="https://raw.githubusercontent.com/vuefrag/vue-make-destructurable/main/banner.svg" alt="vue-make-destructurable" width="100%" />
</p>

<h1 align="center">vue-make-destructurable</h1>

<p align="center">A Vue 3 composition API utility that makes an object destructurable as both an object and an array simultaneously, allowing flexible consumption patterns like composables returning multiple values.</p>

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
import { makeDestructurable } from 'vue-make-destructurable'

const foo = { name: 'foo' }
const bar = 1024

const obj = makeDestructurable(
  { foo, bar } as const,
  [foo, bar] as const,
)

// Access as object
console.log(obj.foo) // { name: 'foo' }
console.log(obj.bar) // 1024

// Access as array
const [a, b] = obj
console.log(a) // { name: 'foo' }
console.log(b) // 1024
```

## License

MIT

Extracted from [VueUse](https://vueuse.org/) for standalone use.
