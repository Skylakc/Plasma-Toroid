# Plasma Toroid DIY Instructions

This document was updated on Sep 14, 2024.

Author: *Diagon Alley Magic Shop*

All components used in this document can be found in the Aliexpress store ***Diagon Alley Magic Shop***. 

[Plasma Toroid Principle](https://www.youtube.com/watch?v=GbMAvn7nRWo)

[Finished product demo video 1](https://www.bilibili.com/video/BV1Lm411z7tf)

[Finished product demo video 2](https://www.bilibili.com/video/BV12f421o7rf) 

[LCEDA Open Source Platform](https://oshwhub.com/skylake/plasmatoroid-drive-circuit)

Plasma toroid open source technology telegram group:
https://t.me/+eRFEajIG6_RiMTY1

<img src=../imgs/imgs_24_7_22\cover.jpg width=80% />

## Copyright Notice©

This document is for personal learning and plasma toroid manufacturing only. Without the author's consent, no one may modify, republish, or distribute the content of this document. It is strictly prohibited to use this document for any commercial activities.

## Disclaimer
Before using this document to make a plasma toroid, please carefully read the following important safety warnings and disclaimers. Using this document means that you fully understand and agree to the following terms:
- Dangers of plasma toroids: The glass bottle will generate high temperatures when the plasma toroid is running, and there is a risk of low-temperature burns. It is never recommended to directly touch the running glass bottle with your hands to avoid burns.
- Magnetic field warning: The plasma toroid will generate a strong magnetic field during operation. For people wearing pacemakers and other medical devices, strong magnetic fields may affect the normal operation of the devices. We recommend that these users stay away from working plasma toroids to avoid potential health risks.
- High voltage risk: The drive circuit of the plasma toroid will generate high voltage during operation. High voltage poses a danger of electric shock or burns. Please do not touch any components, including the primary coil, while the circuit is working to avoid electric shock or burns.
- Component temperature: Please note that some components of the circuit may become very hot during operation, which may cause burns. When the device is running, especially after running for a long time, do not touch these components.
- Electromagnetic interference: The plasma toroid will emit electromagnetic waves around 10MHz when running. This band will not harm the human body, but it may interfere with some electronic devices operating in this band, such as touchpads and card readers. Please keep these devices away from the working drive circuit.

Using this document means that you understand and agree to bear the risks of use. The author is not responsible for any direct or indirect damages caused by not following the safety guidelines.

DIY with caution, safety first!

## Analysis of the Working Principle of Plasma Toroids

  - Glow discharge phenomenon: Under certain conditions, the gas will undergo glow discharge under the action of a strong electric field. In this process, the electrons of the gas molecules are stimulated and jump to higher energy level orbits. Since these electrons are unstable in the high-energy state, they will spontaneously fall back to the original low-energy orbit while releasing photons corresponding to the energy difference according to the law of conservation of energy. This phenomenon is called glow discharge and is applied to devices such as neon lights. The luminescence process of plasma toroids is similar to this.

  - Properties of plasma: In addition to the common solid, liquid, and gas states, plasma is another state of matter that exists in the universe, and flames are an example that contains plasma. When the gas is affected by high temperature, collisions between molecules will cause the outer electrons to escape their orbits, forming a plasma composed of charged particles. This charged ion mixture has electrical conductivity.
  - Generation of toroidal electromagnetic field: By passing a high-frequency alternating current through a toroidal coil, it can be derived from Maxwell's equations that the electric field distribution around it is toroidal. We use a self-excited Class E oscillator circuit to generate an alternating current with a frequency of about 10MHz.

  - Generation process of plasma toroid: In a spherical glass bottle filled with low-pressure xenon gas, the xenon gas is ionized under the action of a strong electric field to form a plasma. These conductive xenon gas plasmas form a stable toroidal structure under the influence of an external toroidal electric field. In the plasma, collisions of charged particles produce glow discharge, which emits a pale purple light, making the plasma toroid visible.

**When using and demonstrating the plasma toroid, please ensure that you understand its working principle and corresponding safety measures to ensure the safety of users.**


## Preparation of Materials

<img src=../imgs/imgs_24_4_13/compress/FullComponents.jpg width=88% /> 


- 80mm glass bottle filled with xenon gas (available in Aliexpress store **Diagon Alley Magic Shop**, larger glass balls cannot be installed in the bracket of this project)
- 1.2mm enameled wire - for winding coils
- Black ring inductor 10uH  
- Circuit board PCB (can be made using the files in the hardware folder)
- Coil support, including base plate and five support pieces
- Heatsink and fan
- MOSFET IRFP260N
- MOSFET heatsink silicone pad
- Potentiometer 1k  
- Resistor 1k * 3
- Resistor 1.8k, 3k
- SMD capacitor 100pf * 4
- SMD capacitor 4.7nF * 2  
- TVS 15V P6KE15CA
- Voltage regulator diode 9.1V
- Input filter capacitor Electrolytic capacitor 63V 220uf
- Toggle switch
- Green terminal block - for connecting coil
- White fan socket
- DC power interface 
- Light emitting diode
- Screws and nylon columns
- Piezoelectric ceramic removed from a lighter (used for initial ignition; this item is prohibited in air transport, so you may need to prepare it yourself, but the circuit can still be made without it)
- XL4015 current limiting module (this module is not required if you have an adjustable power supply)
- 24V power adapter (4A or above, or you can use an adjustable power supply)


## Production Tutorial 
Difficulty ★★★☆☆

### Tools
- Multimeter
- Soldering iron
- Solder wire
- Utility knife
- Diagonal pliers
- Hex screwdriver set 
- Tweezers (for soldering SMD capacitors)

<img src=../imgs/tools.jpg width=50% />

### Steps
- Prepare the five coil brackets, insert them into the base, heat up the soldering iron, and solder them in place with solder. Try to ensure that the brackets are perpendicular to the base plate. (The five coil bracket pieces need some force to fit in)

<img src=../imgs/imgs_24_4_13/compress/Coil1.jpg width=45% /> <img src=../imgs/imgs_24_4_13/compress/Coil2.jpg width=45% />

- Bend the enameled wire according to the diameter of the coil frame, do not straighten the enameled wire, keeping the enameled wire bent helps with threading, once straightened it cannot be threaded.

<img src=../imgs/imgs_24_4_13/compress/Coil3.jpg width=80% />

- Thread the enameled wire through the small holes from top to bottom, a total of four turns. The holes are relatively small, and threading can be done by pushing and pulling.

<img src=../imgs/imgs_24_4_13/compress/Coil4.jpg width=32% /> 
<img src=../imgs/imgs_24_4_13/compress/Coil5.jpg width=32% />
<img src=../imgs/imgs_24_4_13/compress/Coil6.jpg width=32% />


- Make a power supply with current limiting protection (this step can be skipped if you already have an adjustable power supply), prepare a 24V power supply and XL4015 current limiting module, cut the power cord, connect the module in series in the middle, turn the potentiometer for adjusting the output voltage of the XL4015 module clockwise to the end (there will be a clicking sound when turned to the end), and turn the current limiting potentiometer to the 3.5A position. The method to determine the position of the current limiting potentiometer is: set the multimeter to the 10A current range, insert the test leads into the 10A hole, touch the two test leads to the output (at this time, the output is shorted, there may be electric sparks but it's okay), the value displayed on the multimeter is the current limiting value of the current limiting module. Note that using a power supply without current limiting can easily burn out the MOSFET, you must connect the XL4015 module in series before connecting power. If you already have an adjustable power supply, you can skip this step. In the picture below, the potentiometer on the left side of the module is for adjusting the output voltage, and the potentiometer on the right is for adjusting the current limit. Turning clockwise increases the value.
- If you are using an adjustable power supply, please use the current limiting mode (CC), set the output voltage to 24V, and the current limit to 3.5A.

<img src=../imgs/imgs_24_3_1/XL4015.jpg width=64% />
<img src=../imgs/imgs_24_3_1/power_source.jpg width=32% />

- Insert components into the circuit board according to their type (do not install the MOSFET yet). For easy soldering, you can slightly bend the pins to fix them. Note that **the fan connector should be mounted on the back of the PCB, and a light-emitting diode and 1k resistor should also be soldered on the coil bracket PCB**.
The installation positions of each component are shown in the table below.

| Component Name         | Installation Position        |
|------------------------|------------------------------|
| 1k resistor * 3        | R1, R4, coil bracket PCB     |
| Light emitting diode   | coil bracket PCB             |
| 3k resistor            | R2                           |
| 1.8k resistor          | R3                           |
| Voltage regulator diode| D2                           |
| TVS (black)            | D1                           |
| Green terminal block   | P1                           |
| White terminal block   | Q3 (mounted on the back)     |
| 220uf electrolytic cap | C5                           |
| 100pf capacitor * 4    | C1, C2, C3, C4               |
| 4.7nf capacitor * 2    | C6, C7                       |
| 10uH inductor          | L1                           |
| IRFP260                | Q1 (do not install this yet) |
| Switch                 |                              |
| DC5525 black power jack|                              |
| B1K single potentiometer |                            |

- It is recommended to solder the shorter components first, then the taller components, such as soldering the SMD capacitors, resistors, voltage regulators, terminal blocks, etc. first, and finally soldering the electrolytic capacitors and switch. If you have no soldering experience, be sure to search for soldering tutorials on Bilibili to learn first. According to historical statistics, 60% of people who had problems after making it were due to poor contact between components and PCB caused by not mastering the correct soldering method.
  
  > Resistor identification 
  >  - 1k resistor has a brown line
  >	 - 1.8k resistor has a brown line and a gray line  
  >	 - 3k resistor has an orange line
  >	 If you really can't tell them apart, just measure with a multimeter ^_^

  > Capacitor identification
  >  - 4.7nF capacitors are relatively thinner
  >	 - 220pF/100pF capacitors are relatively thicker
  >  - For resonant capacitors, you can choose two 220pF or four 100pF

  > Diode direction identification
  >  - The black TVS is non-directional
  >	 - The red voltage regulator diode needs to be directional, the black line on the voltregulator diode should match the white line position on the PCB silkscreen.age 

  > Some friends may not know how to solder SMD components, you can search for SMD component soldering tutorials on Youtube to learn. Simply put, solder one side first to fix the SMD component, then solder the other side.
  >【How To Solder SMD Correctly - Part 1 /SMD Soldering Tutorial - Youtube】 https://www.youtube.com/watch?v=EW9Y8rDm4kE

  > Be sure to pay attention to the direction of the electrolytic capacitor, soldering it backwards may cause intense heating or even explosion. The longer leg of the electrolytic capacitor is the positive electrode, and the side with the stripe mark is the negative electrode. Please refer to the picture below to install the electrolytic capacitor correctly.

<img src=../imgs/imgs_24_7_22\assembled_front.jpg width=70% />

- When soldering, **be careful of the high temperature of the soldering iron to avoid burns.**

- After all components are soldered, cut off the pins. Please try to ensure that the solder joints are full and smooth, and start from the root when removing the pins.

<img src=../imgs/imgs_24_4_13/assemble_back.jpg width=70% />

- Screw 6mm copper columns (or 6mm nylon columns) into the screw holes around the heatsink.

<img src=../imgs/imgs_24_4_13/compress/Heatsink0.jpg width=60% />

- Install the MOSFET. Place the side of the MOSFET with text **facing up**, pad the other side with a silicone pad and fix it on the heatsink with screws, with the pins **facing downward**. At this time, the pins from left to right are G, D, and S poles respectively.

<img src=../imgs/imgs_24_4_13/compress/Heatsink1.jpg width=40% />

<img src=../imgs/imgs_24_4_13/compress/Heatsink2.jpg width=45% />

- Bend the pins and insert them into the PCB. **First align the holes of the PCB and the heatsink to ensure that the four screws can be tightened**, then solder the MOSFET.

<img src=../imgs/imgs_24_4_13/assemble_new.jpg width=60% />

- Fix the fan. The connection of all layers is shown in the figure below. The fan's airflow is blowing towards the heatsink (blowing upward).

<img src=../imgs/imgs_24_4_13/compress/Fan1.jpg width=30% />

<img src=../imgs/imgs_24_4_13/compress/Fan2.jpg width=30% />

<img src=../imgs/imgs_24_4_13/compress/Fan3.jpg width=30% />


- Use screws to mount the coil bracket to the top, with the two wires facing the green coil terminal block.

<img src=../imgs/imgs_24_4_13/compress/assemble3.jpg width=40% />
<img src=../imgs/imgs_24_4_13/compress/Assemble2.jpg width=48% />


- Cut the enameled wire appropriately so that it can be inserted into the terminal block.
- Use a utility knife to scrape off the enamel at the end of the wire to expose the copper core inside the enameled wire.
- **Note: Be sure to scrape the enamel at the end of the wire clean, otherwise poor contact may prevent it from working!**

<img src=../imgs/imgs_24_4_13/compress/Assemble1.jpg width=60% />



- Insert the two wires of the coil into pins 1 and 3 of the green terminal block (the middle hole is not used), and insert the fan power cord into the fan interface on the back of the PCB.

- After confirming that all parts are properly connected again, you can prepare to power on o(*￣▽￣*)ブ

- If you are using an adjustable power supply, please use the current limiting mode (CC), set the output voltage to 24V, and the current limit to 3.5A.
- Put on the bottle and make sure the potentiometer is at the maximum counterclockwise position.

- Before powering on, please carefully read the safety instructions:
  >  Stay away from the coil when the circuit is working, as the high temperature of the coil may cause burns.

  >  You can rotate the bottle, but the bottle will also heat up. Be careful and keep your hands away from the coil (at least 1cm away) when rotating the bottle.

  >	 You can turn the potentiometer while the circuit is working, but do not hold the bottle with one hand and touch the potentiometer on the circuit with the other hand, because the high-voltage static electricity on the bottle can damage the circuit.

  >	 The circuit will heat up. It is not recommended to run the circuit for a long time. It is recommended to work continuously for no more than two minutes.

  >	 After use, remember to turn off the switch and disconnect the power supply.

- After ensuring that you have read the safety instructions, plug in the power supply and turn on the switch. At this time, the fan should start spinning.

- Turn the potentiometer clockwise. When it is turned about halfway, the circuit will start working. When the circuit starts working, the LED next to the coil will light up. At this point, use a lighter to point at the bottle and click it to generate the toroid. If the lighter fails to generate the toroid, you can turn the potentiometer clockwise a little more and try again.
  
<img src=../imgs/imgs_24_3_1/excite.jpg width=40% />

<img src=../imgs/imgs_24_3_1/ring.jpg width=40% />

- Sometimes, your bottle may glow white without generating a toroid (as shown below). Adjusting the bottle position and re-igniting it a few times usually fixes it.

<img src=../imgs/imgs_24_3_1/white.jpg width=40% />


- After the toroid is generated, slightly turning the potentiometer will cause some changes in the shape of the toroid. If the toroid disappears, re-igniting it will generate it again.

<img src=../imgs/imgs_24_4_13/Xe2.jpg width=40% />

### Reference Circuit Diagram
Since the hardware of this project is still being updated, the circuit diagram is for reference only. The actual circuit should be based on the PCB.
<img src=../imgs/imgs_24_3_1/sch.jpg width=80% />


### FAQ
If you have any questions, join the telegram group：
https://t.me/+eRFEajIG6_RiMTY1.
<img src=../imgs\tg.jpg width=30% />
All project developers are in the group, and you can get answers at the fastest speed.(We try to answer all your questions within 24 hours.)

#### Acknowledgments: 
Tate McAluney