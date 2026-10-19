# Bill of Materials (BOM)

Everything you need to build **one** Shellphone.

| # | Part | Qty | Notes / spec |
|---|------|-----|--------------|
| 1 | Raspberry Pi Zero W **or** Zero 2 W | 1 | Both work. Needs the 40-pin header soldered on (or buy the "WH" version with the header already on). |
| 2 | microSD card, pre-flashed | 1 | 8 GB or larger. Comes pre-flashed in the kit (the software is already on it). |
| 3 | Shellphone audio board (this project's PCB) | 1 | Export Gerbers from the KiCad project (`hardware/pcb/`) and order from a fab |
| 4 | MAX98357A I2S amplifier breakout | 1 | The blue audio amp module. Usually comes with a 7-pin header and a screw terminal. |
| 5 | 2-pin screw terminal, 3.5 mm pitch | 1 | Soldered onto the amp's **+** / **−** output (often included with the amp) |
| 6 | Bone-conduction transducer, with wires | 1 | **8 Ω, 1 W** — vibrates the shell to make sound |
| 7 | Speaker cable with a 2-pin plug | 1 | From the amp's screw terminal to the transducer |
| 8 | 5 mm LEDs | 2 | The snail's "eyes" (any color) |
| 9 | Resistor, 470 Ω | 2 | One per LED |
| 10 | 2×20 male pin header, 2.54 mm | 1 | Soldered to the Raspberry Pi (skip if your Pi already has one) |
| 11 | 2×20 female socket, 2.54 mm | 1 | On the audio board, plugs onto the Pi |
| 12 | 1×07 female socket, 2.54 mm | 1 | On the audio board, for the MAX98357A |
| 13 | A shell | 1 | Any shell works: a real seashell, or print the model in `enclosure/` |
| 14 | Hot glue | a little | To glue the transducer inside the shell |
| 15 | USB power supply + cable | 1 | 5 V, **at least 2 A**, micro-USB, to power the Pi |

### Notes
- Items 10–12 (the headers/sockets) are the connectors that let the boards plug together
  instead of being soldered permanently — easier to assemble and repair.
- The LEDs run from 5 V through the 470 Ω resistors (about 6 mA), so any color is bright enough.
