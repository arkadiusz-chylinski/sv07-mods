# Firmware

## Firmware architecture

The printer uses Klipper firmware with a host–MCU architecture.

The motion planning and high-level control are handled by a single-board computer running Armbian Linux, while the microcontroller is responsible for real-time step generation and hardware interfacing.

## Firmware update

The printer originally shipped with Klipper firmware already installed.
However, both the host operating system and the MCU firmware were significantly outdated.

To ensure compatibility with the latest Klipper features and configuration options, the system was updated as follows:

* the host operating system was reinstalled using a recent version of Armbian using KIAUH
* Klipper and its dependencies were updated on the host
* the MCU firmware was recompiled and reflashed using the Klipper build system

Communication between the host and the printer's mainboard MCU is performed over USB, following the standard Klipper host–MCU architecture.

The update was necessary to ensure compatibility with newer configuration syntax and features introduced in recent Klipper releases.

After installing the EBB36 toolboard the system architecture presents as follows

<img width="750" height="330" alt="obraz" src="https://github.com/user-attachments/assets/2631e064-6f66-45c9-8333-b8bbe2805f40" />

Configuration files used with the printer along with the comments are provided in this folder.


