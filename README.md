# Rix
Initial development on the Rix scripting extension for JavaScript

## Overview
Rix is a minimal library that allows for generative language extensions within standard JavasScript strings.<br>
An example:

```js
let a = `A basic JavaScript string`
console.log(a) // -> "A basic JavaScript string"
```
```js
let a = rix`A [Rix | special | expanded]  JavaScript string`
console.log(a) // -> "A rix JavaScript string" OR
                     "A special JavaScript string" OR
                     "A Rix JavaScript string"
```
