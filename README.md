# RiX
Initial development on the Rix scripting extension for JavaScript

## Overview
RiX is a minimal library that allows for generative language extensions within standard JavasScript strings.<br>
An example:

```js
let a = `A basic JavaScript string`
console.log(a) // -> "A basic JavaScript string"
```
```js
let a = rix`A [RiX | special | expanded]  JavaScript string`
console.log(a) // -> "A RiX JavaScript string" OR
               //    "A special JavaScript string" OR
               //    "A expanded JavaScript string"
```
Notice that the 3rd output (one option is chosen at random each time the string is printed) is not exactly grammatical. Rather than "A expanded..." it should read "_An_ expanded...". We can solve this using RiX _transforms_:

```js
let a = rix`A [RiX | special | expanded].articlize()  JavaScript string`
console.log(a) // -> "A RiX JavaScript string" OR
               //    "A special JavaScript string" OR
               //    "An expanded JavaScript string"
```
### Explanation

The script above uses a *choice* element, in brackets: `[ RiX | special | expanded]`. Each time the script is run, one of the options -- "RiX" or "special" or "expanded" -- is selected.
The script also uses the *articlize()* *transform*. Transforms are basically functions that modify the text they are attached to. In this case the text in brackets --  "RiX" or "special" or "expanded" -- gets the appropriate article (a or an) via the Rix inflector.`
