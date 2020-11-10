# ZigStar

![](/files/images/3DDefault.PNG)

## Features:

- [TI CC2652P](https://www.ti.com/product/CC2652P) SimpleLink™ 2.4 GHz Multiprotocol Wireless MCU targeting Zigbee,Bluetooth 5.1 Low Energy,Thread + 19.5-dBm high-power amplifier
- Support RF-BM-2652P1 and RF-BM-2652P2 Module from RF-STAR,with CC2652P on board
- BSL,RST Buttons
- 2 LED for indication
- Compatible with [Z2M](https://www.zigbee2mqtt.io/)
- SMA antenna port for an external antenna
- Self-programming via the [cc2538-bsl](https://github.com/JelmerT/cc2538-bsl).No external programmer needed! Push BSL button to trigger this mode.
- Communicates via the common CH340E/CH340C USB-UART Bridge

Boards fit in [v.3 Stick Case](https://github.com/mercenaruss/zigbee-stick-v4/tree/main/files/STL) designed by [Jager](https://github.com/Jager-f)

## Revisions

There are 2 versions of stick:
- [CH340E version](https://github.com/mercenaruss/zigbee-stick-v4/blob/main/files/gerber/Gerber_Zigbee%20Stick%20v4.0%20-%20CH340E.zip), more compact,all elements on one side
- [CH340C version](https://github.com/mercenaruss/zigbee-stick-v4/blob/main/files/gerber/Gerber_Zigbee%20Stick%20v4.0%20-%20CH340C.zip), more easy to solder and includes ESD protection

Both versions use the same [3D Model Case](/files/STL)

### Bill of Materials:

EasyEDA Generated Boom,you can order on [LCSC](https://lcsc.com) directly - [BOOM](https://github.com/mercenaruss/zigbee-stick-v4/blob/main/files/BOM_Zigbee%20Stick%204.0%20CH340E-C.csv)

| Designator  | Name  | Footprint | Quantity |
| :------------|:---------------|:-----|:--------:|
| U1| RF-BM-2652P1/P2| | 1 |
| U2|AMS1117-3.3 |SOT-223| 1 |
| U3 | CH340E/CH340C|MSOP-10/SOP-16 |1|
| R1 | 10 kohm|SMD 0805 |1|
| R2,R3 | 1 kohm|SMD 0805 |2|
| R4 | 100 ohm|SMD 0805 |1|
| C1| 10uF|SMD_L3.2-W1.6|1|
| C2,C4| 100nF|SMD 0805|2|
| C3| 22uF|SMD_L3.2-W1.6|1|
| L1,L2| RED/GREEN LED|SMD 0805|2|
| SBL,RST|PUSH BUTTON |SMD_L3.9-W3.0-P4.45|2|
| USB| USB A MALE|USB-A-SMD_USB-A-1-TH|1|
| JTAG| PIN HEADER 5 PIN|2.54x5P|1|
| ANT| SMA ANTENNA PORT 1.6mm||1|
| D1| ESD USBLC6-2SC6|SOT-23-6|1|

**WARNING** D1 is used only for CH340C version stick.

Next items are not available on LCSC,you can get them on Aliexpress:
 - [RF-BM-2652P1/P2](https://letyshops.com/r/aliexpress-f6e2c6d280d5)
 - [RP-SMA Antenna PCB Connector 1.2/1.6mm](https://letyshops.com/r/aliexpress-e6704ce906c0)
 - [RP-SMA Antenna Female - Inner hole](https://letyshops.com/r/aliexpress-14123aa4ecca)
### Firmware

Module is compatible with [Z2M](https://www.zigbee2mqtt.io/)
Firmware [CC1352P_2](https://github.com/Koenkk/Z-Stack-firmware/blob/master/coordinator/Z-Stack_3.x.0/bin/CC1352P_2_20201026.zip)
TX power can be adjusted in zigbee2mqtt config section:

    experimental:
      transmit_power: 20

Available TX power values: -20,-18,-15,-12,-10,-9,-6,-5,-3,0,1..5,14..20

### Downloads
 - [Gerbers](https://github.com/mercenaruss/zigbee-stick-v4/tree/main/files/gerber)
 - [STL Case](https://github.com/mercenaruss/zigbee-stick-v4/tree/main/files/STL)
 - [Schematics (pdf), Revision 1](https://github.com/mercenaruss/zigbee-stick-v4/tree/main/files/schematics)
 - [LCSC Boom File](https://github.com/mercenaruss/zigbee-stick-v4/blob/main/files/BOM_Zigbee%20Stick%204.0%20CH340E-C.csv)

### Thanks go to:
- [@Jager](https://github.com/jager-f), [@Palco](https://github.com/palko), [@Egony](https://github.com/egony) for design review and comments
- Name Credit goes to [nurikk](https://github.com/nurikk), before board had a very boring name. Many thanks to him for a lot of work on Z2M and DIY Devices.

## Contact 
For general enquiries, suggestions and errors spotted: Email me at radu@grecu.info or write me directly in [Telegram](https://t.me/mercenaruss). Community contributions to this page are very much encouraged so you could also send pull requests with your proposed changes.

### Disclamer
We use aliexpress affiliate links for the components and the tools. Some Ad-blockers might block these links an thus they seem to appear broken. You will have to temporarely disable ad-blocker to open these links. 

### License
zigbee-stick-v4 is designed by DarthPCB's / Grecu Radu and licensed under the [GPL-3.0 License](https://opensource.org/licenses/GPL-3.0). 