# pipe

```ts
import pipe from "https://deno.land/x/pipe/mod.ts";

const fn = pipe(
  (...nbs: number[]) => nbs.reduce((a, b) => a + b, 0),
  async (c: number) => c * (await Promise.resolve(10)),
  (d: number) => d + 1000
); // const fn: (...args: number[]) => Promise<number>

await fn(1, 2, 3, 4, 5) // 1150
```
