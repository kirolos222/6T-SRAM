# 6T-SRAM
## introduction
SRAM(static memory access) serves as primary memory for cache and embedded application used in modern digital world, the project shows 6T-SRAM in gf22nm which introduce a leackage current, variablilty to process variation and reduced noise margin.

## Simulation analysis summary
Simulations were conducted in Cadence Virtuoso using the gf22nm FDSOI process design kit (PDK). Key observations include:

Read Operation: The cell successfully holds data with minimal bit line disturbance. Read SNM analysis shows a noise margin of approximately 350 mV, indicating robust stability during read.

Write Operation: The access transistor sizing allows data to be written reliably at nominal supply voltage. Write delay is measured to be 7 ps.

Hold State: The cell maintains data integrity without word line activation, with static noise margins supporting stable data retention.

Power Analysis: Leakage currents increase due to technology scaling but remain within acceptable limits. Dynamic power consumption is minimized by optimized transistor sizing and short bit line activity.

Process Variation: Monte Carlo simulations confirm the design's tolerance to variations in threshold voltage and channel length, ensuring functional reliability across corners.

# Read operation

During a read operation of a '1' (Q=1, Q'=0), the activated word line (W_L=1) allows the cell to influence the precharged bit lines. The Bit_Bar side discharges through the access transistor and the pull-down path of the cell, causing its voltage to decrease. This creates a voltage differential between Bit (which remains high) and Bit_Bar (which decreases). This differential is detected by the sense amplifier, which amplifies it to output a valid logic '1'.

<img width="1368" height="669" alt="image" src="https://github.com/user-attachments/assets/efbf9f9a-f8d4-48f9-a0da-f246659f942b" />

the static noise margin in read operation is :

<img width="1262" height="641" alt="image" src="https://github.com/user-attachments/assets/89820001-695b-474d-a802-04d1417f7f4b" />

PVT variations:

<img width="1912" height="690" alt="image" src="https://github.com/user-attachments/assets/3e75f0bd-cafb-438e-8e12-d12990d5e386" />


## in write operation :
The write operation is initiated by asserting all word lines (W₁, W₂, W₃, W₄ = 1). To write a specific value, the Bit line is driven to a low logic state (GND), while the complementary Bit line is forced to the desired voltage (Vp) through a logic function, effectively creating a strong voltage differential across the cell. This differential is designed to overcome the cell's internal feedback, with the condition that the driving signal (y₁) must be stronger than the cell's retention capability (y_m) to flip its state. The control logic (m₂ = cH, m₁ = 0, g = 1) manages this process, ensuring a successful and reliable write operation.


<img width="1529" height="680" alt="image" src="https://github.com/user-attachments/assets/5336bcc1-db7d-4eb3-920a-463c68ec3109" />

the static noise margin in read operation is :

<img width="1916" height="632" alt="image" src="https://github.com/user-attachments/assets/6f19083f-3dda-438d-93f6-89dcccd5aa77" />

across PVT:

<img width="1541" height="653" alt="image" src="https://github.com/user-attachments/assets/30e83dc2-d950-4445-a5f5-a1401b20e571" />


delay time :

<img width="1919" height="684" alt="image" src="https://github.com/user-attachments/assets/c0adde62-025b-44a3-b933-0b0d02fde9c6" />

## layout :

<img width="1176" height="567" alt="image" src="https://github.com/user-attachments/assets/5710d0af-fa8e-4d92-873f-43ce8f1cd3d9" />

## post layout simulation:

