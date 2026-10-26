# Strategy Pattern Calculator

## Overview

This project demonstrates the Strategy Design Pattern in Java.

The calculator performs mathematical operations using interchangeable strategies. The selected strategy can be changed at runtime without modifying the Calculator class.

## Pattern Structure

### Strategy Interface

`OperationStrategy`

```java
double execute(double a, double b);
```

### Concrete Strategies

- AddStrategy
- SubtractStrategy
- MultiplyStrategy
- DivideStrategy

### Context

`Calculator`

Stores a reference to a strategy and delegates execution to the selected strategy.

### Client

`Main`

Creates the calculator and switches strategies during program execution.

## Project Structure

```text
src
└── main
    └── java
        ├── strategy
        │   ├── OperationStrategy.java
        │   ├── AddStrategy.java
        │   ├── SubtractStrategy.java
        │   ├── MultiplyStrategy.java
        │   └── DivideStrategy.java
        │
        ├── context
        │   └── Calculator.java
        │
        └── Main.java
```

## Example Output

```text
10 + 5 = 15.0
10 - 5 = 5.0
10 * 5 = 50.0
10 / 5 = 2.0
```

## Benefits

- Eliminates conditional logic
- Supports runtime algorithm switching
- Easy to extend
- Follows Open/Closed Principle
- Improves maintainability

## How to Run

1. Open the project in IntelliJ IDEA.
2. Build the project.
3. Run `Main.java`.

## Adding a New Strategy

1. Create a class implementing `OperationStrategy`.
2. Implement the `execute()` method.
3. Set the strategy using:

```java
calculator.setStrategy(new NewStrategy());
```
