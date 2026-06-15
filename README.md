# Wardi 

Wardi , or also  known as Electronic Speed Controller is a device designed to controller the Brushless DC MOtor (BLDC). 


<img width="420" height="595" alt="zine" src="https://github.com/user-attachments/assets/d5ddd2cd-62eb-483a-a75b-c0215223ebb6" />



## What is this Project?
Wardi, also known as Electronic Speed  Controller is a device that is used to operate Brushless DC motors. IT contains mosfets which is used to controll the 3 phase brushless Dc motor. For this Specific ESC I have used 2 mosfet per phase meaning there are total 24 mosftes. 


- BSZ040N06LS5 mosfets
- MCU STM32G071
- Gate driver FD6288Q


## How to use Wardi?
- There are 9 Solder pads! Each solder pad is seperated 3 group of each!
- The BLDC motor has also 3 Wires each motor.
- So first solder each wire to the respective.

## Reason for building this
Well all the traditional ESC i see was either one single one per motor but also 30-40A and after that alot expensive.
And also the traditional 4-in-1 esc were there but lower amps such as 20-60A.
And i wanted a bit more powerful one my Motors were of 80A and i couldnt find any over here so this was the reason i sttarted building this.



## CAD
<img width="786" height="633" alt="Screenshot 2026-06-14 024650" src="https://github.com/user-attachments/assets/e8e4c563-497f-4bd1-8aa4-898888a03172" />
<img width="642" height="363" alt="Screenshot 2026-06-14 024638" src="https://github.com/user-attachments/assets/9d90f81d-03c5-4e56-b6fa-263801cc7c9a" />
<img width="452" height="398" alt="Screenshot 2026-06-14 024548" src="https://github.com/user-attachments/assets/aafbc479-7394-4af8-a5d8-b234dd34820b" />




## Circuit 
### MOSFETs
<img width="257" height="183" alt="Screenshot 2026-06-14 114349" src="https://github.com/user-attachments/assets/0129e1b6-53c3-4c62-9f01-5138d87c008f" />

### MCUs
<img width="282" height="200" alt="Screenshot 2026-06-14 114404" src="https://github.com/user-attachments/assets/ede08742-2dc7-4c85-8698-5a467d72a85b" />

### GATE DRIVERs
<img width="258" height="188" alt="Screenshot 2026-06-14 114357" src="https://github.com/user-attachments/assets/c658d8f2-3330-4557-ba2b-0a51f12f4cb0" />

### BEMF & POWER
<img width="252" height="173" alt="Screenshot 2026-06-14 114411" src="https://github.com/user-attachments/assets/4ac18278-da56-4ad3-ac01-5e2d6c0198d7" />

## PCB
<img width="1070" height="612" alt="Screenshot 2026-06-14 114752" src="https://github.com/user-attachments/assets/b85a8e5d-6d84-4fff-bf78-99747b523205" />
<img width="696" height="493" alt="Screenshot 2026-06-14 114828" src="https://github.com/user-attachments/assets/c2e1eb0e-c8b6-49e1-aa5d-1d01bc174f6f" />


