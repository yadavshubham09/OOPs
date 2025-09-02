
# Classes and Objects

Classes and objects form the foundation of Object-Oriented Programming (OOP).

## What is a Class?

A class is a blueprint or template. It defines the attributes (fields) and behaviors (methods) of an object.

### Defining a Class in C#

To define a class in C#, we use the `class` keyword followed by the name of the class. 

Here's a simple example:

```csharp
public class Car {
    // Attributes
    private string color;
    private string make;
    private string model;
    private int year;

    // Constructor
    public Car(string color, string make, string model, int year) {
        this.color = color;
        this.make = make;
        this.model = model;
        this.year = year;
    }

    // Method to display car details
    public void displayInfo() {
        Console.WriteLine("Car Make: " + make);
        Console.WriteLine("Car Model: " + model);
        Console.WriteLine("Car Year: " + year);
        Console.WriteLine("Car Color: " + color);
    }
}
```
- **Attributes**: The class `Car` has four attributes that describe its state: `color`, `make`, `model`, and `year`.
- **Constructor**: The constructor `Car(string color, string make, string model, int year)` initializes new objects of the class.
- **Methods**: The `displayInfo` method is responsible for showcasing the car details.

## What is an Object?

An object is an instance of a class. When we create an object, we are bringing the blueprint of the class into reality. Object consists of state and behavior defined by the class, with each object holding its own copy of the data.

### Creating Objects in C#

To create an object, we use the `new` keyword followed by the class constructor. 

Here's how we can instantiate objects from the `Car` class:

```csharp
public class Main {
    public static void main(string[] args) {
        // Creating an object of the Car class
        Car car1 = new Car("Red", "Toyota", "Corolla", 2020);
        Car car2 = new Car("Blue", "Ford", "Mustang", 2021);

        // Displaying information of each car
        car1.displayInfo();
        Console.WriteLine("-----------------");
        car2.displayInfo();
    }
}
```

1. **Instantiation**: The `new` keyword is used to create an object, which allocates memory for it.
2. **Initialization**: The constructor (`Car`) initializes the object state with given parameters.
3. **Reference**: The object is referenced through a variable (`car1`, `car2`) that points to its memory location.
