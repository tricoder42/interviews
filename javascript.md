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

## What is `this`?

```javascript
const Person = function(firstName) {
    this.firstName = firstName;
}

Person.prototype.sayHello = function() {
    consolo.log(`Hello, I'm ${this.firstName}`);
}

const alice = new Person('Alice');
const helloAlice = alice.sayHello;

alice.sayHello();  // Hello, I'm Alice
helloAlice();  // Hello, I'm undefined

console.log(helloAlice === alice.sayHello);  // true
```
