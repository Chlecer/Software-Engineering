# SOLID Principles in Java

This README provides an overview of the SOLID principles and their application in Java programming. The SOLID principles are a set of guidelines aimed at creating more maintainable, flexible, and scalable software by promoting modular design and reducing code dependencies.

## Single Responsibility Principle (SRP)

The SRP states that a class should have only one reason to change, meaning it should have a single responsibility. Consider a class that reads and writes data to a file:

```java
// Class violating SRP
public class FileHandler {
    // methods for both reading and writing
}
```

Adhering to SRP:

```java
// Classes following SRP
public class FileReader {
    // method to read data
}

public class FileWriter {
    // method to write data
}
```

## Open/Closed Principle (OCP)
The OCP states that software entities should be open for extension but closed for modification. Consider an area calculator:

```java
// Class violating OCP
public class AreaCalculator {
    // methods for different shapes
}
```

Applying OCP using inheritance and polymorphism:

```java
// Interface and classes adhering to OCP
public interface Shape {
    double calculateArea();
}

public class Rectangle implements Shape {
    // Rectangle implementation
}

public class Circle implements Shape {
    // Circle implementation
}

public class AreaCalculator {
    public double calculateArea(Shape shape) {
        return shape.calculateArea();
    }
}
```
