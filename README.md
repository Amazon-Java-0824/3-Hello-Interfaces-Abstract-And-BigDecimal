# 3-Hello-Interfaces-Abstract-And-BigDecimal

![](/list.png)

## Introduction to ArrayList, Interfaces, Abstract Classes, and BigDecimal
Welcome to today's lesson! We're diving into four powerful concepts in Java: ArrayList, interfaces, abstract classes, and BigDecimal. These tools are like the Swiss Army knives of Java programming – versatile, efficient, and essential for any serious developer.

Imagine you're organizing a toolbox. ArrayList is like an expandable compartment that can hold any type of tool. Interfaces are like the blueprints for specialized tools. Abstract classes are partially built tools that you can customize. And BigDecimal? It's the precision measuring tape when you need exact measurements down to the tiniest fraction.

### Why Use These Concepts?
These concepts help you:
- Create flexible and dynamic collections of data (ArrayList)
- Design clear contracts for classes to follow (interfaces)
- Share code between related classes while allowing customization (abstract classes)
- Perform precise decimal calculations without rounding errors (BigDecimal)

### Basic Concepts

1. ArrayList: A resizable array that can grow or shrink as needed.
2. Interfaces: A contract that specifies what methods a class must implement.
3. Abstract Classes: A partial implementation of a class that can't be instantiated on its own.
4. BigDecimal: A class for performing precise decimal arithmetic.

Let's explore each in detail.

### ArrayList
ArrayList is a dynamic array implementation in Java. It allows you to store and manipulate a collection of objects.

Syntax:
```java
ArrayList<Type> listName = new ArrayList<>();
```

Example:
```java
ArrayList<String> fruits = new ArrayList<>();
fruits.add("Apple");
fruits.add("Banana");
System.out.println(fruits.get(0)); // Outputs: Apple
```

### Interfaces
An interface defines a contract of methods that implementing classes must provide.

Syntax:
```java
public interface InterfaceName {
    returnType methodName(parameters);
}
```

Example:
```java
public interface Drawable {
    void draw();
}

public class Circle implements Drawable {
    @Override
    public void draw() {
        System.out.println("Drawing a circle");
    }
}
```

### Abstract Classes
Abstract classes provide a partial implementation and can't be instantiated directly.

Syntax:
```java
public abstract class AbstractClassName {
    // Concrete methods
    public void concreteMethod() {
        // Implementation
    }
    
    // Abstract methods
    public abstract void abstractMethod();
}
```

Example:
```java
public abstract class Shape {
    public abstract double area();
    
    public void displayArea() {
        System.out.println("Area: " + area());
    }
}

public class Square extends Shape {
    private double side;
    
    public Square(double side) {
        this.side = side;
    }
    
    @Override
    public double area() {
        return side * side;
    }
}
```

### BigDecimal
BigDecimal is used for precise decimal arithmetic, especially important in financial calculations.

Syntax:
```java
BigDecimal number = new BigDecimal("number");
```

Example:
```java
BigDecimal a = new BigDecimal("0.1");
BigDecimal b = new BigDecimal("0.2");
BigDecimal sum = a.add(b);
System.out.println(sum); // Outputs: 0.3
```

### Important Notes
- ArrayList is not thread-safe. Use Vector or Collections.synchronizedList() for thread-safe operations.
- Interfaces can have default and static methods since Java 8.
- Abstract classes can have both abstract and concrete methods.
- Always use the String constructor for BigDecimal to avoid precision issues.

### Practice Exercise: Shopping Cart (15 minutes)
Let's create a simple shopping cart system that uses all four concepts we've learned.

#### Task Description:
1. Create an interface `Product` with methods `getName()` and `getPrice()`.
2. Create an abstract class `AbstractProduct` that implements `Product`.
3. Create two concrete classes `Book` and `Electronics` that extend `AbstractProduct`.
4. Use an ArrayList to store cart items and BigDecimal for prices.

#### Example Code Structure:
```java
import java.math.BigDecimal;
import java.util.ArrayList;

public class ShoppingCartSystem {
    public static void main(String[] args) {
        // TODO: Implement the shopping cart system here
        // 1. Create the Product interface
        // 2. Create the AbstractProduct class
        // 3. Create Book and Electronics classes
        // 4. Create an ArrayList to store cart items
        // 5. Add some products to the cart
        // 6. Calculate and display the total price
    }
}
```

#### Bonus Challenges (if time permits):
1. Implement a discount system using BigDecimal.
2. Add a method to remove items from the cart.

Remember to use proper exception handling when working with BigDecimal arithmetic. Good luck!

This lesson builds on your previous knowledge of classes and objects, while introducing more advanced concepts that will be crucial for building larger, more complex Java applications. In future lessons, we'll explore how these concepts are used in real-world scenarios and dive deeper into design patterns that utilize interfaces and abstract classes.