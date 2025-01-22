---
{"dg-publish":true,"permalink":"/typescript/type-inference-and-annotation/","created":"2025-01-23T01:25:45.347+05:30","updated":"2025-01-23T01:41:47.943+05:30"}
---

```js
let a = "12";// inference
let a: number; // Annotation
let a: number | boolean | string;
a = 12; // allowed
a = true; // allowed
a = "harsh" // alowed
```


##### How to use annotation 

```ts
let  a: boolean;

function abcd(a: number, b: string): void {}
```


