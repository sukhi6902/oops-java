
# OOPS RELATIONSHIP IN JAVASCRIPT

1) IS-A : The "is-a" relationship is typically implemented using inheritance.

```bash
// Vehicle.js
class Vehicle {
    drive() {
        console.log("Vehicle is being driven");
    }
}

// Car.js
class Car extends Vehicle {
    honk() {
        console.log("Car is honking");
    }
}

// Main.js
let myCar = new Car();
myCar.drive(); // Vehicle is being driven
myCar.honk(); // Car is honking
```

2) HAS-A :
The "has-a" relationship is typically implemented using composition.

```bash
class Ink {
  constructor(color) {
    this.color = color;
  }
}

class Pen {
  constructor(brand, ink) {
    this.brand = brand;
    this.ink = ink; // Pen has-a Ink
  }

  write(text) {
    console.log(`Writing "${text}" in ${this.ink.color} with ${this.brand} pen.`);
  }
}

const blueInk = new Ink("blue");
const gelPen = new Pen("Pilot", blueInk);
gelPen.write("Hello, world!"); // Output: Writing "Hello, world!" in blue with Pilot pen.
```

3) USES-A :
  The "uses-a" relationship typically refers to dependency injection or method parameters.

```bash
class Calculator {
    constructor() {
        this.mathLibrary = new MathLibrary();
    }

    add(a, b) {
        return this.mathLibrary.add(a, b);
    }

    subtract(a, b) {
        return this.mathLibrary.subtract(a, b);
    }
}

class MathLibrary {
    add(a, b) {
        return a + b;
    }

    subtract(a, b) {
        return a - b;
    }
}
```


