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
## Composition 🧰⚒️

### Composition is a way to combine objects or data types into more complex ones.

```js
function composeThree ( fn3, fn2, fn1 ) {
    return function composed ( v ) {
        return fn3( fn2( fn1( v ) ) );
    }
}

function minus2 ( x ) { return x - 2; };

function triple ( x ) { return x * 3; };

function increment ( x ) { return x + 1; };

var f = composeThree( minus2, triple, increment );
var p = composeThree( increment, triple, minus2 );

f( 4 );
// 13

p( 4 )
// 7
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
