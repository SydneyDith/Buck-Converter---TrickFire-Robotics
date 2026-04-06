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

It provides formulas and specifications of the buck IC I used to develop this schematic. When selecting footprints for my components, I opted for the 0603 package when possible. For the resistors and capacitors, selecting the handsolder footprint made handsoldering my PCB much easier later on. In my first iteration of schematic design, I made the mistake of choosing an inductor footprint that was only tolerated for a current of ~250mA. When double checking my work, however, I found this mistake and quickly sought another component that could support my desired specifications of 3A. Luckily this fix was easy at this stage in the project, but if left overlooked, my final design wouldn't have worked as intended and costed the project time and money to fix. I quickly found a replacement and ensured my other components were rated for this current and voltage.

![PCB Layout Prototype V1](images/pcbv1.PNG)

Based on the [datasheet](https://www.ti.com/lit/ds/symlink/tps563300.pdf), the following layout/placement strategies were employed:

*  Placed IC, inductor, and caps on the same side of the board.
*  Positioned input/output caps as close to the IC as possible.
*  Placed 0.1µF decoupling caps directly next to the power pins.
*  Kept the switching trace small and current loop small to minimize noise.
*  Positioned the FB divider near the pin and away from noisy power traces.

In my initial design, 
![PCB Layout Prototype V1](images/pcb.PNG)

![PCB Layout 3D Render](images/pcbrender.PNG)
