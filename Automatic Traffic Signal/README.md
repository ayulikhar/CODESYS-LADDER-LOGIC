# Timer-Based Two-Road Traffic Signal Controller

**Domain:** Sequential Control · Boolean Logic · Timer Coordination

## Overview

This project explores the implementation of a two-road traffic signal controller using CODESYS V3.5 and IEC 61131-3 Ladder Diagram (LD).

The controller represents traffic phases through Boolean output signals and cascaded TON timers. It provides a practical setting for studying state transitions, timing dependencies, and the relationship between internal logic and externally visible system behavior.

## Control Objective

Coordinate the signal sequence for two roads while avoiding conflicting green-light outputs.

The intended cycle consists of four phases:

| Phase | Road A | Road B | Duration |
|---|---|---|---:|
| 1 | Green | Red | 10 s |
| 2 | Yellow | Red | 3 s |
| 3 | Red | Green | 10 s |
| 4 | Red | Yellow | 3 s |

The sequence is intended to return to Phase 1 after Road B's yellow phase completes.

## Implementation

Four TON function blocks represent the nominal phase durations:

- `TON0`: Road A green, 10 seconds.
- `TON1`: Road A yellow, 3 seconds.
- `TON2`: Road B green, 10 seconds.
- `TON3`: Road B yellow, 3 seconds.

Normally open and normally closed contacts use timer outputs to determine signal states. Output coils represent the red, yellow, and green signals for each road.

The implementation provides a practical exercise in cascading timers, evaluating Boolean conditions, and tracing control behavior during runtime execution.

## Engineering Considerations

A reliable traffic controller must address more than timer completion. Each phase must reset correctly, the next phase must start deterministically, and the output logic must prevent conflicting green signals.

The cycle-restart behavior is therefore an explicit verification requirement for this project. The implementation should not be considered validated until repeated transitions have been observed and signal conflicts ruled out.

## Verification Plan

- Verify the duration of each phase.
- Confirm that Road A and Road B green outputs never overlap.
- Check the transition from green to yellow and yellow to red.
- Confirm that the Road B yellow phase returns the controller to Road A green.
- Run multiple complete cycles and inspect the output states.

## Technology Stack

- CODESYS V3.5
- IEC 61131-3 Ladder Diagram
- TON timers
- Boolean logic and contact-based interlocking
- Online PLC monitoring and simulation

## Relevance to Automation and Instrumentation

The project develops skills in deterministic sequencing, timed control, interlocking, and runtime debugging. These concepts are relevant to laboratory automation, equipment sequencing, and control systems that coordinate multiple outputs under timing constraints.

## Repository Contents

- Native CODESYS project
- Ladder-logic screenshots
- Timer configuration and variable declarations

**Scope:** Educational simulation, not a safety-certified traffic controller. Deployment would require explicit phase-state management, appropriate clearance intervals, fault handling, and independent safety validation.
