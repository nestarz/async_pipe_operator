# pipe_operator

```ts
import pipe from "https://deno.land/x/pipe_operator/mod.ts";

const fn = pipe(
  (...nbs) => nbs.reduce((a, b) => a + b, 0),
  async (c) => c * (await Promise.resolve(10)),
  (d) => d + 1000
);

await fn(1, 2, 3, 4, 5) // 1150
```
