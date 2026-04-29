# PCB Design Portfolio
This repository contains my original hardware designs developed in KiCad 10. These projects focus on power regulation and PCB layout best practices, including thermal management and signal integrity.


## 1. 12V AC to 5V DC Linear Power Supply
   This project is a regulated power supply designed to convert 12V AC input into a stable 5V DC output.
   ### Technical Design Details
      * Rectification Stage:
            Uses a full-bridge rectifier consisting of four 1N4007 diodes to convert the AC input to pulsating DC.
      * Regulation:
            Features an LM7805 linear regulator in a TO-220 package to provide a constant 5V output.
      * Filtering System:
         - A large **1000µF** electrolytic capacitor (C1) is used for bulk smoothing of the rectified AC ripple.
         -  0.1µF ceramic capacitors (C2, C3) are placed close to the regulator pins to filter out high-frequency noise.
      * Circuit Protection:
            Includes an input fuse (F1) to protect the components from overcurrent or short-circuit conditions.                   
      * Visual Indication:
            An on-board LED with a **2.2kΩ** resistor provides immediate status of the output power.
   ## PCB Layout Strategy
   The layout focuses on safety and stability. I prioritized proper spacing between the AC input terminals and the DC output to prevent interference and ensured the **LM7805** has enough space for heat dissipation.
## 2. Adjustable DC-DC Buck Converter
   This project is a high-efficiency switching regulator based on the **LM2596-ADJ** IC, used for stepping down DC voltages.
   ### Technical Design Details
    *  Switching Regulator:
           Powered by the **LM2596S-ADJ**, which operates at a switching frequency of **150kHz** for high efficiency.
    * Adjustable Output:
          Uses a **10kΩ** potentiometer (RV1) in the feedback loop, allowing the user to precisely set the desired output voltage.
    * Power Components:
       - A **47µH** inductor (L1) and a Schottky diode (D2) are used for energy storage and current steering during the switching cycle.         -  Features a **100µF** input cap and a **220µF** output cap to stabilize the switching waveforms.
    * Indication:
           Includes a power-on LED with a **4.7kΩ** resistor.
## PCB Layout Strategy
For this layout, I focused on Power Integrity:
  * **Wide Copper Pours**: I used large copper areas for the VIN and VOUT nets to handle higher currents without overheating the traces.
  * **Switching Loop** : I placed the diode, inductor, and IC as close together as possible to minimize the loop area, which helps reduce EMI (Electro-Magnetic Interference).
  * **Ground Plane**: A solid ground reference was used to ensure low-noise operation of the feedback pin.
  
  
# Tools & Methodology
### * Software: KiCad 10.0
### * Process : Schematic Capture → Footprint Assignment → PCB Routing → 3D Visualization → PDF Documentation.




Contact: sandhyana384@gmail.com
