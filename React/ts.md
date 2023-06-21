# Modules
    a file that contains functions, variables, or classes.
    Internal Module: import
    External Module: export

# built-in types
  js
    Number
    String
    Boolean
    Null 
    Undefined
    Object
   ts
    any
    unknown
    never
    enum
    tuple

# string interpolation
    `The size is ${value}`

# loops
    for
```javascript
for (let i = 0; i< 10; i++){
    console.log('Hello World')
}
``` 
    while

    do...while
        
    for..in
    iterates all properties of object
```javascript
const object = { a: 1, b: 2, c: 3 };

for (const property in object) {
  console.log(`${property}: ${object[property]}`);
}

// Expected output:
// "a: 1"
// "b: 2"
// "c: 3"
```

    for..of
```javascript
const primes = [2, 3, 5, 7];

for (let prime of primes) {
  console.log(prime);
}

// output

2
3
5
7
```

# decorators
    attribute applied to class/method/property/parameter to change behave
    angular

# let VS var
var => function-scoped
let, const => block-scoped
TDZ =>  temporal dead zone

# any
    any kind of value
    avoid any

# tuple
    a fixed length array each element has particular type
    best practice: two values, key / value 
```javascript
let user: [number, string] = [1, 'Fred'];
```
use javascript array

# enum
```javascript
enum Size {
  Small = 1,
  Medium,
  Large,
}
```

# function
```javascript
function cal(icome: number, tax: number = 2021): number {
  let rate = 1.3;
  if (tax > 2022) return icome * rate;

  return icome * (rate + 0.1);
}
```

# conver string to number
```javascript
const str = '1';
console.log(parseInt(str));
console.log(parseFloat(str));
console.log(Number(str));
```

# contextual typing
```javascript
window.onmousedown = function (mouseEvent) {
  console.log(mouseEvent.button);
  console.log(mouseEvent.kangaroo);
  //Property 'kangaroo' does not exist on type 'MouseEvent'.
};
```

# static typing
when you create a variable you need to tell the computer what kind of data will be stored in it (Text, Numeric, something else...) and you can't change it after the fact

# use ts for backend
ts + node

# check if var is null / undefined
if(value) => not null / undefined / empty / false / 0 / NaN

# object oriented principles
    Encapsulation,
    Inheritance,
    Abstraction, and
    Polymorphism.

# Type Erasure
    TypeScript removes:
        type annotations,
        interfaces,
        type aliases,
    and other type system constructs during compilation.

# ReadonlyArray

# optional chaining
    let x = foo?.bar.baz();

# Nullish Coalescing operator
    nullish coalescing operator (??)
    null or undefined
```javascript
console.log(0 ?? 'error') // 0
console.log('' ?? 'error') // ''
console.log(null ?? 'error') // 'error'
```

# any VS never VS unknown
    unknown
        compiler forces us to do type checking to make sure the method we call is exist on target object 

        typeof xx === 'string'
        xx instanceof Object
    
    never
        see the code that are unreachable
            loop
            throw exception


# Type assertions
    * not convert type, just give more specific type
    1. xx as Type
    2.<Type> xx

# Union type
```javascript
const weight: number | string = 1
```

# Literal Type
```javascript
type Quantity = 50 | 100;
type Metric = 'cm' | 'inch';
```

# namespace 
use to group functions
```javascript
namespace SomeNameSpaceName { 
   export interface ISomeInterfaceName {      }  
   export class SomeClassName {      }  
} 

SomeNameSpaceName.SomeClassName;
```

# let
    block scope

# Ployfill
    specific function support for different browser