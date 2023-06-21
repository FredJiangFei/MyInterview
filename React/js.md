# closure
    child func access parent func variable
    three scopes
        child scope
        parent scope
        global variables
# scope
    each has its own scope, a collection of variables

# typeof
    examine a value and tell you what type it is
```javascript
    typeof xx === 'string'
    xx instanceof Object
```

# DOM
    Document Object Model
    use to manipulate and create different elements in and HTML document

# data types
    Primitive
        String
        Boolean
        Number
        Undefined
        Null
        Symbol
    Non-Primitive
        Object

# '==' VS '==='
    loose equality VS strict equality
    == type conversion

# case sensitive language
 Yes

# this
 object that execute the function
 global object

# callback 
    a func pass into another func and execute after that func finished

# Callback Hell
    callback again and again

# cookie
    information store by browser, send to server-side with request to recognise the user

# browser store
    cookie: 4KB, automatically send it on every HTTP request, Manually set
    local storage: 10MB, Never Expiration
    session storage: 5MB, Expiration On tab close

# undefined VS not defined VS null
    not defined: try to use a not exist variable, throw and error xx is not defined
    undefined: Variable declaration without assigning any value to it
    null: Variable declared and assigned to null 

# empty array
```javascript
    arr = []

    arr.length = 0

    arr.splice(0, arr.length);

    while (arr.length > 0) {
        arr.pop();
    }
```

# Event bubbling
    an event triggers at child and handle by parent 
    event.stopPropagation()

# same-origin policy
    prevents js from making requests across domain boundaries
        URI scheme, 
        hostname, 
        port number

    https://geeksforgeeks.com
        https://geeksforgeeks.com/example1 yes
        https://geeksforgeeks.com/example/example.html  yes
        http://geeksforgeeks.com/example no, protocol different
        https://practice.geeksforgeeks.com/example no, host is different
        https://geeksforgeeks.com:81/example no, port is different

# check array
```javascript
if(Object.prototype.toString.call(arrayList) === '[object Array]') {
  console.log('Array!');
}
```

# check number is integer
    check remainder left divide by 1
```javascript
function isInt(num) {
  return num % 1 === 0;
}

console.log(isInt(4)); // true
console.log(isInt(12.2)); // false
console.log(isInt(0.3)); // false
```

# enqueue and dequeue

# bind() VS apply() VS call()
    change this ref

    call()
        invoke the function immediately
        func.call(thisArg, arg1, arg2, ...argN)

    apply()
        invoke the function immediately
        func.apply(thisArg, [argsArray])

    bind(): 
        return func, excute later

# const VS Object.freeze
    const: can not assign a new value
    Object.freeze: can not change object properties
```javascript
    const person = {
    name: 'fred',
    address: {
        city: 'Xian'
    }
    };
    Object.freeze(person);
    person.address = { city: 'BeiJing' } // error
    person.address.city = 'BeiJing' // work
```

# use strict
    write safer js code

# ES5 VS ES6
    arrow function
    string interpolation
    const
    block scope
    default parameter values
    spread operator
    promises
    export / import


# function foo() {} and var foo = function {}
```javascript
foo() // 123
function foo(){
    console.log('123');
}

foo() // error
var foo = function(){
    console.log('123');
}

```

# coercion
    type conversion

```javascript
var a = "42";
var b = Number(a); // explicit

var c = a * 1; //implicit

```

# IIFE
 Immediately Invoked Function Expressions
```javascript
(function IIFE(){ console.log('123') })()
```

# Currying? 
    take multiple args => take one arg
```javascript
const add = (a, b) => a + b;


```

