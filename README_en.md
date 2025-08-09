<p align="center">
   <img width="768" height="768" alt="Satellite" src="https://github.com/user-attachments/assets/36eb0eb9-4e3e-4b7e-b065-11105dfbef58" />
</p>

<img width="16" height="16" alt="image" src="https://github.com/user-attachments/assets/ed9d7c93-42b9-4f00-a5ab-595a9fa1a3b3" /> [Version française](README.md)

# 🛰️ GPS Satellite – ComputerCraft

## 📖 Overview
This script turns a computer or a turtle equipped with a wireless modem into a GPS beacon for the ComputerCraft location system.  
It allows other devices (turtles, computers, drones, etc.) to obtain their precise coordinates in the Minecraft world.  

This satellite is part of a GPS network consisting of at least 3 beacons (ideally 4 for better accuracy and reliability).

## ⚙️ How It Works
Continuously broadcasts its exact position using ComputerCraft’s GPS protocol.

Uses a wireless modem to communicate with other devices.

Supports both standard modems and Ender Modems for multi-dimensional networks.

Compatible with PixelLink when used in a monitored network.

## 🛠️ Installation

> [!TIP]
> Ideally, the satellite should be placed at layer 255 to maximize range.

1. Build the following structure (7x7x4):

<p align="center">
   <img width="1579" height="1217" alt="2025-08-04_18 44 52" src="https://github.com/user-attachments/assets/d51c7993-c5b9-48e0-a52d-b948f15ddc89" />
</p>

2. Attach the wireless modem on any side.  
3. Precisely note the coordinates (x, y, z) of your beacon.  
4. Download the satellite script: *startup.lua* available in this repository.  
5. Adjust the x, y, and z coordinates in *startup.lua* to match your computer’s position.  
6. Restart the computer.  
7. Repeat this process for the other 3 beacons.  

## 🛰️ Number and Placement of Satellites
Minimum: 3 beacons per satellite for basic functionality.  

Recommended: 4 beacons per satellite, preferably placed at high altitude (> y=100) to maximize range.

Modem ranges:

- Wireless modem: 64 blocks (range increases with altitude, up to 384 blocks at level 256)  
- Ender modem: unlimited, inter-dimensional  

## 🔍 Using with a Turtle
Example to get GPS coordinates:
```
local x, y, z = gps.locate()
if x then
    print("Current position: ", x, y, z)
else
    print("GPS signal unavailable")
end
