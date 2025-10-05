# 🚗 Car (Java)

A simple Java program that simulates a **car’s behavior**, including driving, refueling, and tracking mileage.  
This program models realistic car operations like fuel consumption, range calculation, and odometer tracking.

---

## 📂 Project Structure
```
Car-main/
└── Car.Java
```

---

## 🧩 Overview
The `Car` class represents a car with attributes such as year, make, model, and miles per gallon (MPG).  
It provides methods to simulate driving, refueling, checking fuel levels, and displaying vehicle statistics.

---

## 🧠 Core Class: `Car`

### Constructor
```java
public Car(int year, String make, String model, double mpg)
```
Creates a new car object with:
- `year` — manufacturing year  
- `make` — car manufacturer (e.g., Toyota, Honda)  
- `model` — model name (e.g., Camry, Civic)  
- `mpg` — miles per gallon efficiency  

---

### Methods
| Method | Description |
|--------|--------------|
| `double getRange()` | Returns how many miles the car can travel with the current fuel. |
| `boolean lowFuel()` | Returns `true` if the remaining range is less than 20 miles. |
| `void drive(double distance)` | Simulates driving the car for a given distance, reducing fuel accordingly. |
| `void addFuel(double fuelAmount)` | Adds fuel (in gallons) to the car’s tank. |
| `String toString()` | Returns a formatted summary of the car’s status (fuel, range, and odometer). |

---

## 🧪 Example Usage
```java
public class Main {
    public static void main(String[] args) {
        Car myCar = new Car(2021, "Tesla", "Model S", 120);

        myCar.addFuel(5); // Adds 5 gallons
        System.out.println(myCar); // Displays initial stats

        myCar.drive(100); // Drive 100 miles
        System.out.println(myCar); // Updated stats

        myCar.drive(500); // Drive more than range to test low fuel warning
        System.out.println(myCar); // Displays low fuel warning
    }
}
```

### Sample Output
```
2021 Tesla Model S
Miles Traveled: 0.00
Fuel: 5.00 gallons
Range: 600.00 miles

2021 Tesla Model S
Miles Traveled: 100.00
Fuel: 4.17 gallons
Range: 500.00 miles

WARNING: LOW FUEL
```

---

## ⚙️ How to Run

1. Ensure **Java (JDK 8+)** is installed.  
2. Save both `Car.Java` and `Main.java` in the same folder.  
3. Compile and run:
   ```bash
   javac Car.Java Main.java
   java Main
   ```

---
