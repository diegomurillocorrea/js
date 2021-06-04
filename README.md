# JavaScript Repository.

## Coercion 🔢🆎🆗

### Coercion is the automatic or implicit conversion of values from one data type to another. Conversion is similar to coercion because they both convert values from one data type to another with one key difference. Coercion is implicit whereas conversion can be either implicit or explicit.

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
