# Bark about javascript

Tagged template literals are a misunderstood compositional feature in javascript.

Wolfpup will do a heckin' explainer.

AWRROO!

### tagged template literals

### literal arrays

Let's bark about a subtle implementation detail.

Identical tagged template literal expressions pass the same literal array to tag function on evaluation.

```js
// tag function
function uwu(literalArray, ...injections) {
  return literalArray;
}

// evaluation
function bark(message) {
  // tagged template literal expression
  return uwu`woof! ${message}`
}

let o_o = bark(":3");
let v_v = bark(">:3");

o_o === v_v; // true, each variable references the same literal array
```

This can be barked in more practical terms using the example above: `uwu` returns the same `literalArray` when `bark` returns the same tagged template literal expression.

In this case the tagged template literal expression is ruffly:
```js
uwu`woof!${}`
```

That's programatically interesting!

WOOOF!
