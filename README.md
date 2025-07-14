# UART Transmitter and Receiver in Verilog

UART (Universal Asynchronous Receiver and Transmitter) is a widely used serial communication protocol that allows for full-duplex data transmission between two devices without the use of a clock signal. It converts parallel data from the CPU or memory into serial form for transmission and vice versa for reception. This project involves the design, implementation, and simulation of a UART Transmitter and Receiver in Verilog, targeting communication at 115200 baud with a 25 MHz clock.


## Features
- Fully synthesizable Verilog code
- 8-bit data transmission and reception
- Start and stop bit detection
- 16x oversampling for accurate reception
- Baud rate configurable (default: 115200 bps)
- Self-checking testbench
- Waveform dump via VCD for GTKWave

<img width="730" height="593" alt="Screenshot 2025-07-14 at 10 09 20 PM" src="https://github.com/user-attachments/assets/d78877a8-304a-44b3-9d09-4e5390762fd8" />

## UART Working
- UART converts parallel data into serial form for transmission and reconverts it on the receiving side:
- Transmitter adds Start (0) and Stop (1) bits to each 8-bit data frame.
- Receiver detects the Start bit, samples incoming bits using 16x oversampling, and reconstructs the byte.
- No shared clock between transmitter and receiver (asynchronous).
- Baud rate must be matched on both ends.
  
