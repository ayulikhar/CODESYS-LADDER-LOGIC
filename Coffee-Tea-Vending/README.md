# PLC-Based Beverage Dispensing System

**Domain:** Industrial Automation · Sequential Control · Timer-Based Actuation

## Overview

This project implements a programmable beverage-dispensing sequence using CODESYS V3.5 and IEC 61131-3 Ladder Diagram (LD). It explores how discrete operator inputs, internal control states, and timed actuator outputs can be coordinated to automate a small process.

The project focuses on the practical implementation of PLC sequencing logic, with an emphasis on predictable output behavior, timer coordination, and readable control logic.

## System Architecture

The control logic is organized into four functional layers:

- **Operator inputs:** Start command, beverage selection, optional milk selection, and reset.
- **Sequence control:** Internal Boolean variables represent the active dispensing stage.
- **Timing:** TON function blocks determine dispensing intervals.
- **Actuator outputs:** Separate outputs represent coffee, tea, and milk dispensing.

## Operating Sequence

1. **Order selection:** The operator initiates an order and selects coffee or tea.
2. **Beverage dispensing:** The selected output is activated for a nominal five-second interval.
3. **Optional milk dispensing:** A separate two-second timer represents the milk-dispensing operation.
4. **Cycle completion:** Status outputs indicate whether the system is busy or ready.
5. **Reset handling:** The reset command is intended to clear the active sequence.

Sugar dispensing is excluded from automatic control and can remain a manual preference.

## Control Implementation

The program uses normally open and normally closed contacts, Boolean coils, internal state variables, and TON timer instances. Timer completion signals provide conditions for changing actuator states.

This structure offers a practical introduction to discrete-event control and the separation of operator commands from process outputs.

## Verification

The intended validation cases are:

- Coffee selection and dispensing.
- Tea selection and dispensing.
- Optional milk operation.
- Correct timer completion and output deactivation.
- Reset behavior and readiness for a subsequent order.

Actual test results should be recorded after these cases have been executed in the PLC runtime.

## Technology Stack

- CODESYS V3.5
- IEC 61131-3 Ladder Diagram
- TON timer function blocks
- Boolean control logic
- PLC simulation

## Relevance to Automation and Instrumentation

This project demonstrates foundational control-system concepts applicable to automated laboratory equipment, sample-handling mechanisms, and small process-control systems: input interpretation, timed actuation, sequencing, and state monitoring.

## Repository Contents

- Native CODESYS project
- Ladder-logic screenshots
- Variable declarations and implementation notes

**Scope:** Educational simulation. Physical deployment would require actuator feedback, suitable electrical interfaces, and appropriate interlocks.
