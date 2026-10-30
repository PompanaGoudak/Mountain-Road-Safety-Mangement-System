# Mountain-Road-Safety-Mangement-System
Smart Road Safety and Vehicle Accident Prevention for Mountain Roads
# Smart Road Safety and Vehicle Accident Prevention for Mountain Roads

## 1. Project Overview

Road accidents are common on narrow mountain roads because of sharp turns, blind curves, steep slopes and limited road width. In some mountain areas, vehicles coming from opposite directions cannot see each other clearly.

This project, **Smart Road Safety and Vehicle Accident Prevention for Mountain Roads**, is designed to reduce the risk of accidents by controlling vehicle movement using an automatic traffic signal system.

The system uses an Arduino UNO to detect vehicles approaching from two different sides. Based on the detection, it controls red, yellow and green LEDs. A 16x2 LCD displays the current road condition, and a buzzer provides an alert during dangerous situations.

The complete project is designed and tested using the Wokwi online simulator.

## 2. Problem Statement

Narrow mountain roads and sharp bends create difficulties for drivers because vehicles approaching from opposite directions may not be visible to each other.

When two vehicles enter a narrow road section at the same time, there is a possibility of collision.

Traditional traffic signals may not be available in remote mountain areas. Therefore, an automatic system is required to detect approaching vehicles and provide suitable warning signals.

This project aims to develop a simple and low-cost road safety system that helps control vehicle movement and reduces the possibility of accidents on narrow mountain roads.

## 3. Objectives

The main objectives of this project are:

- To detect vehicles approaching from two different sides.
- To control vehicle movement using automatic traffic signals.
- To use red, yellow and green LEDs to indicate road conditions.
- To display vehicle detection information on a 16x2 LCD.
- To activate a buzzer during dangerous situations.
- To reduce the possibility of collisions on narrow mountain roads.
- To develop a simple and affordable road safety solution.
- To simulate and test the system using Wokwi.

## 4. Components Used

The following components are used in the project:

| Component | Purpose |
|---|---|
| Arduino UNO | Main controller of the system |
| Red LEDs | Indicate that vehicles must stop |
| Yellow LEDs | Provide warning and caution signals |
| Green LEDs | Indicate that vehicles can proceed |
| 16x2 LCD | Displays road conditions and warning messages |
| Buzzer | Produces an alert during dangerous conditions |
| Pushbuttons | Simulate vehicle detection sensors in Wokwi |
| Connecting wires | Connect all electronic components |

**Note:** In the Wokwi simulation, pushbuttons are used instead of actual IR obstacle sensors to represent vehicle detection.

## 5. Software Requirements

- **Wokwi Simulator:** Used to design the circuit and test the project virtually.
- **Arduino IDE:** Used to write and compile the Arduino program.

## 6. System Architecture

The system contains two vehicle detection sections:

- Side A: Detects vehicles approaching from one direction.
- Side B: Detects vehicles approaching from the opposite direction.

The Arduino UNO receives the detection signals and processes them. Based on the input conditions, it controls the traffic LEDs, LCD and buzzer.

### System Flow

1. Vehicle detection inputs are received from Side A and Side B.
2. Arduino UNO checks the input conditions.
3. The controller identifies whether the road is empty or vehicles are approaching.
4. Traffic LEDs are controlled according to the detected condition.
5. The LCD displays the current road status.
6. The buzzer provides an alert when vehicles are detected from both sides.

## 7. Working Principle

The project works based on vehicle detection from two opposite directions.

### Condition 1: No Vehicles Detected

When no vehicles are detected from either side, both green LEDs turn ON.

The LCD displays:

`EMPTY ROAD`

This indicates that the road is clear in the simulation.

### Condition 2: Vehicle Detected from Side A

When a vehicle is detected from Side A, the red LED on Side A turns ON, and the green LED on Side B turns ON.

The LCD displays:

`VEHICLE SIDE A`

This indicates that Side A must stop while Side B is allowed to proceed.

