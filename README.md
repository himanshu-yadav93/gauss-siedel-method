**Gauss-Seidel Load Flow Analysis**

This repository contains a set of MATLAB functions designed to solve the power flow problem for a 6-bus electrical power system. The simulation calculates bus voltage magnitudes and phase angles based on given generation and load parameters.

**Files Included**

gaussiedal.m: The main execution script. It performs the iterative Gauss-Seidel algorithm, handles PV bus to PQ bus switching (Q-limit checking), and calculates the final voltage vectors.
busdata6.m: A function that returns the bus data table, including bus types (Slack, PV, PQ), initial voltages, real/reactive power (generation and load), and reactive power limits.
ybusppg.m: A utility function that constructs the Bus Admittance Matrix and the Bus Impedance Matrix from the system's line data.
linedata6.m: (Required dependency) This file is called by ybusppg.m and should contain the network's line parameters (resistance, reactance, and half-line charging).

**System Configuration**

The provided busdata6.m defines a 6-bus system with the following characteristics:
Bus 1: Slack Bus.
Buses 2 & 3: PV (Generator) Buses with specified voltage setpoints and real power injection.
Buses 4, 5, & 6: PQ (Load) Buses with defined real and reactive power demands.

**How to Run**

 Ensure all .m files are in the same MATLAB directory.
 Open gaussiedal.m.Run the script.
 The command window will display:The total number of iterations required for convergence.
 The final complex voltages. Voltage magnitudes and angles in degrees.
