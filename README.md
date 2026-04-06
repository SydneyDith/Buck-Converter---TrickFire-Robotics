# Buck-Converter---TrickFire-Robotics
Independently developed a 24V-12V buck converter using the TPS563300 IC designed to operate at 3A. Performed calculations to find ideal component values for best performance while refering to the IC datasheet. Designed schematics and PCBs on KiCAD iterating through prototypes as I learned from mistakes.

| Parameter | Value |
| :--- | :--- |
| **Input Voltage** | 24V |
| **Output Voltage** | 12V |
| **Max Current** | 3A |

## Visuals
![Schematic Screenshot](images/schem.PNG)

To develop the buck converter schematic I frequently refered to the main operating ICs datasheet: [datasheet](https://www.ti.com/lit/ds/symlink/tps563300.pdf)

It provides formulas and specifications of the buck IC I used to develop this schematic. When selecting footprints for my components, I opted for 



![PCB Layout](images/pcb.PNG)

![PCB Layout 3D Render](images/pcbrender.PNG)
