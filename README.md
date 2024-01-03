![image](https://github.com/afzalamu/Design-of-two-stage-operational-amplifier-at-180nm-Technology/assets/124300839/90772548-30d2-4c20-99eb-8a95b6ed4521)# Design of Two-Stage Operational Amplifier at 180nm Technology

## Project Description
This project involves the design of a two-stage operational amplifier at 180nm technology using the gm over Id methodology. The amplifier is designed to meet specifications such as Gain > 60dB, load capacitance Cl = 20fF, gain bandwidth product (GBW) = 1GHz, and Phase margin > 50 degrees.

## Table of Specifications

| Specification          | Value     |
|------------------------|-----------|
| Gain                   | > 60dB    |
| Load Capacitance (Cl)  | 20fF      |
| GBW                    | 1GHz      |
| Phase Margin           | > 50°     |

## Design Details

### Model and Methodology
- **Model File:** CMOS180nm
- **Design Methodology:** gm over ID methodology (Emphasis on optimized W/L ratio and Width/Length multiples of 0.18nm)

### Prerequisites
Before designing, the following steps were taken:
- Used Analog Designer Toolbox (ADT) for generating parameter charts using the CMOS180.txt model file.
- ADT allows plotting various parameter charts for NMOS and PMOS devices, considering different specifications such as length, VDS, VSB, etc.

### Tools Used
- LTspice: Schematic and simulation purposes
- ADT (Analog Designer Toolbox): Generating lookup tables for CMOS 180nm and parameter charts for gm over Id methodology
- Electric Binary Software: Layout design

### Calculations for the First Stage
- Gain = 40  , "CL" =20f , Rout = 93 KΩ (Assumed after Back Calculations)
- Let 𝐺𝑚= 𝐺𝑎𝑖𝑛/𝑅𝑜𝑢𝑡 = 0.43mS 
![image](https://github.com/afzalamu/Design-of-two-stage-operational-amplifier-at-180nm-Technology/assets/124300839/9769efeb-24d5-490d-ba47-53cef894966b)


- 𝐺𝑚/𝐼𝑑 = 0.43mS/12 = 35.83uA
- Various calculations for NMOS and PMOS.

### Calculations for Next Stage (Common Source using PMOS and Current Source Load)
- Gain = 28, CL = 20f
- Various calculations for PMOS and NMOS.

## Schematic Pictures
[Insert Schematic Pictures here]

## Simulation Pictures
[Insert Simulation Pictures here]

## Simulation Results
- GBW: 1.01 GHz
- Gain: 1125 (61.03dB)
- Phase Margin: 47°

## References
- "The Gm/Id Design Methodology Demystified" by Dr. Hesham Omran
- "CMOS Analog IC Design Lectures" by Dr. GS Javed
- "The Design of TWO STAGE Miller OpAmp: Final Verdict" by Dr. Hesham Omran
- NPTEL IIT Madras Course on OpAmp (Lecture 1, Lecture 2, Lecture 3)
