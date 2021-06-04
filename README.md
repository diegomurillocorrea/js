# 🟨 JavaScript Repository 🟨

## Coercion 🔢🆎🆗

### Coercion is the automatic or implicit conversion of values from one data type to another. Conversion is similar to coercion because they both convert values from one data type to another with one key difference. Coercion is implicit whereas conversion can be either implicit or explicit.

```js
// Explicit
var number = "1";
Number ( number ) 
// 1

var age = 18;
"Hello, I am " + String ( age ) + " years old."
// "Hello, I am 18 years old."

// Implicit
var number = "1";
+number
// 1

var age = 18;
"Hello, I am " + age + " years old."
// "Hello, I am 18 years old."
```

## Callbacks 📲🔙

### A callback is a function that is passed into another function as an argument, which is then invoked inside the outer function to complete some kind of process or action.

```js
function multiplyByTwo ( arr, cb ) {
  return cb( arr );
}
  
function callback ( arr ) {
  var newArray = [];
    
  for ( let i = 0 ; i < arr.length ; i++ ) {
    newArray.push( arr[ i ] * 2 );
  }
    
  return newArray;
}
  
var array = [ 1,2,3,4,5 ];

multiplyByTwo( array, callback );
```
## Immutability🗣️🚫

### Immutability is a core principle in functional programming, and has lots to offer to object-oriented programs as well.

```js
var name = "Diego";
name = "Enrique";
// This is allowed

const country = "El Salvador";
country = "Nicaragua";
// This is not allowed
```
### How to solve Immutability

```js
var name = "Diego";
const age = 18;

function changeName ( newName ) {
    return `${ newName } Murillo`;
}

function changeAge ( newAge ) {
    return newAge + 1;
}

changeName( name );
// "Diego Murillo"

changeAge( age );
// 19
```
