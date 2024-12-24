# WLED Pixie - Rev A
 A Small Form factor ESP32-C3 with an integrated battery charger & 5V boost, running WLED 
 
![Demo](/Pics/6-Test_Setup.JPG)
*Pixie Board running WLED w/WS2812C Fairy LEDs*

### Description

I've always been fascinated by LEDs. Learning how to control them was one of the reasons I became an Electrical Engineer. So when a friend introduced me to WLED and showed how easy it was to get a project running, I was amazed.

For as long as I can remember, personal electronics projects have often been limited by the available power sources. AA batteries are bulky, and lithium-ion batteries, while effective, are expensive and come with shipping restrictions. However, with the rise of disposable vaporizers, I saw an opportunity: repurposing their small but powerful lithium-ion batteries for personal projects.

My goal for this project was to design a WLED-compatible board in the form factor of an common 801640 LiPo disposable vape battery. This would allow the PCB to stack neatly on top of the battery and fit into a simple 3D-printed enclosure. I used the ESP32-C3 module with an IPEX-3 connector to minimize the PCB footprint and to enable the use of an external flex antenna for improved Wi-Fi range. To support two outputs for WS2812 Neopixels, I included two 3V3-to-5V level shifters.

For the PMIC (Power Management IC), I got creative and chose the IP5305T, originally designed for inexpensive 5V power banks. This single SOIC-8 package handles lithium battery charging, 5V boosting, and includes a power path for USB input. It even integrates a push-button controller, making it an ideal all-in-one solution. To power the ESP32-C3, I used an LDO to provide a stable 3V3 supply.
The final design offers a compact WLED board that can be powered either via a 5V USB connection or recycled 801640 vape batteries. The two LED outputs can be toggled on and off using an assigned GPIO button or the WLED app. Additionally, the PMIC includes an on/off button for easy shutdown, perfect for power-saving applications.

This project combines my love for LEDs with my commitment to sustainability, offering a practical way to breathe new life into disposable vape batteries while creating something fun and functional.

---

## Table of Contents
- [Features](#features)
- [Schematic](#Schematic)
- [WLED](#WLED)
- [Bringup](#Bringup)


---

## Schematic
The latest schematic can be found here
[Schematic](/WLED_Pixie_Rev_A/Project%20Outputs%20for%20WLED_Pixie_Rev_A/PDF/WLED_Pixie_Rev_A-2024-10-12.PDF)

---

## WLED
The project runs WLED firmware
WLED can be installed on this board by using the web installer here: 
https://install.wled.me/

---

## Bringup
The boards were manufactured by JLCPCB. Due to the pitch of the ESP32 module the project required xray instection service.


![DFM Xrays](/Pics/7-WLED_Pixie_RevA_Xray.jpg)
*The xrays view of the board was kinda interesting to see*

The boards were manufactured in a 1-up configuration and returned with the tabs intact

![Panel View](/Pics/1-panel_view.jpeg)
*1-up PCBs recieved from JLCPCB*

The MCO was designed to be the same size as a standard disposable vape battery

![Top_Stacked](/Pics/3-top_stacked.jpeg)
*Pixie board stacked*

![Side-by-side](/Pics/4-botton-sidebyside.jpeg)
*Pixie board next to battery*

![Module-with-antenna](/Pics/5-module-antenna.jpeg)
*Pixie board w/antenna*

![Module-with-antenna](/Pics/8-enclosure.jpg)
*Packaged in an enclousure*


---

