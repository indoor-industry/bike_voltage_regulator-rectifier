Schematic, PCB design and 3D-printable case for a voltage regulator-rectifier designed for foot-crank motorbikes without batteries and a one wire accessories stator output.

For a bike with a battery, resistors R8 and R10 must be changed in accordance with the datasheet of the differential comparator (LM2903).
In the presence of a battery, the electrolytic capacitors can be removed for the sake of compactness. Additionally, a fifth input acting as an ignition turn-on switch should be added to avoid the regulator from slowly depleting the battery. All this is not necessary for batteryless bikes.

Output current may be limited by heat dissipation capabilities, the case is designed for the PCB to be immersed in resin or gel once inside it. Further testing is required.

The REF net is a stable 2.495V reference for the comparator. Right now the R8/R9 voltage divider scales down the output voltage at the other input of the comparator by 0.188. Such that it crosses the stable reference when the output voltage of the regulator is around   2.495V / 0.188 = 13.27V.
This implies that to change the regulation treshold one could, for example, replace R8 with a 24kOhm resistor and achieve a treshold of around 14.26V.

R10 adds hysteresis to the comparator to make it more stable and give a regulation band instead of a precise value. A higher R10 can give a more narrow band.

The two TO-220 packaged components have different nets connected to their tabs, if adding a heatsing to them, isolate the tabs from it and GND.

IMPORTANT: for single wire stators, the other wire is wired to the chassis, then one of the AC inputs to the regulator goes to the chassis as well and the the negative DC output should not be wired to the chassis to avoid losing full bridge rectification.
If the stator has 2-wires coming out of it and neither goes to the chassis, the negative DC output of the regulator can go to the chassis of the bike.
