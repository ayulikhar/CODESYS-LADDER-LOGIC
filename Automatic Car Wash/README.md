# Automated Car Wash: Multi-Stage Process Control

**Domain:** Industrial Automation · Process Sequencing · Conveyor Control

## Overview

This project models an automated car-wash process using PLC ladder logic. The system coordinates vehicle movement with three sequential processing stages: water washing, soap application, and drying.

The objective is to translate a multi-stage process into a structured control sequence using timed operations and actuator outputs. The project emphasizes the relationship between transport, process timing, and coordinated equipment operation.

## Process Architecture

The simulated process consists of three sequential zones:

1. **Water-washing stage:** Represents the initial cleaning operation.
2. **Soap-application stage:** Represents detergent application.
3. **Drying stage:** Represents the final processing operation before the vehicle exits.

A conveyor motor represents vehicle transport between stages. Separate output signals represent the washing, soap, and drying equipment.

## Control Strategy

The ladder logic coordinates the sequence through TON function blocks and Boolean conditions. Timer completion signals provide transition conditions between transport intervals and processing operations.

The nominal timing scheme uses a 15-second travel interval per zone, a 10-second process interval, and a 5-second entry/exit margin. These values represent the configured simulation timing and should be checked against the actual timer-input logic in the project.

The implementation uses six timer instances to coordinate the three zones and their associated operations.

## Implementation Details

| Element | Function |
|---|---|
| Conveyor motor output | Represents vehicle movement |
| Water-wash output | Represents the first processing stage |
| Soap output | Represents detergent application |
| Dryer output | Represents the final processing stage |
| TON function blocks | Provide timing conditions |
| Boolean contacts and coils | Coordinate stage transitions and outputs |

The control program demonstrates how a process can be divided into functional stages and represented through readable ladder-logic networks.

## Verification Plan

The intended validation cases are:

- Verify the order of the three processing stages.
- Check that each output activates only during its intended interval.
- Verify the relationship between conveyor movement and processing.
- Confirm that timer completion advances the sequence as intended.
- Check the behavior at the beginning and end of a complete cycle.

Record observed behavior after running the program in the PLC environment.

## Technology Stack

- CODESYS V3.5
- IEC 61131-3 Ladder Diagram
- TON timer function blocks
- Boolean control logic
- PLC simulation

## Relevance to Automation and Instrumentation

This project provides experience with multi-stage process control, timer-based sequencing, actuator coordination, and control-logic verification. Similar principles are used in automated material handling, production lines, and laboratory workflows.

## Repository Contents

- Native PLC project
- Ladder-logic screenshots
- Timer and variable configuration

**Scope:** Educational simulation. A physical implementation would require vehicle-position sensing, actuator feedback, emergency-stop circuitry, appropriate interlocks, and validation of the actual process timings.