### Condition 3: Vehicle Detected from Side B

When a vehicle is detected from Side B, the red LED on Side B turns ON, and the green LED on Side A turns ON.

The LCD displays:

`VEHICLE SIDE B`

This indicates that Side B must stop while Side A is allowed to proceed.

### Condition 4: Vehicles Detected from Both Sides

When vehicles are detected from both sides at the same time, both red LEDs turn ON and the buzzer is activated.

The LCD displays:

`STOP BOTH SIDES`

`DANGER ALERT!`

This indicates a dangerous situation and warns vehicles to stop.

## 8. Pin Connections

### Traffic LEDs

| Component | Arduino Pin |
|---|---|
| Side A Red LED | D2 |
| Side A Yellow LED | D3 |
| Side A Green LED | D4 |
| Side B Red LED | D5 |
| Side B Yellow LED | D6 |
| Side B Green LED | D7 |

### LCD Connections

| LCD Pin | Arduino Pin |
|---|---|
| RS | D8 |
| EN | D9 |
| D4 | D10 |
| D5 | D11 |
| D6 | D12 |
| D7 | D13 |

### Other Connections

| Component | Arduino Pin |
|---|---|
| Side A Pushbutton | A0 |
| Side B Pushbutton | A1 |
| Buzzer | A2 |

The pushbuttons are connected using the Arduino internal pull-up resistors (`INPUT_PULLUP`).

## 9. Simulation and Testing

The project is simulated using the Wokwi online simulator.

Different input conditions are tested to verify the working of the system.

| Test | Side A | Side B | Expected Result |
|---|---|---|---|
| Test 1 | No vehicle | No vehicle | Both green LEDs ON |
| Test 2 | Vehicle detected | No vehicle | Side A red, Side B green |
| Test 3 | No vehicle | Vehicle detected | Side A green, Side B red |
| Test 4 | Vehicle detected | Vehicle detected | Both red LEDs ON and buzzer ON |

The simulation helps verify whether the Arduino receives the correct inputs and controls the output devices according to the programmed conditions.

## 10. Advantages

- Simple and easy-to-understand design.
- Low-cost electronic components.
- Automatic vehicle detection logic.
- Provides visual warning signals.
- LCD displays the current road condition.
- Buzzer provides an additional warning.
- Can be tested without physical hardware using Wokwi.

## 11. Limitations

- The current project uses pushbuttons as simulated vehicle sensors.
- It does not physically detect real vehicles in the Wokwi simulation.
- The basic control logic does not include vehicle clearance timing.
- It does not use wireless communication between distant road sections.
- It is a prototype and is not suitable for direct real-world traffic control without further development and safety testing.

## 12. Future Scope

The project can be improved in several ways:

- Replace simulated pushbuttons with actual IR obstacle sensors or suitable vehicle detection sensors.
- Add wireless communication between two road sections.
- Include automatic timing and vehicle clearance detection.
- Add solar power to support remote mountain locations.
- Use cameras and AI techniques for advanced vehicle detection.
- Add emergency vehicle detection.
- Develop a more reliable fail-safe traffic management system.

## 13. Conclusion

The Smart Road Safety and Vehicle Accident Prevention for Mountain Roads project demonstrates a simple method of controlling vehicle movement on narrow mountain roads.

The system uses Arduino UNO, LEDs, an LCD and a buzzer to indicate road conditions and provide warnings when vehicles approach from opposite directions.

The Wokwi simulation demonstrates the basic working of the system under different vehicle detection conditions.

This project provides a foundation for developing more advanced and reliable road safety systems for narrow roads and mountain areas.

## 14. Project Simulation Link

**Wokwi Project:**  
https://wokwi.com/projects/479237136342909953

## 15. Repository Contents

- `sketch.ino` – Arduino source code.
- `diagram.json` – Wokwi circuit configuration.
- `libraries.txt` – Required libraries, if applicable.
- `README.md` – Project documentation.
