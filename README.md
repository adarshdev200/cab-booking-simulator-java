# 🚕 Cab Booking System

A simple **Java-based Cab Booking System** that runs completely through the **Command Line Interface (CLI)**.

The project is designed to demonstrate basic **Object-Oriented Programming (OOP)** concepts in Java while providing a small real-world cab booking simulation.

## 📌 About the Project

The Cab Booking System allows users to:

* Register passengers
* Register cab drivers
* View available drivers
* Book a cab
* Automatically select the nearest available driver
* Complete a ride
* Cancel a ride
* View ride history

The application does not require a GUI and can be executed directly from a terminal.

---

## ✨ Features

### 👤 Passenger Registration

Users can register passengers by providing:

* Rider code
* Name
* Phone number

### 🚕 Driver Registration

Drivers can be added with:

* Driver code
* Name
* Phone number
* Distance from the passenger

### 📍 Nearest Driver Selection

When a passenger books a cab, the system checks all available drivers and selects the driver who is closest to the passenger.

Example:

```text
Driver A → 3.2 km
Driver B → 1.5 km
Driver C → 4.1 km

Selected Driver → Driver B
```

### 💰 Fare Calculation

The fare is calculated using a simple formula:

```text
Fare = Base Fare + (Distance × Rate per km)
```

Current values:

```text
Base Fare = ₹50
Rate = ₹15/km
```

### ✅ Ride Management

A ride can have the following statuses:

```text
BOOKED
COMPLETED
CANCELLED
```

### 📋 Ride History

Users can view all previously created rides along with:

* Trip number
* Passenger
* Driver
* Distance
* Fare
* Status

---

## 🛠️ Technologies Used

* **Java**
* Java OOP
* `ArrayList`
* `Scanner`
* Exception Handling
* Command Line Interface (CLI)

No external libraries or GUI frameworks are required.

---

## 🧱 Project Structure

The project contains the following main classes:

```text
Main.java
│
├── Person
│
├── Rider
│
├── CabDriver
│
└── Trip
```

### `Person`

The parent class containing common information such as:

```text
Person Code
Name
Phone Number
```

### `Rider`

Extends the `Person` class and represents a passenger.

### `CabDriver`

Extends the `Person` class and contains additional information such as:

```text
Distance from passenger
Cab availability
```

### `Trip`

Represents a booked ride and stores:

```text
Trip number
Rider
Driver
Distance
Fare
Trip status
```

### `Main`

Contains the main menu and controls the overall application.

---

## 🧠 OOP Concepts Demonstrated

### 1. Encapsulation

Class variables are kept private and accessed through methods.

Example:

```java
private String personName;

public String getPersonName() {
    return personName;
}
```

### 2. Inheritance

`Rider` and `CabDriver` inherit common properties from `Person`.

```text
        Person
        /    \
       /      \
    Rider   CabDriver
```

### 3. Constructors

Constructors are used to initialize objects when they are created.

### 4. Objects and Classes

The project uses separate classes for different real-world entities such as riders, drivers and trips.

### 5. ArrayList

`ArrayList` is used to store:

```java
ArrayList<Rider>
ArrayList<CabDriver>
ArrayList<Trip>
```

### 6. Exception Handling

`try-catch` is used to handle invalid input entered through the terminal.

---

## ▶️ How to Run

### Step 1 — Install Java

Make sure Java is installed on your system.

Check using:

```bash
java -version
```

Also check:

```bash
javac -version
```

### Step 2 — Clone the Repository

```bash
git clone YOUR_REPOSITORY_URL
```

### Step 3 — Open the Project Folder

```bash
cd your-project-folder
```

### Step 4 — Compile the Program

```bash
javac Main.java
```

### Step 5 — Run the Program

```bash
java Main
```

---

## 🖥️ Example Menu

```text
==============================
       CAB BOOKING APP
==============================

1. Add Rider
2. Add Cab Driver
3. Show Drivers
4. Book Cab
5. Complete Trip
6. Cancel Trip
7. Show Trip History
8. Exit

Enter your choice:
```

---

## 📖 Example Booking

First, register a rider:

```text
Enter rider code: 101
Enter rider name: Rahul
Enter phone number: 9876543210

Rider added successfully.
```

Then add drivers:

```text
Enter driver code: 201
Enter driver name: Amit
Enter phone number: 9876543211
Enter distance from passenger: 2.5

Driver added successfully.
```

When booking:

```text
--- BOOK A CAB ---

Enter rider code: 101
Enter journey distance: 8

--- BOOKING DETAILS ---
Rider    : Rahul
Driver   : Amit
Distance : 8.0 km
Fare     : Rs. 170.0

Confirm booking? (Y/N): Y

Cab booked successfully.
Your trip number is 1001
```

---

## 🔄 Basic Working Flow

```text
Start
  ↓
Register Rider
  ↓
Register Drivers
  ↓
Book Cab
  ↓
Find Available Drivers
  ↓
Select Nearest Driver
  ↓
Calculate Fare
  ↓
Confirm Booking
  ↓
Trip Created
  ↓
Complete / Cancel Trip
  ↓
View Trip History
```

---

## ⚠️ Current Limitations

This is a basic CLI project, so it currently does not include:

* Database storage
* Online payments
* GPS/live location
* Real-time driver tracking
* User authentication
* GUI
* Multiple cities

The data is stored only while the program is running.

---

## 🚀 Future Improvements

Possible improvements include:

* Add SQLite/MySQL database
* Add login for riders and drivers
* Add different cab types
* Add different pricing for different vehicles
* Add rating system
* Add payment simulation
* Add waiting-list functionality
* Add ride search
* Store ride history permanently
* Add admin functionality

---

## 🎯 Project Objective

The main objective of this project is to create a simple real-world application while understanding and applying fundamental Java programming concepts such as:

* Classes and objects
* Inheritance
* Encapsulation
* Constructors
* Collections
* Methods
* Conditional statements
* Loops
* Exception handling

---

## 👨‍💻 Author

**Your Name**

Java | OOP | CLI Project

---

## 📄 License

This project is created for **educational and learning purposes**.
