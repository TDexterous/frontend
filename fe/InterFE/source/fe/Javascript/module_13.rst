Module 13 : JAVASCRIPT - Object Oriented Programming
====================================================

- Object-oriented programming (OOP) is a programming language model organized around objects rather than "actions" and data rather than logic.

Concepts of OOP
---------------

1. Encapsulation
2. Abstraction
3. Inheritance 
4. Polymorphism

1. Encapsulation
^^^^^^^^^^^^^^^^

- Encapsulation is the concept of bundling data (properties) and methods (functions) that operate on the data into a single unit, i.e., an object.
- It helps in restricting direct access to some of an object's components, allowing for better control and maintaining the integrity of the object.

Ex:

.. code-block:: javascript
   :linenos:

    // Encapsulation example
    class BankAccount {
    constructor(accountHolder, balance) {
        this.accountHolder = accountHolder;
        this.balance = balance;
    }

    deposit(amount) {
        if (amount > 0) {
        this.balance += amount;
        console.log(`Deposited $${amount}. New balance: $${this.balance}`);
        }
    }

    withdraw(amount) {
        if (amount > 0 && amount <= this.balance) {
        this.balance -= amount;
        console.log(`Withdrawn $${amount}. New balance: $${this.balance}`);
        } else {
        console.log("Insufficient funds.");
        }
    }
    }

    const myAccount = new BankAccount("Alice", 1000);
    myAccount.deposit(500); // Output: Deposited $500. New balance: $1500
    myAccount.withdraw(200); // Output: Withdrawn $200. New balance: $1300
    myAccount.withdraw(1500); // Output: Insufficient funds.

2. Abstraction
^^^^^^^^^^^^^^

- Abstraction is the process of simplifying complex reality by modeling classes based on the essential properties and behaviors an object should have, while hiding unnecessary details.
- It focuses on what an object does rather than how it does it.

Ex:

.. code-block:: javascript
   :linenos:

    // Abstraction example
    class Shape {
    constructor(name) {
        this.name = name;
    }

    area() {
        throw new Error("Subclasses must implement the 'area' method.");
    }
    }

    class Circle extends Shape {
    constructor(radius) {
        super("Circle");
        this.radius = radius;
    }

    area() {
        return Math.PI * this.radius ** 2;
    }
    }

    const circle = new Circle(5);
    console.log(`Area of the circle: ${circle.area().toFixed(2)}`);
    // Output: Area of the circle: 78.54

3. Inheritance
^^^^^^^^^^^^^^

- Inheritance is the mechanism by which a class can inherit properties and methods from another class.
- It promotes code reuse and allows you to create new classes based on existing ones.

Ex:

.. code-block:: javascript
   :linenos:

    // Inheritance example
    class Vehicle {
    constructor(make, model) {
        this.make = make;
        this.model = model;
    }

    displayInfo() {
        console.log(`Make: ${this.make}, Model: ${this.model}`);
    }
    }

    class Car extends Vehicle {
    constructor(make, model, year) {
        super(make, model);
        this.year = year;
    }

    displayInfo() {
        super.displayInfo();
        console.log(`Year: ${this.year}`);
    }
    }

    const myCar = new Car("Toyota", "Camry", 2022);
    myCar.displayInfo();
    // Output:
    // Make: Toyota, Model: Camry
    // Year: 2022

4. Polymorphism
^^^^^^^^^^^^^^^

- Polymorphism is the ability of different objects to respond to the same method name in their own unique way.
- It allows objects of different classes to be treated as instances of a common superclass.

Ex:

.. code-block:: javascript
   :linenos:

    // Polymorphism example
    class Animal {
    constructor(name) {
        this.name = name;
    }

    makeSound() {
        throw new Error("Subclasses must implement the 'makeSound' method.");
    }
    }

    class Dog extends Animal {
    makeSound() {
        return "Woof!";
    }
    }

    class Cat extends Animal {
    makeSound() {
        return "Meow!";
    }
    }

    function performSound(animals) {
    animals.forEach(animal => {
        console.log(`${animal.name} says: ${animal.makeSound()}`);
    });
    }

    const dog = new Dog("Buddy");
    const cat = new Cat("Whiskers");

    performSound([dog, cat]);
    // Output:
    // Buddy says: Woof!
    // Whiskers says: Meow!

