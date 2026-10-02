# Open Tiny Biased Photodetector – Assembly Instructions
This document describes the assembly, mechanical installation, electrical inspection and initial operation of the **Open Tiny Biased Photodetector**.
The current PCB revision is **untested**. The instructions below describe the intended assembly and operating procedure. Verify the circuit and PCB before applying power.

---

## 1. Required Parts
### Electronics
* 1× PCB
* 1× photodiode:
  - Hamamatsu S5971
  - Hamamatsu S5972
  - Hamamatsu S5973
* 1× C1 – 100 nF
* 1× R1 – 1 kΩ
* 1× BNC female bulkhead connector
* 1× red 4 mm banana socket
* 1× black 4 mm banana socket
* 2× red wire
* 2× black wire

### Mechanical Parts
* 1× 3D-printed enclosure
* 2× M3 heat-set inserts
* 1× M4 heat-set insert
* 2× M3 × 5 mm screws

# 2. Required Tools
The following tools are recommended:
* Soldering iron
* Solder
* Side cutters
* Wire stripper
* Multimeter
* Suitable tool for installing heat-set inserts
* 3D printer for manufacturing the enclosure
* 9 V DC laboratory power supply or suitable 9 V supply
* Oscilloscope with 50 Ω input or suitable 50 Ω terminator for high-speed measurements

A microscope or magnifying glass can be useful for inspecting the PCB solder joints.

# 3. PCB Assembly
## 3.1 Install C1
Install the **100 nF capacitor** at position **C1**.
Verify that the component is correctly positioned on the PCB.

## 3.2 Install R1
Install the **1 kΩ resistor** at position **R1**.
Verify the resistor value before soldering.

## 3.3 Install the Photodiode
Install the selected photodiode at position **U1**.
Compatible photodiodes:
* Hamamatsu S5971
* Hamamatsu S5972
* Hamamatsu S5973
The three variants use the same PCB footprint.
**Pay particular attention to the photodiode orientation and polarity.**
Do not apply forward bias to the photodiode.
Because the photodiode is ESD-sensitive, appropriate ESD precautions should be used during assembly.

## 3.4 Install the BNC Connector
Install the **BNC female bulkhead connector**
* **BNC+ – red**
* **BNC- – black**
Ensure that the connector is mechanically secure and that the center signal and ground connections are correctly soldered.

## 3.5 Install the Banana Sockets
Install the two 4 mm banana sockets:
* **V+ – red**
* **V- – black**

### Supply
Keep the wires as short as practical and route them so that they cannot interfere with the enclosure or PCB.
Before powering the detector, verify the wiring with a multimeter.

# 5. Enclosure Preparation
The enclosure is provided as a 3D-printable STL file.
Print the enclosure according to the dimensions and orientation of the supplied STL file.
The enclosure contains mounting points for heat-set inserts.

## 5.1 M3 Inserts
Install the two **M3 inserts** into the designated mounting points.
Use a suitable soldering iron or heat-set insert tool.
Heat the insert sufficiently for it to enter the plastic without excessive force.
Allow the plastic to cool before assembling the PCB.

## 5.2 M4 Insert
Install the **M4 insert** into its designated mounting point on the bottom.
Verify that the insert is seated straight and does not protrude excessively from the enclosure.

# 6. PCB Installation
Place the assembled PCB into the enclosure.
Check the following:
* PCB is seated without mechanical stress.
* Wires or parts are not trapped or pinched.

Secure the PCB using the designated mounting points and **M3 × 5 mm screws**.
Do not overtighten the screws.

# 7. Final Mechanical Inspection
Before closing the enclosure, inspect the complete assembly.
Check:
* PCB orientation
* Connector alignment
* Screw installation
* Wire routing
* Photodiode position
* No loose parts inside the enclosure

# 8. Electrical Inspection Before Power-On
**Do not connect the 9 V supply yet.**

Perform the following checks:
1. Verify the photodiode orientation.
2. Verify the polarity of V+ and V-.
3. Check for solder bridges.
4. Check for visible soldering defects.
5. Check the supply wiring for accidental shorts.
6. Verify the ground connection.
7. Verify that the BNC connector is correctly connected.
8. Check that there is no unintended connection between the supply and ground.

Use a multimeter to check for unexpected low resistance between the positive supply and ground.

# 9. Initial Power-On
The detector is intended to be operated from a: **9 V DC supply**
For the initial power-on, a **current-limited laboratory power supply** is recommended.

Connect:
* **Red → +9 V**
* **Black → GND**

Verify the polarity before switching on the supply.

After powering the detector, check for:
* abnormal current consumption
* unexpected heating
* smoke
* unusual smell
* visible damage

If anything abnormal occurs, disconnect the power immediately and inspect the PCB.

# 10. Signal Connection
The BNC connector provides the detector output.
For high-speed operation, use: **Photodetector → 50 Ω coaxial cable → 50 Ω oscilloscope input**
A suitable external **50 Ω terminator** may also be used if the oscilloscope does not provide a selectable 50 Ω input.

## 10.1 50 Ω Termination
For the intended high-speed measurement configuration, a **50 Ω termination is required**.
The 50 Ω termination provides impedance matching between the detector output, coaxial cable and measurement input.
This minimizes signal reflections and ringing and provides the intended electrical measurement conditions.
Use a **50 Ω coaxial cable** and keep the cable as short as practical when high bandwidth is required.

## 10.2 High-Impedance Measurement
A 1 MΩ oscilloscope input can be used for low-frequency or DC measurements.
However, this is **not equivalent to the intended 50 Ω high-speed configuration**.
With a high-impedance input, the measured output voltage can be higher, while the bandwidth and transient response will differ.

# 11. Operating Precautions
### Reverse Bias
The photodiode is operated in **reverse bias**.
**Do not apply forward bias to the photodiode.**

### ESD
The photodiode and electronic circuitry are ESD-sensitive.
Use appropriate ESD precautions during:
* PCB assembly
* photodiode installation
* troubleshooting
* modification
* handling of the assembled detector

### Supply Voltage
The intended supply voltage is:
**9 V DC**
Do not exceed the specified supply voltage.
Always verify supply polarity before connecting the detector.

### Optical Safety
The detector does not generate optical radiation itself.
However, it may be used with lasers or other potentially hazardous optical sources.
Follow appropriate laser and optical safety procedures when using hazardous light sources.

# 12. Troubleshooting
## No Output Signal
Check:
1. 9 V supply voltage
2. Supply polarity
3. Ground connection
4. Photodiode orientation
5. BNC connection
6. Oscilloscope input configuration
7. 50 Ω termination
8. Optical alignment and illumination
For high-speed measurements, verify that the oscilloscope input is configured for **50 Ω**.

## Unexpectedly High Output Voltage
Check whether the oscilloscope is configured for **1 MΩ** instead of 50 Ω.
The measurement conditions are different and the output voltage can therefore be higher.

## Excessive Ringing
Check:
* 50 Ω termination
* coaxial cable impedance
* cable length
* oscilloscope input configuration
* connector quality

For high-speed operation, use a short **50 Ω coaxial connection** and a properly terminated 50 Ω input.

# 14. Related Project Files
The project repository contains the files required to reproduce and modify the detector.

Typical files include:
* **EasyEDA Pro project** – editable PCB and schematic design
* **Gerber files** – PCB manufacturing files
* **STEP file** – 3D CAD assembly
* **STL files** – 3D-printable mechanical parts
* **Images** – project and assembly documentation

Always use the files belonging to the same PCB revision when manufacturing the hardware.
