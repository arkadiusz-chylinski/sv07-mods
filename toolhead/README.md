# Toolhead upgrade

## Motivation

The stock SV07+ toolhead had several limitations that made further upgrades difficult.

First, the original design was not compatible with the linear rail upgrade of the X axis. While adapter parts could be designed, the closed construction of the stock toolhead made deeper modifications impractical.

The toolhead was also highly integrated and did not allow easy replacement of key components such as the stepper motor, hotend or temperature sensor. This limited both repairability and future upgrades.

Another significant issue was the stock breakout board connected via a ribbon cable. This type of connection is mechanically fragile and prone to failure due to repeated bending during printer operation.

Finally, the stock toolhead was both relatively heavy and long, resulting in increased bending moments on the X carriage and reduced mechanical rigidity of the motion system.

For these reasons the original toolhead was replaced with a more modular design.

---

## Selected design

The upgraded printer uses the **XoL toolhead** developed by Armchair Heavy Industries.

Project repository:
https://github.com/Armchair-Heavy-Industries/Xol-Toolhead

The XoL design was selected primarily because of:

* compatibility with **BTT EBB36 toolboards**
* modular component layout
* improved cooling performance
* relatively low mass
* compatibility with several high-performance hotends

The design was slightly modified to properly mount a **Dragon HF hotend equipped with a melt zone extender**.

---

## Hardware configuration

The upgraded toolhead contains the following components:

**Hotend**

* Phaetus Dragon HF
* Melt Zone Extender (MZE)
* PT1000 temperature sensor

**Extruder**

* Wristwatch BMG extruder
  https://github.com/bythorsthunder/Voron_Mods/tree/main/Wristwatch_Extruder_BMG

**Cooling system**

* 2 × 4010 radial blowers for part cooling
* 1 × 2510 axial fan for hotend cooling

**Electronics**

* BTT EBB36 toolboard
* integrated ADXL345 accelerometer
* integrated MCU temperature sensor

**Bed probing**

* BTT Eddy Coil eddy-current probe

---

## Toolboard integration

The printer uses a **BTT EBB36 toolboard connected via USB**.

Most electrical connections were moved from the mainboard to the toolhead:

* extruder stepper driver
* hotend heater
* thermistor
* cooling fans
* probe
* accelerometer
* status LEDs

As a result, only two cables run to the toolhead:

* 24 V power supply
* USB communication cable

This significantly simplifies wiring and improves reliability compared to the stock ribbon cable solution.

To support the toolboard, a dedicated **24 V power line** was added directly from the power supply.

---

## Mechanical integration

The upgrade required several printed components defined by the XoL project.

Additionally, a few modifications were made:

* modified **hotend mounting geometry** to properly fit the Dragon HF with melt zone extender
* modified **belt attachment** to integrate with the upgraded motion system

These changes ensured proper alignment and compatibility with the linear rail X axis.

---

## Cooling system

Cooling performance was improved compared to the stock toolhead.

The upgraded configuration includes:

* **two 4010 blower fans** dedicated to part cooling
* **one 2510 axial fan** for hotend heatsink cooling

This configuration provides significantly higher airflow and improves print quality, particularly on overhangs and bridges.

---

## Sensors

Several sensors are integrated into the toolhead assembly:

* **PT1000 temperature sensor** for hotend temperature measurement
* **ADXL345 accelerometer** (on the EBB36 toolboard) used for resonance measurement and input shaping
* **MCU temperature sensor** on the toolboard for diagnostics
* **BTT Eddy Coil eddy-current probe** used for bed probing and Z homing

---

## Firmware integration

Integration of the new toolhead required firmware changes, including:

* configuration of the **EBB36 toolboard MCU**
* configuration of the **ADXL345 accelerometer**
* setup of the **eddy current probe**
* new extruder configuration
* updated fan and heater definitions

The corresponding configuration files are available in the **firmware** directory of this repository.

---

## Results

The upgraded toolhead significantly improved the mechanical and thermal performance of the printer.

Key improvements include:

* reduced toolhead mass
* reduced mechanical flex in the X carriage
* improved reliability of the extrusion system
* easier serviceability and component replacement
* significantly improved cooling performance
* higher achievable print speeds
* reduced print artifacts
* improved overhang performance

The higher thermal capacity of the Dragon HF hotend also enables higher flow rates, allowing faster printing without extrusion limitations.

---

## Media

<img width="377" height="493" alt="obraz" src="https://github.com/user-attachments/assets/05172a47-04ec-4092-ba2d-2f77b73b55e4" />

