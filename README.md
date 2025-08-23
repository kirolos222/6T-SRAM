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

Butterfly graph:

<img width="828" height="638" alt="image" src="https://github.com/user-attachments/assets/1562d4f1-554f-4e11-94f4-ce99036fe436" />
