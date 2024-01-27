## JavaScript as an Object-Oriented Language

### Overview of JavaScript

JavaScript is a versatile, high-level, and dynamic programming language primarily used for building interactive and dynamic web pages. It is known for its ability to run in web browsers, making it a fundamental part of web development. While JavaScript is not strictly a class-based Object-Oriented Programming (OOP) language like Java or C++, it embraces prototype-based OOP.

#### OOP Principles in JavaScript

JavaScript incorporates the following OOP principles:

### Encapsulation:

Explanation: </br> Encapsulation in JavaScript involves bundling data (properties) and methods (functions) into objects. Objects in JavaScript act as containers for related functionality and state. </br>

Example

```js
// Object encapsulating data and methods
const car = {
  make: "Toyota",
  model: "Camry",
  speed: 0,
  accelerate: function () {
    this.speed += 10;
    console.log(
      `${this.make} ${this.model} is accelerating. Current speed: ${this.speed} km/h`
    );
  },
  brake: function () {
    this.speed -= 5;
    console.log(
      `${this.make} ${this.model} is braking. Current speed: ${this.speed} km/h`
    );
  },
};

car.accelerate(); // Output: Toyota Camry is accelerating. Current speed: 10 km/h
car.brake(); // Output: Toyota Camry is braking. Current speed: 5 km/h
```

### Inheritance:

Explanation: JavaScript supports prototypal inheritance, where objects can inherit properties and methods from other objects. This enables code reuse and the creation of object hierarchies. </br>

Example:

```js
// Parent object
const vehicle = {
  type: "Generic Vehicle",
  start: function () {
    console.log(`${this.type} is starting.`);
  },
};

// Child object inheriting from the parent
const car = Object.create(vehicle);
car.type = "Car";

car.start(); // Output: Car is starting.
```

### Polymorphism:

Explanation: </br> JavaScript supports polymorphism through function overloading and dynamic typing. Functions can adapt to different data types and behaviors. </br>

Example: </br>

```js
// Polymorphic function
function calculateArea(shape) {
  if (shape instanceof Circle) {
    return Math.PI * shape.radius ** 2;
  } else if (shape instanceof Square) {
    return shape.sideLength ** 2;
  }
}

class Circle {
  constructor(radius) {
    this.radius = radius;
  }
}

class Square {
  constructor(sideLength) {
    this.sideLength = sideLength;
  }
}

const circle = new Circle(5);
const square = new Square(4);

console.log(calculateArea(circle)); // Output: 78.54
console.log(calculateArea(square)); // Output: 16
```
