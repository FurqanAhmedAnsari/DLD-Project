# 24 JK Flip-Flop Digital Counter

A digital counter circuit implemented using 24 JK flip-flops that displays time in HH:MM:SS format, designed and simulated in Proteus ISIS.

## 📋 Project Overview

This project implements a continuous digital counter using discrete JK flip-flops to count seconds, minutes, and hours. The counter displays time in a 24-hour format (HH:MM:SS) using 7-segment displays and operates with a 1Hz clock source.

**Note**: This counter operates as a continuous counter and does not reset after 24 hours - it continues counting indefinitely until manually stopped.

## 🔧 Circuit Specifications

### Core Components
- **24 JK Flip-Flops**: Primary counting elements
  - 8 flip-flops for seconds counter
  - 8 flip-flops for minutes counter  
  - 8 flip-flops for hours counter
- **Clock Source**: 1Hz frequency generated using 555 timer
- **Display**: 7-segment common cathode displays with 7447 BCD-to-7-segment decoders
- **Logic Gates**: 7408 quad 2-input AND gates for counter logic
- **Power Supply**: Battery with appropriate voltage regulation

### Supporting Components
- 7447 BCD-to-7-segment decoder ICs
- 7-segment displays (common cathode)
- Resistors for current limiting and pull-up/pull-down
- Capacitors for timing and filtering
- 555 timer IC for clock generation

## ⚡ Circuit Operation

### Clock Generation
- 555 timer configured as astable multivibrator
- Generates precise 1Hz clock pulses
- Clock signal drives the seconds counter chain

### Counting Logic
1. **Seconds Counter**: 8 JK flip-flops count from 00 to 59, then overflow to minutes
2. **Minutes Counter**: 8 JK flip-flops count from 00 to 59, then overflow to hours  
3. **Hours Counter**: 8 JK flip-flops count continuously (no 24-hour reset)

### Display System
- Each counter section drives 7447 BCD decoders
- Decoders convert binary output to 7-segment display format
- Six 7-segment displays show HH:MM:SS format
- Current limiting resistors protect displays and maintain brightness

## 🎯 Features

- ✅ Real-time counting at 1Hz rate
- ✅ HH:MM:SS display format
- ✅ Continuous operation (no automatic reset)
- ✅ BCD-to-7-segment decoded output
- ✅ Built entirely with discrete flip-flops
- ✅ Educational demonstration of digital counter design

## 🚀 Getting Started

### Prerequisites
- Proteus ISIS (Version 8.0 or later recommended)
- Basic understanding of digital logic and flip-flops

### Opening the Simulation
1. Download the `.pdsprj` file from this repository
2. Open Proteus ISIS
3. Load the project file: `File → Open → digital_counter.pdsprj`
4. Run the simulation using the play button

### Circuit Operation
1. Power on the circuit (close power switch if present)
2. The 555 timer will begin generating 1Hz clock pulses
3. Observe the 7-segment displays counting in HH:MM:SS format
4. Counter will continue indefinitely until manually stopped

## 🔍 Technical Details

### Flip-Flop Configuration
- All JK flip-flops configured in toggle mode (J=K=1)
- Cascaded connection for binary counting
- Appropriate reset and clock connections

### Timing Analysis
- **Clock Frequency**: 1Hz ±5%
- **Propagation Delay**: Cumulative through flip-flop chain
- **Display Update Rate**: 1 second intervals

### Note: 
- This counter operates continuously and does not implement a 24-hour reset mechanism.