# BOM
| #  | Designator                                                                     | Footprint    | Description                                   | LCSC #   | Qty | Unit (USD) | Link                                              |
|----|--------------------------------------------------------------------------------|--------------|-----------------------------------------------|----------|-----|------------|---------------------------------------------------|
| 1  | U6,U7,U8,U9                                                                    | LQFP-48      | STM32G071CBT6  ARM Cortex-M0+  64KB Flash     | C432212  | 4   | $1.850     | https://www.lcsc.com/product-detail/C432212.html  |
| 2  | U2,U3,U4,U5                                                                    | QFN-24       | FD6288Q  3-Phase Gate Driver  AM32 compatible | C328453  | 4   | $0.850     | https://www.lcsc.com/product-detail/C328453.html  |
| 3  | Q25-Q48                                                                        | DFN-8        | BSZ040N06LS5  60V 40A N-ch MOSFET  x24        | C3279309 | 24  | $0.420     | https://www.lcsc.com/product-detail/C3279309.html |
| 4  | U12                                                                            | SOIC-8-EP    | LM5164QDDATQ1  100V Buck Regulator            | C1850350 | 1   | $2.100     | https://www.lcsc.com/product-detail/C1850350.html |
| 5  | U10                                                                            | SOT-89-3     | CJA1117B-3.3  3.3V 1A LDO Regulator           | C24253   | 1   | $0.120     | https://www.lcsc.com/product-detail/C24253.html   |
| 6  | L1                                                                             | IND-SMD      | CY75-68UH  68uH Power Inductor  Sumida CD73   | C2929442 | 1   | $0.850     | https://www.lcsc.com/product-detail/C2929442.html |
| 7  | D14-D37                                                                        | SOD-323      | BAT54WS  Schottky Diode  30V 200mA  x24       | C466657  | 24  | $0.030     | https://www.lcsc.com/product-detail/C466657.html  |
| 8  | U1                                                                             | CONN-TH      | S8B-PH-K-S(LF)(SN)  8-Pin JST PH Connector    | C157915  | 1   | $0.180     | https://www.lcsc.com/product-detail/C157915.html  |
| 9  | R25-R28,R35-R37,R44-R46,R53-R55,R62-R64                                        | R0402        | 1k ohm  0402WGF1001TCE  x16                   | C11702   | 16  | $0.001     | https://www.lcsc.com/product-detail/C11702.html   |
| 10 | R29-R34,R38-R43,R47-R52,R56-R61                                                | R0402        | 10k ohm  0402WGF1002TCE  x24                  | C25744   | 24  | $0.001     | https://www.lcsc.com/product-detail/C25744.html   |
| 11 | R66                                                                            | R0402        | 453k ohm  0402WGF4533TCE                      | C27009   | 1   | $0.001     | https://www.lcsc.com/product-detail/C27009.html   |
| 12 | R69-R92                                                                        | R0603        | 10 ohm  RC0603FR-0710RL  Gate resistors  x24  | C109318  | 24  | $0.002     | https://www.lcsc.com/product-detail/C109318.html  |
| 13 | R67                                                                            | R0603        | 10.2k ohm  RMC060310.2K1%N                    | C269897  | 1   | $0.010     | https://www.lcsc.com/product-detail/C269897.html  |
| 14 | R68                                                                            | R0603        | 75k ohm  0603WAF7502T5E                       | C23242   | 1   | $0.010     | https://www.lcsc.com/product-detail/C23242.html   |
| 15 | R65                                                                            | R0603        | 100k ohm  0603WAF1003T5E                      | C25803   | 1   | $0.010     | https://www.lcsc.com/product-detail/C25803.html   |
| 16 | C98-C101,C103-C106,C109-C112,C115-C118,C121-C123,C127-C129,C133-C135,C139-C141 | C0402        | 1uF  CL05A105KA5NQNC  x28                     | C52923   | 28  | $0.003     | https://www.lcsc.com/product-detail/C52923.html   |
| 17 | C158                                                                           | C0402        | 2.2nF  0402B222K500NT                         | C1531    | 1   | $0.003     | https://www.lcsc.com/product-detail/C1531.html    |
| 18 | C159                                                                           | C0402        | 3.3nF  TCC0402X7R332K500AT                    | C696855  | 1   | $0.003     | https://www.lcsc.com/product-detail/C696855.html  |
| 19 | C97,C108,C114,C120,C126,C132,C138,C144-C156                                    | C0402        | 10nF  CC0402KRX7R9BB103  x20                  | C60133   | 20  | $0.003     | https://www.lcsc.com/product-detail/C60133.html   |
| 20 | C41                                                                            | C0402        | 22uF  GRM155R60J226ME11D                      | C415703  | 1   | $0.060     | https://www.lcsc.com/product-detail/C415703.html  |
| 21 | C124,C130,C136,C142                                                            | C0402        | 100nF  CL05B104KO5NNNC  x4                    | C1525    | 4   | $0.003     | https://www.lcsc.com/product-detail/C1525.html    |
| 22 | C125,C131,C137,C143                                                            | C0603        | 1uF  CL10A105KB8NNNC  x4                      | C15849   | 4   | $0.011     | https://www.lcsc.com/product-detail/C15849.html   |
| 23 | C162-C185                                                                      | C0603        | 22nF  CL10B223KB8NNNC  x24                    | C21122   | 24  | $0.003     | https://www.lcsc.com/product-detail/C21122.html   |
| 24 | C160                                                                           | C0603        | 56pF  CC0603JRNPO9BN560                       | C107053  | 1   | $0.003     | https://www.lcsc.com/product-detail/C107053.html  |
| 25 | C40,C42-C61,C102,C107,C113,C119,C186-C189                                      | C1206        | 10uF  CL31A106KBHNNNE  x29                    | C13585   | 29  | $0.012     | https://www.lcsc.com/product-detail/C13585.html   |
| 26 | C161                                                                           | C1206        | 47uF  CL31A476MPHNNNE                         | C96123   | 1   | $0.050     | https://www.lcsc.com/product-detail/C96123.html   |
| 27 | C157                                                                           | CAP-SMD-Elec | 2.2uF 50V  RVT1H2R2M0405  Electrolytic        | C970595  | 1   | $0.050     | https://www.lcsc.com/product-detail/C970595.html  |



## HOw to build!

<img width="258" height="188" alt="Screenshot 2026-06-14 114357" src="https://github.com/user-attachments/assets/334dfc0a-329e-462e-8596-a2cb2d2fcae9" />
<img width="257" height="183" alt="Screenshot 2026-06-14 114349" src="https://github.com/user-attachments/assets/fdad7ffb-0954-403d-8653-4f0697d6000a" />
<img width="282" height="200" alt="Screenshot 2026-06-14 114404" src="https://github.com/user-attachments/assets/9c90a901-0172-4842-898f-7ecc146de309" />
<img width="252" height="173" alt="Screenshot 2026-06-14 114411" src="https://github.com/user-attachments/assets/2165f0f0-3ce3-4d04-bf68-091a6045e037" />


### What you need
- Soldering iron (fine tip recommended)
- Solder wire
- Flux
- Multimeter



### Assembly order
1. Solder all the SMD passives first (resistors, capacitors)
2. Solder ICs - MCU STM32G071, Gate driver FD6288Q, BSZ040N06LS5 mosfets
3. Solder the JST connector.
4. Solder the BLDC motor.
5. Connect to a flight controller via the JST connector.


### Firmware Setup

The esc runs on AM32, an open source ESC firmware which manages motor control, communication via dshot, and telemetry.

#### Bootloader

First of all, we need to install the bootloader onto each of the chips. There are overall 4 MCUs each one for each BLDC MOTOR. For each chip, connect via the exposed SWLINK communicatino links swdio/swclk, as outlined in the following table, and flash the bootloader hex file from **firmware/**

#### Firmware

Next connect the flight controller (which should be flashed before this step),
visit [am32 configurator](https://am32.ca/) and upload the firmware from **firmware/**



# Feature
- 60-80A continuous Current
- 101A brust peak current
- upto 6s
- BEC 3.3v
- DSHOT protocol support



