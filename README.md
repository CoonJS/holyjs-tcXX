# ECMAScript proposal: @Name
- [Motivation](#motivation)
- [High-level API](#high-level-api)
- [FAQ](#faq)

## Motivation

Immutable

You can create immutable objects to be sure that the properties of the object will not be overwritten.

Exmample:

```js
const obj = {
	a: 2,
	b: [],
	c: {
		prop1: 'oldPropValue'
	}
};

const immutableObject = new Immutable(obj);

obj.a = 3; // Uncaught TypeError: Properties of the Immutable object will not be overwritten.
obj.b = [1,2,3]; // Uncaught TypeError: Properties of the Immutable object will not be overwritten.
obj.c.prop1 = 'newPropValue' // Uncaught TypeError: Properties of the Immutable object will not be overwritten.

```

## High-level API

```
Immutable([object])
```

### FAQ
#### Question

Answer
