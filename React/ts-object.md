# class VS interface
class: blueprint of object, implement all code
interface: 
    define the shape of object
    a virtual structure, 
    type-checking purposes, 
    specific a syntax that class must use
``` javascript
interface Calendar {
  name: string;
  addEvent(): void;
  removeEvent(): void;
}

interface CloudCalendar extends Calendar {}

class GoogleCalendar implements Calendar {
  name: string;
  addEvent(): void {
    throw new Error('Method not implemented.');
  }
  removeEvent(): void {
    throw new Error('Method not implemented.');
  }
}
```

# abstract calss VS interface
    interface: no logic, no any code, just method define
    abstract calss: has logic and coed want share to subclass

```javascript
abstract class Calendar {
  constructor(public name: string) {}
  addEvent() {}
  abstract removeEvent(): void;
}

interface Calendar {
  name: string;
  addEvent(): void;
  removeEvent(): void;
}
```

# class constants
readonly myProperty

# access modifiers
    Public
    Private
    Protected

    Everything in a class is public if not specified.
    Everything in a module is private unless the export keyword is used.

# getters/setters
call method as property
```javascript
get balance(): number {
    return this._balance;
}

set balance(value: number) {
if (value === 0) throw new Error('Invalid amount');

this._balance = value;
}
```

# Type aliases
```javascript
// Type aliases
type Employee = {
  readonly id: number;
  name: string;
  nickname?: string;
  retire: (date: Date) => void;
};
```

# generics class / function
Generics are able to create a component or function to work for many types rather than one type.
```javascript
    /** A class definition with a generic parameter */
    class Queue<T> {
        private data = [];
        push = (item: T) => this.data.push(item);
        pop = (): T => this.data.shift();
    }

    const queue = new Queue<number>();
    queue.push(0);
    queue.push("1"); // ERROR : cannot push a string. Only numbers allowed
```

# generics constraints
```javascript
function echo<T extends number | string>(value: T): T {
  return value;
}
```

# generics extends
```javascript
class Store<T> {
  objects: T[] = [];

  add(obj: T): void {
    this.objects.push(obj);
  }
}

class CompressibleStore<T> extends Store<T> {
  compress() {}
}
```

# Intersection Type
```javascript
let weight: number & string;

type Draggable = {
  drag: () => void;
};

type Resizable = {
  resize: () => void;
};

type UIWidget = Draggable & Resizable;
```

# Index Signatures
```javascript
class SeatAssignment {
  [seatNumber: string]: string;
}

let seats = new SeatAssignment();
seats.A1 = 'Fred';
seats.A2 = 'Tom';
seats['A3'] = 'Sun';
```

# Static members
```javascript
export class Ride {
  private static _activeRides: number = 0;

  start() {
    Ride._activeRides++;
  }

  stop() {
    Ride._activeRides--;
  }

  static get activeRides(): number {
    return Ride._activeRides;
  }
}
```

# Inheritance
    Inheritance: extends, super()
    Override: override

```javascript
export class Person {
  constructor(public firstName: string, public lastName: string) {}

  get fullName() {
    return this.firstName + ' ' + this.lastName;
  }

  wals() {
    console.log('Walking');
  }
}

export class Student extends Person {
  constructor(public studentId: number, firstName: string, lastName: string) {
    super(firstName, lastName);
  }
}

export class Teacher extends Person {
  override get fullName() {
    return 'Professor ' + super.fullName;
  }
}

```

# call base class constructor
    super()

# Polymorphism

# Abstract class
    not ready class, can not creat instance
    Shape => Circle, Square
```javascript
abstract class Shape {
  constructor(public color: string) {}

  // abstract only exist in abstract class
  abstract render(): void;
}
class CirCle extends Shape {}
class Square extends Shape {}
```

# Anonymous Function
    no function name
```javascript
var res = function(name) { }
```

# keyof
keyof Product => 'name' | 'price'

```javascript
interface Product {
  name: string;
  price: number;
}
```

# type mapping
```javascript
interface Phone {
  name: string;
  price: number;
}

interface ReadOnlyPhone {
  readonly name: string;
  readonly price: number;
}

type ReadOnlyPhoneMap = {
  readonly [K in keyof Phone]: Phone[K];
};

type ReadOnly<T> = {
  readonly [K in keyof T]: T[K];
};

type Optional<T> = {
  [K in keyof T]?: T[K];
};

type Nullable<T> = {
  [K in keyof T]: T[K] | null;
};

// google: typescript utility types

```