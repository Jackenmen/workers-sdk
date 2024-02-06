---
"miniflare": minor
---

feature: add a `getCf` method to Miniflare instances

add a new `getCf` method attached to instances of `Miniflare`, this `getCf` returns
the `cf` object that the Miniflare instance provides to the actual workers and it
depends of the core option of the same name

Example:

```ts
import { Miniflare } from "miniflare";

const mf = new Miniflare({ ... });

const cf = await mf.getCf();

console.log(`country = ${cf.country} ; colo = ${cf.colo}`); // logs 'country = GB ; colo = LHR'
```