# JS

## Unsolved 

-  Will they both return the same thing? Why or why not?

> My Question what if we use strict mode !!

```javascript
function foo1()
{
  return {
      bar: "hello"
  };
}

function foo2()
{
  return
  {
      bar: "hello"
  };
}
console.log("foo1 returns:");
console.log(foo1());
console.log("foo2 returns:");
console.log(foo2());
/*
Output 
foo1 returns:
Object {bar: "hello"}
foo2 returns:
undefined 
*/
```

- tricky for loop 

> My question :  try using var and try passing the value in log ?

```javascript
let i;
for (i = 0; i < 3; i++) {
  const log = () => {
    console.log(i);
  }
  setTimeout(log, 100);
}
```

- process.nextTick is given preference or Promise in nodejs event loop ?
> My question : which is given more preference ?

```javascript
// console.log(1);
// process.nextTick(() => console.log(2));
// console.log(3);

process.nextTick(() => console.log(2));
Promise.resolve().then(() => console.log(1));
// output is 1, 2

// Doubt : video output is 2 1 
// https://youtu.be/M3sbOSJvhxg?si=GJOcSEDUnxmPPxVD&t=423
```

## Solved