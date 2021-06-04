# JavaScript Repository.

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
