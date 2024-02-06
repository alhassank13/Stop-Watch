# Stop-Watch
This repository contains the source code and hardware configuration for a Stop Watch system implemented using the ATmega32 microcontroller. The project utilizes Timer1 in CTC mode for accurate time counting and employs six common anode 7-segment displays connected in a multiplexed configuration.

## Project Specifications

1.  **Microcontroller:**
    
    -   ATmega32 with a frequency of 1MHz.
2.  **Timer Configuration:**
    
    -   Configure Timer1 in CTC mode for precise Stop Watch time counting.
3.  **7-Segment Display:**
    
    -   Use six common anode 7-segment displays.
    -   Implement multiplexing using a 7447 decoder for all 7-segments.
    -   Control enable/disable for each 7-segment using NPN BJT transistors connected to MCU pins.
4.  **Multiplexing Technique:**
    
    -   Switch between 7-segment displays to create a continuous display using transistors.
    -   Utilize persistence of vision for a seamless visual experience.
5.  **Hardware Connections:**
    
    -   Connect 7447 decoder to the first 4 pins in PORTC.
    -   Use the first 6 pins in PORTA as enable/disable pins for the six 7-segments.
6.  **Stop Watch Functionality:**
    
    -   Start counting once power is connected to the MCU.
    -   Configure External Interrupt INT0 with a falling edge to reset the Stop Watch time.
    -   Configure External Interrupt INT1 with a rising edge to pause the Stop Watch time.
    -   Configure External Interrupt INT2 with a falling edge to resume the Stop Watch time.

