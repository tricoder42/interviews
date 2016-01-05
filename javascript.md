Javascript
==========

## Mocking of `window` object

Piece of universal javascript. `isBrowser` is `false` even tough right hand side expression is `true`.

```
const isBrowser = typeof window !== "undefined";
const window = isBrowser ? window : {};

console.log(typeof window !== "undefined");  // true
console.log(isBrowser); // false
```
