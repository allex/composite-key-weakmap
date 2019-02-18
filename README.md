# @allex/composite-key-weakmap 
 
> A map for weakly holding nested references.

## Docs

> CompositeKeyWeakMap.d.ts

```ts
export declare class CompositeKeyWeakMap<T> {
  private _weakMap;
  set(keys: any[], value: T): void;
  get(keys: any[]): T;
  has(keys: any[]): boolean;
  delete(keys: any[]): void;
}
```

## Usage

```ts
import { CompositeKeyWeakMap } from @allex/composite-key-weakmap
interface ILoaderEntry {
  name: string;
}
const map = new CompositeKeyWeakMap<ILoaderEntry>();
const obj = {}
const bar = {}
map.set([ obj, bar ], 'foo')
map.get([ obj, bar ]) // -> foo
```

## License

[MIT](http://opensource.org/licenses/MIT) Copyright (c) [Allex Wang][1]

[1]: https://iallex.com
