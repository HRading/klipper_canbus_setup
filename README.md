# voron_canbus_setup

## Introduction
This is my guide for how to setup Klipper on my Voron 2.4 350 to use canbus It focuses on Octopus Pro based on a F429 chip, and a Mellow Fly SB2040 EBB.
Its main purpose is for me to remebmer what I did, if i ever need to reinstall.

The content of this guide is based on information gathered from different sources, promarily these two:
- Akhamars great guide:  https://github.com/akhamar/voron_canbus_octopus_sb2040
- TeamFDM guide: [How to Use CAN Toolhead Boards Connected Directly to Octopus / Octopus Pro on CanBoot](https://www.teamfdm.com/forums/topic/672-how-to-use-can-toolhead-boards-connected-directly-to-octopus-octopus-pro-on-canboot/)

## used hardware
- Raspberry Pi 4 with 32GB SD card.
- Bigtreetech Octopus Pro v1.0 with F429 chip
- Mellow Fly-SB2040 v1 board for StealthBurner

# Prerequisites
Download and install the following tools on PC
- [Raspberry Imager](https://www.raspberrypi.com/software/)
- [STM32CubeProgrammer](https://www.st.com/en/development-tools/stm32cubeprog.html)
- [PuTTY](https://www.putty.org/)

# Installation

## Raspberry OS
Start the Raspberry Imager on PC and insert SD card in reader

1. Click Choose OS and Select the "Raspberry Pi OS Lite (64-bit)" Image found under the Rasbberry PiOS (other) menu.
2. Change Settings by clicking the gear icon
   1. Set hostname to `voron24`
   2. Enable SSH, Use password authentication
   3. Set username and password
      1. leave username as `pi`
      2. set password
   4. Configure wireless LAN
      1. Set SSID
      2. Set password
      3. Set Wireless LAN country to `DK`
   5. Set locale settings
      1. Time zone: `Europe/Copenhagen`
      2. Keyboard layout: `dk`
3. Choose storage and Write.

Insert the SD card in the Pi and power up

## Install Klipper
Connect to the Pi using SSH (I use PuTTY for this)
Login as `pi`

Install Git and KIAUH (Klipper Installation And Update Helper)
```	
sudo apt-get install git -y
cd ~
git clone https://github.com/th33xitus/kiauh.git
./kiauh/kiauh.sh
```

Use KIAUH interface to install the following components (click 1 for install and follow instructions)
1. Klipper
2. Moonraker
3. Fluidd





