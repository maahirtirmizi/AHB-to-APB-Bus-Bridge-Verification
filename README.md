# AHB-to-APB Bridge Verification using UVM Methodology
This project focuses on verifying the AHB-to-APB bridge, which acts as an interface between the high-speed AHB (Advanced High-performance Bus) and the lower-performance APB (Advanced Peripheral Bus) using UVM (Universal Verification Methodology). The bridge operates as an AHB slave and an APB master, facilitating communication between these two bus protocols.

Design Under Test (DUT)
The DUT in this project is the AHB-to-APB Bridge, functioning as an AHB Slave and APB Master. The goal is to ensure that data transfers between the AHB Master and APB Slaves are correctly implemented.

Testbench Setup
AHB Master: A single AHB Master is used to drive data to the bridge.
APB Slaves: The bridge communicates with four APB Slaves to perform read and write operations.
Verification Objective
The primary objective is to verify that the data sent by the AHB Master is correctly received by the intended APB Slave, and vice versa. The UVM-based testbench ensures that all aspects of the bridge’s functionality are covered, including correct address latching, decoding, data transfer, and peripheral selection.

Bridge Operations
The AHB-to-APB bridge is responsible for the following tasks:

Address Latching: Latches the address and holds it valid throughout the transfer.
Address Decoding: Decodes the address to generate the appropriate peripheral select signal. Only one select signal is active during each transfer.
Data Transfer: Drives data onto the APB bus during write operations and drives data from the APB bus onto the system bus during read operations.
