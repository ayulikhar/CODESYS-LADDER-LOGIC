# CODESYS PLC Projects

A collection of PLC automation projects developed using **CODESYS V3.5** and Ladder Diagram (LD). These projects demonstrate basic industrial automation concepts, including timed sequencing, motor control, sensor-based operation, and process control.

## Projects

### 1. Automatic Coffee & Tea Vending Machine

**Objective:** Develop a PLC-based vending machine program that simulates the dispensing of coffee or tea.

**Features**
- Coffee and tea selection logic
- Timed beverage dispensing
- Optional milk dispensing
- Start and reset controls
- Ready and busy status indicators

**Logic screenshots:**
<img width="1917" height="1016" alt="Screenshot 2026-10-12 212528" src="https://github.com/user-attachments/assets/0ee572ec-c9a3-4d38-ab81-1b8d39822a59" />

<img width="1917" height="1018" alt="Screenshot 2026-10-12 212627" src="https://github.com/user-attachments/assets/2317da60-0b9e-4990-85fa-90f0fe491daf" />


### 2. Automatic Traffic Light Control System

**Objective:** Implement a traffic light controller that sequences signals for two roads using timers.

**Features**
- Green and yellow signal sequencing for both roads
- Timer-based transitions
- Red-light indication
- Configurable signal durations

**Logic screenshots:** 
<img width="1062" height="697" alt="Screenshot 2026-10-12 200037" src="https://github.com/user-attachments/assets/d42d9a2f-977a-40e1-9ec6-c1c24c12db3c" />

<img width="1917" height="1021" alt="Screenshot 2026-10-12 204903" src="https://github.com/user-attachments/assets/3831d2f9-dfdc-4179-ac11-f054e2e8925d" />

### 3. Automatic Car Wash System

**Objective:** Develop a PLC-based automatic car wash system using Ladder Diagram (LD) in CODESYS.

**Features**
- Start and stop control
- Sequential car wash operations
- Timer-based control of washing stages
- Automated control of outputs such as water spray and cleaning mechanisms
- Sequential operation of the car wash cycle

  
**Logic screenshots:** 
<img width="1917" height="1017" alt="Screenshot 2026-10-12 205034" src="https://github.com/user-attachments/assets/205f35b2-2b4e-4783-bb33-fe9d75221889" />
<img width="1917" height="1018" alt="Screenshot 2026-10-12 205131" src="https://github.com/user-attachments/assets/d1bb49b5-f273-416d-8d5b-9d459bb18553" />



## Tools & Technologies

- CODESYS V3.5
- Ladder Diagram (LD)
- PLC timers (TON)
- Counter function blocks (CTU)
- Boolean logic and internal variables
- Sensor and actuator simulation

## Repository Structure

```text
CODESYS-PLC-Projects/
├── README.md
├── Coffee-Tea-Vending/
├── Traffic-Light-Control/
└── Automatic Car Wash/
```

## How to Use

1. Install CODESYS V3.5.
2. Clone or download this repository.
3. Open the relevant `.project` file in CODESYS.
4. Review the ladder logic and variable declarations.
5. Configure a compatible runtime or simulation target before running the program.

## Note

These projects are intended for educational purposes and PLC programming practice. Screenshots illustrate the ladder logic; actual execution requires the corresponding project files and a compatible runtime configuration.
