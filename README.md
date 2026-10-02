# Open Tiny Biased Photodetector

Open Tiny Biased Photodetector is a compact open-source hardware project for optical signal detection in lab and embedded setups.  
It combines a Hamamatsu photodiode, a custom-designed PCB, and a 3D-printed enclosure in a small, practical form factor.

> This project is an independent design inspired by the general concept of commercial amplified photodetectors.  
> It is not affiliated with, endorsed by, or a copy of any commercial product.

## Key Features

- Compact, open hardware photodetector architecture
- Reverse-biased photodiode front end for improved response
- Custom analog PCB for signal conditioning
- 3D-printable enclosure for mechanical protection and mounting
- Suitable as a baseline platform for custom optical instrumentation

## Hardware Architecture

The detector is built around:

1. **Photodiode stage** – Hamamatsu photodiode operated with bias.
2. **Analog front end** – transimpedance/conditioning circuitry on a custom PCB.
3. **Power and output interface** – connectorized power input and analog signal output.
4. **Mechanical package** – compact 3D-printed enclosure that aligns and protects the assembly.

## Build Overview

1. Fabricate or order the PCB from the design files.
2. Source all electronic components (including the Hamamatsu photodiode).
3. Assemble and solder the PCB.
4. Print the enclosure parts.
5. Install PCB and photodiode into the enclosure.
6. Power the unit and verify baseline electrical behavior before optical testing.

## Required Components

- Hamamatsu photodiode (selected model)
- PCB (from project design files)
- Analog front-end ICs and passives (op-amp(s), resistors, capacitors, bias network)
- Connectors/cabling for power and output
- Fasteners/enclosure hardware
- 3D-printed enclosure parts

## PCB and Enclosure Files

- **PCB design files**: custom board sources and manufacturing outputs
- **Enclosure files**: 3D-printable CAD/export files for the case

If you are publishing this project structure, place these files in clearly named hardware folders (for example, `hardware/pcb/` and `hardware/enclosure/`).

## Testing and Measurement Results

Validate each build with:

- Power rail and bias checks (no optical input)
- Dark/noise baseline measurement
- Response measurement using a controlled light source
- Bandwidth/rise-time checks for your target application

Document measured sensitivity, noise floor, and frequency response for your specific component selections and assembly quality.

## License

This project is open source under the terms of the [LICENSE](LICENSE) file.
