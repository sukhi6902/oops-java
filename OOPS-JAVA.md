# OOPS RELATIONSHIP IN JAVA.

1) IS-A : The "is-a" relationship is typically implemented using inheritance.

```bash
interface Vehicle {
    void move();
}

class Car implements Vehicle {
    public void move() {
        System.out.println("Car is moving...");
    }
}

class Bike implements Vehicle {
    public void move() {
        System.out.println("Bike is moving...");
    }
}

public class IsARelationship {
    public static void main(String[] args) {
        Vehicle car = new Car();
        car.move(); // Output: Car is moving...

        Vehicle bike = new Bike();
        bike.move(); // Output: Bike is moving...
    }
}


```
2) HAS-A :
The "has-a" relationship is typically implemented using composition.

```bash
// Car.java
public class Car {
    private Engine engine;

    public Car() {
        this.engine = new Engine();
    }

    public void start() {
        engine.start();
    }
}

// Engine.java
public class Engine {
    public void start() {
        System.out.println("Engine started");
    }
}

// Main.java
public class Main {
    public static void main(String[] args) {
        Car myCar = new Car();
        myCar.start(); // Engine started
    }
}
```

3) USES-A :
  The "uses-a" relationship typically refers to dependency injection or method parameters.

```bash
// Printer.java
public class Printer {
    public void print(String content) {
        System.out.println(content);
    }
}

// Document.java
public class Document {
    private Printer printer;

    public Document(Printer printer) {
        this.printer = printer;
    }

    public void printDocument(String content) {
        printer.print(content);
    }
}

// Main.java
public class Main {
    public static void main(String[] args) {
        Printer myPrinter = new Printer();
        Document myDocument = new Document(myPrinter);
        myDocument.printDocument("Printing document");
    }
}
```