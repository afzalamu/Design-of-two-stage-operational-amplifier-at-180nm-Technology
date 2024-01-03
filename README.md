# Design of Two-Stage Operational Amplifier at 180nm Technology
![image](https://github.com/afzalamu/Design-of-two-stage-operational-amplifier-at-180nm-Technology/assets/124300839/1792bfa7-0244-4d07-81af-db67d53d9f7c)

## Project Description
This project involves the design of a two-stage operational amplifier at 180nm technology using the GM over Id methodology. The amplifier is designed to meet the specifications: Gain > 60dB, load capacitance Cl = 20fF, gain bandwidth product (GBW) = 1GHz, and Phase margin > 50 degrees.

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
- ADT (Analog Designer Toolbox): Generating lookup tables for CMOS 180nm and parameter charts for GM over Id methodology
- Electric Binary Software: Layout design

### Calculations for the First Stage
- Gain = 40  , "CL" =20f , Rout = 93 KΩ (Assumed after Back Calculations)
- Let 𝐺𝑚= 𝐺𝑎𝑖𝑛/𝑅𝑜𝑢𝑡 = 0.43mS
- Taking  𝐺𝑚/𝐼𝑑=12, Id = 0.43𝑚𝑆/12 = 35.83uA
- **For NMOS:** (From Look Up Tables in ADT)
- For 𝐺𝑚/𝐼𝑑=12, 𝐺𝑚/𝐺𝑑𝑠=77.05, 𝐼𝑑/𝑊=9.913 , Vgs=0.7316 
- Hence,	Gds= 0.43𝑚𝑆/77.05 = 5.58uS 	W= 35.83𝑢/9.913 =3.6u 	and  Vg =0.7316+0.45
- and Vg = 1.18
- **For PMOS:**
- As, Rout = Ro(NMOS) || Ro(PMOS)   	Gds(PMOS)= 1/𝑅𝑂𝑈𝑇 - Gds(NMOS)
- Hence , GDS(PMOS)= 5.172uS
- Now, as the current will remain the same i.e 35.83uA  
- 𝐼𝑑/(𝐺𝑑𝑠(𝑃𝑀𝑂𝑆))= 35.83𝑢/5.17𝑢=6.93    using this From LUT in ADT(Analog Designer Toolbox), Gm/Id is calculated for PMOS
- Hence ,   𝐺𝑚/𝐼𝑑=5.487	Gm (PMOS) = 5.487 * 35.83uA = 0.196mS
- For, 𝐺𝑚/𝐼𝑑=5.487   	 𝐼𝑑/𝑊=10.8	Vsg=0.781
- Hence,	W= 35.83𝑢/10.8 = 3.317  (Taken 3.24u)
- And Vb = 1.8 – 0.781 = 1.019
- AS CL=20f, BW (-3dB) = 𝐺𝑚/(2𝜋𝑅𝑜𝑢𝑡 𝐶𝐿)=85.56MHz

### Calculations for Next Stage (Common Source using PMOS driver and Current Source Load)
- Gain = 28, CL = 20f
- Various calculations for PMOS and NMOS.
- Gain = 28, "CL" =20f 
- **For PMOS:**
- Taking  𝐺𝑚= 8 * 0.43mS = 3.44 mS  	
- As, Av=Gm*Rout		Rout = Av/Gm=8.139K
- Vb(PMOS) = 1.0296 V     	Vsg=0.7704 
- From ADT, For Vsg =0.7704 Gm/Id is Calculated	 𝐺𝑚/𝐼𝑑=5.658	Id=607.8U
- Now, for the above Gm/Id 	   𝐺𝑚/𝐺𝑑𝑠=47.92,    𝐼𝑑/𝑊=10.51 
- Hence ,	Gds = 71.7uS 	W = 57.84u
- **For NMOS:**
- As, Rout = Ro(NMOS) || Ro(PMOS)   	Gds(NMOS)= 1/𝑅𝑂𝑈𝑇 - Gds(PMOS)
- Hence , GDS(NMOS)= 48.5uS
- Now, as the current will remain the same i.e 607.98uA  
- 𝐼𝑑/(𝐺𝑑𝑠(𝑁𝑀𝑂𝑆))=12.534   using this From LUT in ADT, Gm/Id is calculated for NMOS
- Hence, 𝐺𝑚/𝐼𝑑=5.61	Gm (PMOS) = 5.61 * 607.98uA = 3.41mS
- For, 𝐺𝑚/𝐼𝑑=5.61, 𝐼𝑑/𝑊=36.7, Vgs=0.7913
- Hence,	W= 16.56u
  
## Schematic Pictures
**First Stage Schematic**
![image](https://github.com/afzalamu/Design-of-two-stage-operational-amplifier-at-180nm-Technology/assets/124300839/517f9562-aaea-4b91-aa50-543dde734563)
**Second Stage Schematic**
![image](https://github.com/afzalamu/Design-of-two-stage-operational-amplifier-at-180nm-Technology/assets/124300839/58b06365-22d3-4836-937a-6c0bec3c9cb7)
**Two-Stage Operational Amplifier Schematic**
![image](https://github.com/afzalamu/Design-of-two-stage-operational-amplifier-at-180nm-Technology/assets/124300839/d1da8f8a-a900-4ac8-8c65-625a232feb94)

## Simulation Pictures
**Transfer Function**
![image](https://github.com/afzalamu/Design-of-two-stage-operational-amplifier-at-180nm-Technology/assets/124300839/2677fb3c-654a-4575-af90-9e90ee4a80b0)
**Transient Analysis**
![image](https://github.com/afzalamu/Design-of-two-stage-operational-amplifier-at-180nm-Technology/assets/124300839/e1d85ed5-75f6-4532-aa87-2a0ed8d0bf2f)
**Frequency Response**
![image](https://github.com/afzalamu/Design-of-two-stage-operational-amplifier-at-180nm-Technology/assets/124300839/e5e4d721-7075-4bce-893c-78a9243801f2)

## Simulation Results
![image](https://github.com/afzalamu/Design-of-two-stage-operational-amplifier-at-180nm-Technology/assets/124300839/73a7b984-aba1-48ce-8e4c-cd77ea951aea)


## References
- "The Gm/Id Design Methodology Demystified" by Dr. Hesham Omran
- "CMOS Analog IC Design Lectures" by Dr. GS Javed
- "The Design of TWO STAGE Miller OpAmp: Final Verdict" by Dr. Hesham Omran
- NPTEL IIT Madras Course on OpAmp (Lecture 1, Lecture 2, Lecture 3)
