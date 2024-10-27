# Alarm-Clock-Circuit
An original logic circuit for a basic alarm clock. The interface displays time in 12-hour format, indication of AM/PM, and provide the facilities to set the time and an alarm. When the alarm is enabled, an alarm LED is turned on when the time is reached.
![Logo](static.png)
![Logo](operational.png)

## Overview

This repository contains the design and implementation of a basic alarm clock logic circuit developed using Logisim. The clock displays time in a 12-hour format with AM/PM indication, allows users to set the time and alarm, and activates an LED when the alarm time is reached.

## Features

- **12-Hour Format Display**: Time is displayed in a 12-hour format with an AM/PM indicator.
- **Set Time Functionality**: The clock can be paused to set the current time. 
- **Minute and Hour Increment Buttons**: Users can increment the time by pressing buttons to add minutes or hours.
- **Alarm Functionality**: An alarm LED is activated when the alarm time matches the current time.

## Development Stages

### Stage 1: Minute Counter

- Implemented separate counters for the ones and tens columns of the minutes (0-9 for ones, 0-5 for tens).
- Utilized a 4-bit ripple counter to connect to a Hex Digit Display for visual output.
- Added logic to reset the minute counters when they reach 59.

### Stage 2: Set Time Functionality

- Introduced a button to switch to "Set Time" mode, pausing the clock.
- Implemented a button to increment the minute counter manually.
- Used an OR gate to pause the clock when in "Set Time" mode.

### Stage 3: Hour Counter

- Created separate counters for the ones and tens columns of the hours (0-9 for ones, wraps to 0 after 12; 0-1 for tens).
- Added a button to increment the hour display.
- Included an AM/PM LED that toggles state after reaching 12.

### Stage 4: Integration of Counters

- Combined the hour and minute counters to synchronize the clock.
- Set up the system to allow minute overflow to increment the hour counter.

## Logic Gates Used

- **AND Gates**
- **OR Gates**
- **XOR Gates**
- **Inverters**

## Components

- **4-bit Ripple Counters**: Used for counting minutes and hours.
- **JK Flip-Flops**: Implemented for state management of the counters.
- **Hex Digit Displays**: Used to visually represent the time on the clock.

## Installation

1. Download Logisim from [Logisim's official site](http://www.cburch.com/logisim/).
2. Clone this repository:
   ```bash
   git clone https://github.com/your-username/basic-alarm-clock.git
