<div align="center">
<h1>
<a href="https://github.com/YuaXan/BM3451XXDC-T28A-Board">BM3451XXDC-T28A-Board</a></h1>

**Rechargeable battery protection board based on BM3451 IC**
______________________________________________________________________

[![KiCad Version: 7.0.6](https://img.shields.io/badge/KiCad-7.0.6%7C7.0.10%7Cnightly--7.99%7Cnightly--8.0.0-blue?logo=kicad)](https://www.kicad.org/)
![Design Rule Check: passing](https://img.shields.io/badge/DRC-passing-brightgreen.svg)
![GitHub Release](https://img.shields.io/github/v/release/YuaXan/BM3451XXDC-T28A-Board)
![GitHub Downloads (all assets, all releases)](https://img.shields.io/github/downloads/YuaXan/BM3451XXDC-T28A-Board/total)
![GitHub contributors](https://img.shields.io/github/contributors/YuaXan/BM3451XXDC-T28A-Board)
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-brightgreen.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-brightgreen.svg)](https://creativecommons.org/licenses/by/4.0/)
</div>

## Product Introduction
The board uses `BM3451XXDC-T28A` to protect 3/4/5 cells rechargeable battery pack. the IC works constantly to monitor each cell’s voltage, the current of charge or discharge, and the temperature of the environment to provide overcharge, over-discharge, discharge overcurrent, short circuit, charge overcurrent, and over-temperature protections, etc. Besides, it also can change the protection delay time of overcharge, over-discharge, and discharge overcurrent by setting the external capacitors.
![Charge or discharge mosfets](/png/BM3451XXDC-T28A-Board.png "Charge or discharge mosfets")

## Application Scenarios
1. Power tools
2. Electric bicycle
3. UPS applications
4. etc.

## Product Description
The board's power supply voltage range is 5-30V, charge or discharge current MAX is 30A. 

The four MOSFET `Q8`, `Q9`, `Q10`, `Q11` and tow jepsun current resistor `RSENSE1` and `RSENSE2` can be replaced to achieve higher current output. 
![Charge or discharge mosfets 3D](/png/charge-or-discharge-mosfets-3D.png "Charge or discharge mosfets 3D")

![Charge or discharge mosfets](/png/charge-or-discharge-mosfets.png "Charge or discharge mosfets")

![Jepsun current resistors 3D](/png/jepsun-current-resistors-3D.png "Jepsun current resistors 3D")

![Jepsun current resistors](/png/jepsun-current-resistors.png "Jepsun current resistors")

---

Select the number of cells based on whether `RSET1` and `RSET2` are mounted with 0Ω resistors.

When `RSET1` and `RSET2` all not mounting with 0Ω resistors leads to the `SET` pin in a floating state, and the board can connect 5 cells. 
When `RSET1` is mounting with resistors, `RSET2` is not mounting with resistors, and short circuits `B1` and `B-`, the board can connect 4 cells.
When `RSET1` is not mounting with resistors, and `RSET2` is mounting with resistors, and short circuits `B2`, `B1`, and `B-`, the board can connect 3 cells.

**[Warning]: Not `RSET1` and `RSET2` all to mounting with 0Ω resistors, this behavior will cause a short circuit**

![B2/B1/B- Conncets](/png/B2-B1-B--conncets.png "B2/B1/B- Conncets")

![SET PIN and resistors 3D](/png/SET-PIN-and-resistors-3D.png "SET PIN and resistors 3D")

![SET PIN and resistors](/png/SET-PIN-and-resistors.png "SET PIN and resistors")

![3/4/5 cells application selection](/png/3-4-5-cells-application-selection.png "3/4/5 cells application selection")

---

 There are five LEDs to monitor the balancing status of the cells. When one of the LEDs is lit, it means that the corresponding cell is starting to balance. 
 
 `LED1`, `LED2`, `LED3`, `LED4`, and `LED5` correspond to `B1`, `B2`, `B3`, `B4`, and `B5` respectively:
![balance led 3D](/png/balance-led-3D.png "balance led 3D")

 ---
 
 At the same time, the `DO` and `CO` pins correspond to `DO_LED1` and `CO_LED1` respectively. This allows you to check the discharge and charge status. 
 
![CO DO led 3D](/png/CO-DO-led-3D.png "CO DO led 3D")

 ---
 
 Safe and reliable by providing control discharge overcurrent release terminals with optical coupler.

Control of `OCCT` pin is via `XH P2.5mm 3pin` terminal.

**[Warning]: The "OCCT" pin has not been tested. Usage instructions are not provided in the datasheet. Usage instructions will be provided after board testing.**

![OCCT 3D](/png/OCCT-3D.png "OCCT 3D")


## Instruction Manual
The board connection diagram is shown in the image.
![BM3451XXDC-T28A-Board Connection Diagram](/png/BM3451XXDC-T28A-Board-Connection-Diagram.png "BM3451XXDC-T28A-Board Connection Diagram")

## TODO
- [ ] The board is not manufactured.
- [ ] The board is not testing.
- [ ] How the `OCCT` are work.
- [ ] The donation channel is not currently open.

## Contributions
Every contribution to this repository is highly appreciated! If you spot any bug or problem, open a issue or pull request so that it can be rectified for everyone.

For feature requests: Please open a issue and I'll add the feature in a future release once I get some time in my hands.

## Donors
The donation channel is not currently open, so stay tuned.

## License
For e-enthusiasts or geeks, follow the [CC-BY-NC-SA 4.0](/LICENSE.txt) license. For contributors and donors you can follow the [CC-BY 4.0](/LICENSE-CC-BY-4.0.txt) license, which means that commercial use is supported and distributed freely.

