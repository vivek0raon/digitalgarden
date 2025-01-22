---
{"dg-publish":true,"permalink":"/typescript/introduction-to-basic-types/","created":"2025-01-23T00:41:33.139+05:30","updated":"2025-01-23T01:25:02.049+05:30"}
---

## Two types

#### primitives and reference

###### eg:

```
a = 12
b = a

b+2 // kya hoga?
// a = 12 hoga aur b = 14?

```

[] {} () => reference type 

12 // primitive
harsh
sharma
huhu
true
[] // reference
{}
"apple"


#### primitive can be copied put reference can't


## Primitive types

let  // let a = 12
const 

## Non primitive types

[[Typescript/Arrays\|Arrays]]
[[Typescript/Tuples\|Tuples]]
objects
[[Typescript/enumerations\|enumerations]]







#### Any, Unknown, Void, Null, Undefined, Never

```js
let a: number; // this will only store number
```

###### any: can store anything
let a;
a = 12;
a = "harsh";


###### unknown

let a: unknown
a = 12;
a = "harsh";

> Difference between any and unknown is that when any is used typescript doesn't check many errors 


```js
let a: unknown; 
a = 12;
a = "harsh";

if(typeof a == "string")
{
	a.toUpperCase();
}

```

###### Void

```ts
function abcd(): void {
	return  true;
}
```


###### Null

```ts
let a: null;
a = 12; // Error
// union
let a:
```


###### Undefined

When variable is not defined


###### Never

Used when it will never return

```ts
function abcd(): never {
	while(true) {}
}
abcd();
console.log("hey");
```