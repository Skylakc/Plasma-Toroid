# Plasma Toroid Making Tutorial

Last updated on March 1st, 2024  

Author: *Diagon Alley Magic Shop*
All parts used in this tutorial can be found at online shop ***Diagon Alley Magic Shop***

[Demonstration video](https://www.bilibili.com/video/BV1YQ4y157gs)

[JLC open source platform](https://oshwhub.com/skylake/plasmatoroid-drive-circuit) 

QQ Group for plasma toroid open source community: 736688139


<img src=../imgs/cover.jpg width=100% />

## Copyright Notice ©

This tutorial is for personal learning and making plasma toroids only. No one is allowed to modify, republish or distribute the content without the author's consent. Any commercial use of this tutorial is strictly prohibited.

## Disclaimer
Please read the following important safety warnings and disclaimers before using this tutorial to make a plasma toroid. By using this tutorial, you agree that you have fully understood and accepted the following terms:

- Plasma toroid hazards: The glass bottle of a running plasma toroid will get very hot, posing risks of low temperature burns. Never touch the hot glass bottle directly during operation to avoid burns.

- Magnetic field warning: Strong magnetic fields are generated when the plasma toroid is running. For people with pacemakers or other medical devices, the strong magnetic field may affect normal operation of the devices. We recommend these users stay away from a running plasma toroid to avoid potential health risks. 

- High voltage risks: The drive circuit of the plasma toroid operates at high voltages. There are risks of electric shocks or burns at high voltages. Do not touch any components including the primary coil when the circuit is powered on to avoid shocks or burns.

- Component temperature: Note that some components in the circuit can get very hot during operation, which may cause scalding. Do not touch these components when the device is running, especially after long periods of operation.

- Electromagnetic interference: The plasma toroid emits electromagnetic waves around 10MHz when running. This frequency is harmless to humans, but may interfere with some electronic devices operating at this frequency band, such as touchpads and card readers. Please keep these devices away from the running drive circuit.  

By using this tutorial, you agree that you understand and accept the risks, and the author is not responsible for any direct or indirect damage resulting from failure to follow the safety guidelines.  

DIY with caution, safety first!

## How A Plasma Toroid Works

- Glow discharge phenomenon: Under certain conditions, gas glows and discharges in strong electric fields. In this process, the electrons of gas molecules get excited and transition to higher energy levels. Since these electrons at high energy levels are not stable, they will spontaneously fall back to their original low energy levels, emitting photons with energy equal to the energy gap in this process. This phenomenon is called glow discharge, and it is used in neon lights and other devices. The light emission process of a plasma toroid is similar.

- Properties of plasma: Besides the common solid, liquid and gas states, plasma is another state of matter that exists in the universe. Flames contain plasma. When gas gets heated to high temperatures, collisions between molecules will strip electrons from their orbits, forming a plasma that consists of charged particles. This mixture of charged ions and electrons is electrically conductive. 

- Generation of toroidal electromagnetic field: By passing high-frequency alternating currents through a toroidal coil, a toroidal electric field can be generated around it according to Maxwell's equations. We use a self-oscillating Class E oscillator circuit to generate AC currents around 10MHz.

- Plasma toroid formation: In a spherical glass bottle filled with low-pressure xenon gas, the xenon gas gets ionized and forms a plasma in the strong electric field. These conductive xenon plasma ions and electrons form a stable toroidal structure under the influence of the applied toroidal electric field. Collisions within the plasma result in glow discharge and emit a pale purple light, making the plasma toroid visible.

**Please make sure you understand the working principles and associated safety measures before using or demonstrating a plasma toroid, to ensure safety.**

## List of Materials Needed

<img src=../imgs/all_components.jpg width=80% />

- 80mm glass bottle filled with xenon gas (can be found by searching "plasma toroid" on Taobao, larger glass balls cannot fit in this project's coil stand)
- 1.2mm enameled wire - for winding the coil  
- 10uH yellow toroidal inductor
- PCB board (perfboard or Manhattan style can work as substitutes)
- Coil stand, including base plate and 5 stand pieces
- Heatsink and fan
- MOSFET IRFP260N
- Thermal silicone pad for MOSFET
- 1k potentiometer
- 1k resistor x 2
- 2.7k, 5.6k resistors
- 30pf ceramic capacitors x 4  
- 4.7nF SMD capacitors x 2
- 15V TVS diode P6KE15CA 
- 9.1V Zener diode
- 63V 220uf electrolytic input filter capacitors x 2
- Toggle switch
- Green screw terminals - for connecting the coil
- White fan power socket
- DC5.5 power jack
- Screws and nylon spacers
- Piezo igniter harvested from a lighter (for initial ignition)
- XL4015 current limiting module (can be skipped if using an adjustable power supply)  
- 24v power adapter (>=4A, or use an adjustable power supply)

## Making Steps
Difficulty: ★★★☆☆   

### Tools Needed
- Multimeter
- Soldering iron  
- Solder wire
- Cutter
- Pliers
- Hex screwdriver set

<img src=../imgs/tools.jpg width=40% />

### Steps

- Prepare the 5 coil stand pieces, insert them into the base plate, heat up the soldering iron and solder them to fix in place. Try to keep the stands perpendicular to the base plate as much as possible. (It takes some force to insert the 5 stand pieces.)

<img src=../imgs/imgs_24_3_1/Coil0.jpg width=45% />
<img src=../imgs/imgs_24_3_1/Coil1.jpg width=45% />

- Bend the enameled wire following the diameter of the coil stands, do not straighten the wire, keeping it bent helps threading it through the holes.  

<img src=../imgs/imgs_24_3_1/Coil5.jpg width=40% />

- Thread the enameled wire through the holes from top to bottom, 3 turns in total. The holes are small, push and pull to get it through.

<img src=../imgs/imgs_24_3_1/Coil2.jpg width=30% />
<img src=../imgs/imgs_24_3_1/Coil3.jpg width=30% /> 
<img src=../imgs/imgs_24_3_1/Coil4.jpg width=30% />

- Make a power supply with current limiting protection (skip if you already have an adjustable power supply). Prepare a 24V power adapter and XL4015 current limiting module, cut open the power adapter cable, connect the module in series, turn the voltage adjust potentiometer on the XL4015 module fully clockwise, and turn the current limit potentiometer to 3.5A. Determine this position by: set the multimeter to 10A current range, short the output pins with the probe (this effectively shorts the output), the displayed value is the current limit of the module. Note, using a power supply without current limiting can easily burn the MOSFETs, you can skip this step if you already have an adjustable power supply. In the picture below, the potentiometer on the left adjusts output voltage, and the one on the right adjusts current limit.
- If using an adjustable power supply, use current limiting mode (CC), set output to 24V, with 3.5A current limit.

<img src=../imgs/imgs_24_3_1/XL4015.jpg width=60% />
<img src=../imgs/imgs_24_3_1/power_source.jpg width=32% />

- Insert all components into the PCB board according to their markings (do not install the MOSFETs yet), bend the leads to temporarily hold them in place to make soldering easier. Note, the fan power socket should be installed on the back of the PCB. 
- It is recommended to first solder shorter components, then taller ones. For example, solder resistors, zener diodes, power sockets first, capacitors and switches last.

> Resistor identification:  
> - The slightly larger ones are 1k resistors.
> - Ones with green and blue bands are 5.6k resistors. 
> - Ones with red and purple bands are 2.7k resistors.

<img src=../imgs/imgs_24_3_1/Solder0.jpg width=40% />

- Be very careful of the high temperature of the soldering iron when soldering, **watch out for burns**.

- After all components are soldered, clip the leads. Try to keep the solder joints full and rounded, start clipping from the base when removing leads.

<img src=../imgs/imgs_24_3_1/Solder1.jpg width=40% />

- Screw copper spacers into the 4 holes around the heatsink.

<img src=../imgs/imgs_24_3_1/heatsink0.jpg width=40% />

- Install the MOSFET. Place the MOSFET with the writing facing **up**, put a silicone pad on the underside and screw it onto the heatsink, with the **leads facing down**. The left, center and right leads are drain, gate and source respectively.

<img src=../imgs/imgs_24_3_1/heatsink1.jpg width=40% /> 

- Bend the MOSFET leads and insert into the PCB, **first align the PCB and heatsink holes and screw in place before soldering**, then solder the MOSFET. 

<img src=../imgs/imgs_24_3_1/assemble0.jpg width=40% />

- Mount the fan, the connection order of all layers is shown below, fan should blow air towards the heatsink (upwards).

<img src=../imgs/imgs_24_3_1/fan0.jpg width=30% />
<img src=../imgs/imgs_24_3_1/fan1.jpg width=30% />
<img src=../imgs/imgs_24_3_1/fan2.jpg width=30% />

- Use screws to mount the coil stand onto the top, with the two coil wires going into the green screw terminals.

<img src=../imgs/imgs_24_3_1/assemble1.jpg width=40% />

- Cut the enameled wires to appropriate length to plug into the terminals.   
- Scrape off the enamel coating at the ends with a knife to expose the copper.
- **Make sure to completely remove the enamel, otherwise it can cause bad contact and prevent operation!** 

<img src=../imgs/imgs_24_3_1/Coil6.jpg width=40% />

- Insert the two coil wires into terminals 1 and 3 of the green screw terminals (skip the middle hole), plug the fan power wire into the fan socket at the back of the PCB.

- Double check all connections before powering up o(* ̄▽ ̄*)ブ

- For adjustable power supply, use current limiting mode (CC), set output to 24V, with 3.5A current limit.  
- Place on the glass bottle with the potentiometer turned fully counter-clockwise.

- Carefully read the safety guidelines before powering on:
  > Stay away from the coil when circuit is running, the high temperature can cause burns.   

  > The bottle can be rotated, but it also gets hot. Be careful, keep hands at least 1cm away from coil when rotating bottle.

  > Do not hold bottle in one hand and turn potentiometer on circuit with the other, as high voltage static on bottle can damage circuit.

  > Circuit will get hot, do not run for more than 2 minutes continuously.   

  > Turn off switch and disconnect power after use.

- After reading safety guidelines, plug in power adapter and flip power switch, fan should start spinning. 

- Slowly turn potentiometer clockwise, circuit should start working around 80% into the rotation range. Use piezo igniter to ignite a ring when it starts working. If unable to ignite, turn potentiometer slightly more clockwise and try again.

<img src=../imgs/imgs_24_3_1/excite.jpg width=40% />
<img src=../imgs/imgs_24_3_1/ring.jpg width=40% />

- Sometimes the bottle glows white without forming a ring (shown below). Adjust bottle position and ignite again, it should correct after a few attempts.  

<img src=../imgs/imgs_24_3_1/white.jpg width=40% />

- After a ring forms, slightly adjusting the potentiometer changes the shape. If ring disappears, simply ignite again to bring it back.

<img src=../imgs/imgs_24_3_1/ring1.jpg width=40% />

### Circuit Schematic
Since this project's hardware is still evolving, schematic is for reference only, actual circuit should follow the PCB.
<img src=../imgs/imgs_24_3_1/sch.jpg width=80% />


### FAQ
For any other questions, join QQ Group 736688139 where all project developers are active and can provide the quickest answers.

Credits: Tate McAluney