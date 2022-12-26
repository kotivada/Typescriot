# Tips

## Type Inference 

TypeScript is a typed language. However, it is not mandatory to specify the type of a variable. TypeScript infers types of variables when there is no explicit information available in the form of type annotations.

Types are inferred by TypeScript compiler when:

  * Variables are initialized
  * Default values are set for parameters
  * Function return types are determined

Example :
```
let data: number; 
number = 5;
```
_For more examples, please refer to the [Documentation](https://www.typescriptlang.org/docs/handbook/type-inference.html#:~:text=The%20type%20of%20the%20x,cases%2C%20type%20inference%20is%20straightforward.)_

## Unary Operator

Unary plus(+) operation is a single operand operator (which means it worked with only a single operand preceding or succeeding to it), which is used to convert its operand to a number.
https://www.geeksforgeeks.org/javascript-unary-plus-operator/

``` const a = true; //Expected output: 1
  const b = false; //Expected output: 0
  const c = null; //Expected output: 0
  const d = "100"; //Expected output: 

  console.log(+a) //Expected output: 1
  console.log(+b) //Expected output: 1
  console.log(+c)  //Expected output: 1
  console.log(typeOf +d) //Expected output: number
```