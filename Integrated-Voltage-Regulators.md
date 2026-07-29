## Overview

Large AI and datacentre chips require hundreds of watts but operate at very low (<2 V<sub>DC</sub>) core voltages, consequently current draw is often over 100 A.

## Existing Voltage Regulation Methods

Providing these high currents is typically achieved using multiple banks of parallelised switching regulators. For example, first stepping down from 48 V<sub>DC</sub> to 5 V<sub>DC</sub>, then from 5 V<sub>DC</sub> to the desired chip voltage.<br>
This two-tier approach allows each stage to operate more efficiently than a single regulator whilst also making the power rail powering the target chip more robust to sudden changes in the supply voltage.

These regulators are often located on a separate section of a PCB, relatively far from the compute chips they power.<br>
The long PCB traces connecting them lead to higher I<sup>2</sup>R losses, which are becoming a serious inefficiency problem, with 10-20% being lost just in the PCB traces between the regulators and the chips.

## Integrated Voltage Regulators

Some chips have started to incorporate Integrated Voltage Regulators (IVRs) within the package to reduce the distance between the regulator and chip, thus reducing the I<sup>2</sup>R losses.<br>
This in turn creates heat dissipation challenges where the regulator itself can heat up the target chip and necessitates additional cooling requirements, for example on-chip active cooling or larger substrates / packages / interposers.

## Current Limitations

The main design issue with these switched-mode regulators is the need for physically large inductors, limiting their miniaturization.<br>
Manufacturers are currently developing different materials to make smaller inductors capable of the inductance needed to power these large chips, most of which is proprietary.

## Notable Companies in IVR Design and Manufacture
- Ferric
  - High-end designs tailored to large scale compute and AI, offering current densities up to 4.5 A/mm<sup>2</sup>.
- Empower Semi 
  - Offers a variety of medium and high-end designs for both low power (<50 W) and high power (>500 W) applications with current densities >1 A/mm<sup>2</sup>.
