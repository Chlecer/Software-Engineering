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

## Liskov Substitution Principle (LSP)
The LSP ensures derived classes can substitute their base classes without affecting correctness. Example with animals:

```java
// Animal hierarchy adhering to LSP
public class Animal {
    // method for making sound
}

public class Dog extends Animal {
    // Dog-specific sound
}

public class Cat extends Animal {
    // Cat-specific sound
}

## Interface Segregation Principle (ISP)
The ISP advises avoiding forced dependencies. Example with printer interfaces:

```java
// Printer interfaces adhering to ISP
public interface Printer {
    void print();
}

public interface Scanner {
    void scan();
}

public class LaserPrinter implements Printer {
    // LaserPrinter implementation
}

public class InkjetPrinter implements Printer, Scanner {
    // InkjetPrinter implementation
}
Dependency Inversion Principle (DIP)
The DIP promotes depending on abstractions. Example with Report and Formatter:

```java
// Formatter abstraction
public interface Formatter {
    String formatData(List<String> data);
}

// Report using Formatter through dependency injection
public class Report {
    private Formatter formatter;

    public Report(Formatter formatter) {
        this.formatter = formatter;
    }

    public void generateReport(List<String> data) {
        // Logic using injected formatter
    }
}
Applying the SOLID principles leads to maintainable code and effective programming practices.

These practical examples showcase how to apply SOLID principles in Java programming.
