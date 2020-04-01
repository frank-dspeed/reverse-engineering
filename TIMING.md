## Timing SIDE-CHANNEL-LEAK
Test Functions for execution time via diffrent inputs if there is a diffrence you know what to do as they are using string equal operations or similar tech to verfiy your input.
You can verify which input is more valid then a other. via the precission of the execution time. Maybe they use early exits like length or char compare.

## Prevent Timing via Header
```Timing-Allow-Origin: https://example.com```

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

Video
```js
function timing(resource) {
  return new Promise((res)=>{
  const image = new Video()
  let start;
  image.onsuspend = function() { start = performance.now(); }
  image.onerror = function() {
    const end = performance.now()
    const distance = end - start
    res(distance)
  }
  image.src = resource
  })
}
```


fetch
```js
function timing(url) {
  const requestToBeCached = new Request('timing')
  let start, end
  return fetch(url,{
    'credentials': 'include',
    'mode': 'no-cors'
  }).then(res=>{
     start = performance.now();
     return cache.put(requestToBeCached,res.clone())
  }).then(()=>end=performance.now()).then(()=>start-end)
}
```
can also remote tell us if user is logged in masure load time of login page

detect facebook age. via custom filter posts.

- https://mths.be/bva
- https://mths.be/buy

