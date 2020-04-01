## Timing SIDE-CHANNEL-LEAK
Test Functions for execution time via diffrent inputs if there is a diffrence you know what to do as they are using string equal operations or similar tech to verfiy your input.
You can verify which input is more valid then a other. via the precission of the execution time. Maybe they use early exits like length or char compare.

## via Frontend
HR Time Safe Function
```js
function timing(resource) {
  return new Promise((res)=>{
  const image = new Image()
  image.onerror = function() {
    const end = performance.now()
    const distance = end - start
    res(distance)
  }
  const start = performance.now();
  image.src = resource
  })
}
timing('https').then(console.log) //=> 1000uq
```
