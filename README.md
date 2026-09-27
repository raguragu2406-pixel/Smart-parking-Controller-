# Smart Parking Controller

## Project Overview
A Smart Parking Controller is a digital RTL-based system used to monitor the number of vehicles in a parking area and control vehicle entry and exit based on available parking capacity.

## Objective
To design and simulate a Verilog RTL-based Smart Parking Controller that:
- Counts occupied parking slots.
- Detects vehicle entry and exit.
- Indicates available parking slots.
- Detects when the parking area is full.
- Controls whether a vehicle is allowed to enter or exit.

## Features
- Vehicle entry detection
- Vehicle exit detection
- Occupied slot counting
- Available slot indication
- Parking full indication
- Entry permission
- Exit permission
- Reset functionality

## RTL Design
The controller is implemented using Verilog RTL.

### Inputs
- `clk` – Clock signal
- `reset` – Reset signal
- `vehicle_entry` – Vehicle entry sensor
- `vehicle_exit` – Vehicle exit sensor

### Outputs
- `occupied_count` – Number of occupied slots
- `slots_available` – Number of available slots
- `parking_full` – Indicates whether parking is full
- `entry_allowed` – Indicates whether entry is allowed
- `exit_allowed` – Indicates whether exit is allowed

The parking capacity used in the design is 8 vehicles.

## Testbench
A Verilog testbench is used to verify the functionality of the Smart Parking Controller.

The testbench verifies:
1. Reset operation
2. Vehicle entry
3. Multiple vehicle entries
4. Parking full condition
5. Vehicle entry when parking is full
6. Vehicle exit
7. Vehicle entry after a slot becomes available

## Simulation Result
The design was successfully compiled and simulated using EDA Playground with the Icarus Verilog simulator.

The `$monitor` statement was used to observe:
- Entry status
- Exit status
- Occupied vehicle count
- Available slots
- Parking full status
- Entry permission

## Expected Working
- After reset, the occupied count is 0.
- When a vehicle enters, the occupied count increases by 1.
- When a vehicle exits, the occupied count decreases by 1.
- When all 8 slots are occupied, `parking_full` becomes 1.
- When the parking area is full, another vehicle cannot increase the occupied count.
- When a vehicle exits, a slot becomes available and another vehicle can enter.

## Tools Used
- Verilog HDL
- EDA Playground
- Icarus Verilog
- GitHub

## Project Structure

```text
Smart-Parking-Controller/
│
├── design.sv
├── tb_smart_parking.sv
├── simulation_output.png
└── README.md
Conclusion
The Smart Parking Controller was successfully designed using Verilog RTL and verified using a testbench. The simulation demonstrates vehicle counting, parking capacity monitoring, entry control, and exit control.
 
