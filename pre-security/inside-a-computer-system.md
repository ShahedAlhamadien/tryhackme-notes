# Inside a Computer System

**Path:** Pre Security
**Section:** Computer Fundamentals
**Date:** [10/26/2026]
**Room Link:** [Inside a Computer System](https://tryhackme.com/room/insideacomputer)

## Overview

A computer is built from separate parts that each do one job and connect to the motherboard or the chassis. In this room I played a forensics investigator who had to rebuild a workstation from a breach scene. Only 7 parts belong to the machine and the rest are impostors.

## Key Terms

- **CPU** = the brain of the computer. It runs programs and instructions. Goes in the CPU socket.
- **RAM** = temporary fast memory for data currently in use. It is erased when the power is off. Goes in the DIMM slots.
- **GPU** = creates everything shown on the screen (images, video, 3D). Goes in the PCIe x16 slot.
- **SSD** = permanent storage with no moving parts, fast and silent. Goes in the M.2 slot.
- **HDD** = permanent storage with spinning disks and moving parts. Sits in a drive bay.
- **PSU** = converts wall electricity into the right voltage for each part. Sits at the edge of the chassis.
- **Network Adapter** = lets the computer send and receive data over a network. Sits inside the chassis near the rear.
- **I/O Panel** = the external ports (USB, HDMI, audio, Ethernet). Sits at the rear opening of the chassis.

## Attack Steps (Investigation Steps)

1. Read the case briefing: rebuild the machine, boot it, find the evidence file, and email it to the senior analyst.
2. Read the evidence tags and the Parts & Function notes to learn what each part does and where it belongs.
3. Picked the 7 parts that belong: CPU, RAM, GPU, SSD, PSU, Network Adapter, I/O Panel.
4. Rejected the impostors: Laptop GPU, Laptop Power Charger, Wi-Fi Dongle, and HDD.
5. Assembled the machine and booted it.
6. Found the evidence file and emailed the flag to the senior analyst.

## Why the Impostors Were Wrong

| Impostor | Reason |
|---|---|
| Laptop GPU | Made for laptops, not a desktop PCIe x16 slot |
| Laptop Power Charger | External charger, not an internal PSU |
| Wi-Fi Dongle | Plugs into a USB port outside, but the adapter must be internal |
| HDD | The machine uses an SSD (M.2 slot) for storage |

## Final Note

Every part is chosen by its function and position, so reading the details carefully matters more than guessing. For security this is useful because RAM loses its data when powered off (investigators capture memory first), SSD and HDD are recovered differently, and every external port on the I/O panel is a possible entry point for an attack.
