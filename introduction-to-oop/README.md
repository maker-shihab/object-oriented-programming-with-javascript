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

## Characteristics of OOP

### Encapsulation:

- Explanation: Encapsulation is like putting your code in a protective bubble. It involves bundling data (attributes) and the methods (functions) that operate on that data into a single unit, called an object.

- Example: Think of a Person object with private attributes like name and age. Encapsulation ensures that these attributes are accessed and modified through well-defined methods, maintaining control over data integrity.

```js
class Person {
  constructor(name, age) {
    this._name = name; // Using '_' to indicate a private attribute
    this._age = age;
  }

  get name() {
    return this._name;
  }

  set name(newName) {
    this._name = newName;
  }

  get age() {
    return this._age;
  }

  set age(newAge) {
    this._age = newAge;
  }
}

const john = new Person("John", 25);
console.log(john.name); // Output: John
john.age = 26;
console.log(john.age); // Output: 26
```

### Inheritance:

- Explanation: Inheritance is a way for a new class (subclass) to inherit properties and behaviors from an existing class (superclass). It promotes code reuse and establishes a hierarchy among classes.

- Example: Extending the Person class to create a Student class, inheriting properties like name and age while adding new ones like grade.

```js
class Student extends Person {
  constructor(name, age, grade) {
    super(name, age);
    this._grade = grade;
  }

  get grade() {
    return this._grade;
  }

  set grade(newGrade) {
    this._grade = newGrade;
  }
}

const alice = new Student("Alice", 20, "A");
console.log(alice.name); // Output: Alice
console.log(alice.grade); // Output: A
```

### Polymorphism:

- Explanation: Polymorphism allows objects of different types to be treated as objects of a common type. It provides flexibility by enabling methods to be called on objects without knowing their specific types.

- Example: A Shape class with a polymorphic calculateArea method that behaves differently for various shapes like Circle and Square.

```js
class Shape {
  calculateArea() {
    // Generic area calculation
  }
}

class Circle extends Shape {
  calculateArea() {
    // Area calculation specific to a circle
  }
}

class Square extends Shape {
  calculateArea() {
    // Area calculation specific to a square
  }
}

const circle = new Circle();
const square = new Square();

console.log(circle.calculateArea()); // Output: Area calculation specific to a circle
console.log(square.calculateArea()); // Output: Area calculation specific to a square
```
