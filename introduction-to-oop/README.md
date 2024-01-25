## 1. Introduction to OOP

### Definition of OOP

Object-Oriented Programming (OOP) is a programming paradigm that organizes code into reusable, self-contained units called objects. These objects represent real-world entities, each encapsulating data and the operations that can be performed on that data. In simpler terms, OOP enables developers to model the structure and behavior of their applications using objects.

### Example:

Imagine you're building a car simulation. In OOP, you'd create a Car object with properties like make, model, and speed, along with methods like accelerate and brake.

```js
class Car {
  constructor(make, model) {
    this.make = make;
    this.model = model;
    this.speed = 0;
  }

  accelerate() {
    this.speed += 10;
    console.log(
      `${this.make} ${this.model} is accelerating. Current speed: ${this.speed} km/h`
    );
  }

  brake() {
    this.speed -= 5;
    console.log(
      `${this.make} ${this.model} is braking. Current speed: ${this.speed} km/h`
    );
  }
}

const myCar = new Car("Toyota", "Camry");
myCar.accelerate(); // Output: Toyota Camry is accelerating. Current speed: 10 km/h
myCar.brake(); // Output: Toyota Camry is braking. Current speed: 5 km/h
```
