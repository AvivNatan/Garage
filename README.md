# Garage Management System

## Overview
The **Garage Management System** is a software application developed in C# to manage the operations of a garage handling different types of vehicles. The system is built with an object-oriented programming approach, utilizing inheritance, polymorphism, and collections, while incorporating advanced C# features like `enums` and working with external assemblies (`.dll`). 

This project is part of a training exercise in .NET development, focusing on multi-project environments and exception handling.

---

## Features
1. **Add a New Vehicle to the Garage**:
   - Supports five types of vehicles:
     - Regular Motorcycle
     - Electric Motorcycle
     - Regular Car
     - Electric Car
     - Truck
   - Automatically manages vehicle states:
     - If the vehicle already exists, updates its state to *"In Repair"*.
     - Otherwise, prompts the user to input details about the vehicle and its wheels.

2. **View List of Vehicles**:
   - Displays all vehicle license numbers currently in the garage.
   - Includes filtering options based on vehicle state.

3. **Change Vehicle State**:
   - Update the state of a specific vehicle (e.g., *"Paid"*, *"Fixed"*, or *"In Repair"*).

4. **Inflate Wheels to Maximum**:
   - Automatically inflates all wheels of a specified vehicle to their maximum pressure.

5. **Refuel Vehicles**:
   - Allows refueling of fuel-based vehicles with a specified type and quantity of fuel.
   - Ensures that the fuel type matches the vehicle's requirements and the amount does not exceed the tank's capacity.

6. **Charge Electric Vehicles**:
   - Charges the battery of electric vehicles by a specified duration (in hours).
   - Ensures the charging time does not exceed the maximum capacity of the battery.

7. **Display Vehicle Details**:
   - Provides full details for a specified vehicle, including:
     - License Number
     - Model Name
     - Owner Name and Contact
     - Garage Status
     - Wheels Information (Manufacturer, Pressure)
     - Energy Source (Fuel Type and Amount or Battery Status)
     - Additional details specific to the vehicle type:
       - **Motorcycles**: Engine volume, license type.
       - **Cars**: Color, number of doors.
       - **Trucks**: Cargo volume, hazardous material indicator.

---

## Technologies and Skills Demonstrated
- **C# OOP**: Implemented classes with inheritance and polymorphism.
- **Collections**: Managed dynamic lists of vehicles and their components.
- **Enums**: Used for properties like fuel type, license type, and garage status.
- **Multi-Project Solution**: Divided the system into multiple projects for modularity.
- **External Assemblies**: Incorporated `.dll` files for reusable components.
- **Exception Handling**: Ensured user inputs are validated and errors are handled gracefully.

---

## System Design
### Vehicle Types
Each vehicle type extends the base `Vehicle` class, inheriting common attributes and methods. Unique features are added through specialized properties and methods:
- **Motorcycle**:
  - License Type
  - Engine Volume
- **Car**:
  - Color
  - Number of Doors
- **Truck**:
  - Hazardous Material Indicator
  - Cargo Volume

### Core Functionalities
- **Wheel Management**: Each vehicle contains a collection of `Wheel` objects with attributes like manufacturer, current air pressure, and maximum air pressure.
- **Energy Management**: Separate handling for fuel-based and electric vehicles, ensuring proper validation during refueling or charging operations.

---

## Installation and Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo-name/garage-management-system.git
