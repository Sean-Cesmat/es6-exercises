# es6-exercises

### Modify the following code to use var, const, and let appropriately. Replace the underlines with either 'var', 'const', or 'let'

```js
const SPEED_OF_LIGHT = 299792458

var speedArray = [55, 9.8, 1000000000, 186300]

for (let i = 0; i < speedArray.length; i++) {
  if (speedArray[i] > SPEED_OF_LIGHT) {
    console.log("Faster than light")
  } else {
    console.log("Sub-light speed")
  }
}
```

### What errors will the following code blocks produce? Why?

```js
const foo = 5;
foo = 6;
```
#### My Answer
you cannot reassign foo because it's a constant
```js
var foo = 5;
if (foo > 3) {
  let bar = 2;
  foo = foo * bar;
}
console.log(foo);
console.log(bar);
```
#### My Answer
bar is undefined
```js
const farge = {
  prop1: "one",
  prop2: "two",
  prop3: "three"
}
farge = {newProp: "new"};  // Error?
farge.prop1 = "forty-two"; // Error?
farge.propX = "ex";        // Error?
delete farge.propX;        // Error?
console.log(farge);
```
#### My Answer
1. You cannot reassign farge because it's a constant
2. No Error
3. No Error
4. No Error

### Rewrite the following functions using arrow functions

```js
var adder = function(a, b) {
  return a + b;
}
```
#### My Answer
```js
var adder = (a, b) => a + b;
```

```js
function printFarge() {
  console.log('farge');
}
```
#### My Answer
```js
printFarge = () => console.log('farge');
```

```js
var cleanTheString = function(str) {
  let newStr = str.replace(/\s/g, '');
  newStr = newStr.toUpperCase();
  return newStr;
}
```
#### My Answer
```js
cleanTheString = (str) => {
  let newStr = str.replace(/\s/g, '');
  newStr = newStr.toUpperCase();
  return newStr;
}
```

### Use Object Literal shorthand to clean up the following code

```js
var color = "blue";
var length = 14;
var style = "Flamenco";

var widget = {
  color: color,
  length: length,
  style: style
}
```

#### My Answer
```js
var color = "blue";
var length = 14;
var style = "Flamenco";

var widget = {
  color,
  length,
  style
}
```

### Use String Literals to make the following code more readable

```js
var name = "Paco";
var location = "Nogales";
var food = "steak";

var bio = name + " is from " + location + " and really likes to eat " + food;
```
#### My Answer
```js
var name = "Paco";
var location = "Nogales";
var food = "steak";

var bio = `${name} is from ${location} and really likes to eat ${food}`;
```

### The blocks below represent two separate files. Write out the statements needed to use the function from the first file in the code in the second file

```js
// This is in hello.js
var hello = function(name) {
  console.log(`Hello, ${name}!`);
}
// Add your code here...
export hello
```
```js
// This is in main.js
// Add your code here...
import hello from './hello.js'
hello("Siouxsie");
```
