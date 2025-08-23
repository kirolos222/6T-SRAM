# 6T-SRAM
## introduction
SRAM(static memory access) serves as primary memory for cache and embedded application used in modern digital world, the project shows 6T-SRAM in gf22nm which introduce a leackage current, variablilty to process variation and reduced noise margin.

## Simulation analysis summary
Simulations were conducted in Cadence Virtuoso using the gf22nm FDSOI process design kit (PDK). Key observations include:

Read Operation: The cell successfully holds data with minimal bit line disturbance. Read SNM analysis shows a noise margin of approximately XX mV, indicating robust stability during read.

Write Operation: The access transistor sizing allows data to be written reliably at nominal supply voltage. Write delay is measured to be YY ps.

Hold State: The cell maintains data integrity without word line activation, with static noise margins supporting stable data retention.

Power Analysis: Leakage currents increase due to technology scaling but remain within acceptable limits. Dynamic power consumption is minimized by optimized transistor sizing and short bit line activity.

Process Variation: Monte Carlo simulations confirm the design's tolerance to variations in threshold voltage and channel length, ensuring functional reliability across corners.

# Read operation

During a read operation of a '1' (Q=1, Q'=0), the activated word line (W_L=1) allows the cell to influence the precharged bit lines. The Bit_Bar side discharges through the access transistor and the pull-down path of the cell, causing its voltage to decrease. This creates a voltage differential between Bit (which remains high) and Bit_Bar (which decreases). This differential is detected by the sense amplifier, which amplifies it to output a valid logic '1'.

<img width="1368" height="669" alt="image" src="https://github.com/user-attachments/assets/efbf9f9a-f8d4-48f9-a0da-f246659f942b" />

the static noise margin in read operation is :

<img width="1262" height="641" alt="image" src="https://github.com/user-attachments/assets/89820001-695b-474d-a802-04d1417f7f4b" />

