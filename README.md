# nemoPAD V1

A wireless split mechanical keyboard with per key kalih hotswap sockets, per key underglow RGB, a slide potentiometer for brightness control on the right half, and a rotary encoder for volume control on the left half. Uses a sandwich mount case (bottom case + plate + top frame) held together with heatset inserts and m2 20mm screws. The CAD features a unique design so it can join up to change into a full keeb visually. A project by Nemo made for Forge YSWS by Hackclub.

## Useful links
- **Total time spent:** [41h 11m](https://hackatime.hackclub.com/@Nemo_Donut/project/Keeb)
- **Devlogs:** [`JOURNAL.md`](./JOURNAL.md)
- **Onshape:** [CAD part of the project](https://cad.onshape.com/documents/d864244cbdf9531af3bfa9a7/w/1dab6020ee26630806b280f9/e/8f26d1999df9f3097243071e)

## Features
- Wireless split halves, each with its own XIAO nRF52840 MCU and LiPo battery
- Full hotswap (Kailh CPG151101S11 sockets), no soldering required for switches
- Per key RGB backlight using reverse mount underglow (SK6812MINI-E)
- MCP23017 I2C GPIO expander per half for full matrix coverage
- Slide potentiometer (right half) for brightness
- Rotary encoder with push (left half) for volume
- Sandwich mount case: top frame + plate + bottom case, screwed together with heatset inserts and m2 20mm screws

## Images
- Full 3D model render of the assembled keyboard (both halves)
  <img width="1540" height="519" alt="Screenshot_2026-09-04_02-22-25" src="https://github.com/user-attachments/assets/3a232dfd-a712-42f4-98ec-7c9b9fdd62a9" />

- PCB render/photo with components populated (both halves)
  <img width="1425" height="809" alt="Screenshot_2026-08-28_23-58-05" src="https://github.com/user-attachments/assets/23cb5420-9245-4964-9cdf-646af97ba9ca" /><img width="1398" height="844" alt="Screenshot_2026-08-28_23-58-38" src="https://github.com/user-attachments/assets/dbb1fc2f-e60e-4b54-bd47-6fb57a984e13" /><img width="1676" height="549" alt="Screenshot_2026-08-28_23-59-55" src="https://github.com/user-attachments/assets/5a5c89b3-d482-495f-84af-5bfc4ec5cd66" /><img width="1670" height="629" alt="Screenshot_2026-08-28_23-59-23" src="https://github.com/user-attachments/assets/8a2826cf-8928-458f-8f83-be6b3fa13cd8" />

- Schematic screenshots (1st image is left and 2nd image is right)
  <img width="4096" height="2896" alt="image" src="https://github.com/user-attachments/assets/44add1b8-890f-446d-80d9-4d8634af98d2" /><img width="4096" height="2896" alt="image" src="https://github.com/user-attachments/assets/e582bb9a-8771-4318-a64f-584c0f2b3515" />

- Exploded view of the sandwich mount stack (bottom case / plate / top frame)
  <img width="1175" height="755" alt="Screenshot_2026-09-04_00-50-46" src="https://github.com/user-attachments/assets/c9c23030-a82f-4a82-9955-6583c2c8a18b" /><img width="1621" height="394" alt="Screenshot_2026-09-04_00-51-38" src="https://github.com/user-attachments/assets/56c5ee4a-63d6-4c25-afd3-521554b51488" />

- Decal logo, custom encoder knob and hackclub logo emboss
  <img width="1217" height="631" alt="Screenshot_2026-09-04_01-49-30" src="https://github.com/user-attachments/assets/9b2d7237-ad8b-480b-9239-d40826769d83" /><img width="1483" height="761" alt="Screenshot_2026-09-04_01-49-09" src="https://github.com/user-attachments/assets/01323123-45d1-48f9-b91f-449617c4ae7c" /><img width="1365" height="831" alt="Screenshot_2026-09-04_00-55-01" src="https://github.com/user-attachments/assets/882a1318-ce00-4176-8b7f-69cde2169131" /><img width="1286" height="845" alt="Screenshot_2026-09-04_00-54-28" src="https://github.com/user-attachments/assets/057fdf02-d924-4327-baff-f9963403a1ac" />

## From concept to CAD
<p align="center">
  <img width="42%" alt="1dd2464e-4f92-4cd7-a45b-adbc3583a7b4" src="https://github.com/user-attachments/assets/3b827c1e-4936-42f4-9cda-f3b9f34c285b" />
  &nbsp;&nbsp;&nbsp;&nbsp;➡️&nbsp;&nbsp;&nbsp;&nbsp;
  <img width="42%" alt="Screenshot_2026-09-04_02-22-25" src="https://github.com/user-attachments/assets/aeeb57b2-e42c-4cd8-bda7-bd16f9c383ce" />
</p>

## Hardware design

### Sandwich mount stackup
| Layer | Thickness | Notes |
|---|---|---|
| Top frame | 6.3mm | Blind hole Ø3.5mm, 4.6mm deep for the heatset insert, no hole visible from outside |
| Plate | 1.5mm | Through hole Ø2.4mm for screw clearance |
| PCB | 1.6mm | |
| Bottom case (inner wall height) | 8mm | Clears the 3.05mm tall hotswap socket + ~3.16mm USB-C connector on the back layer with margin |
| Bottom case (bottom wall) | 3mm | Ø2.4mm x 1.2mm countersink on the underside so the screw head sits flush |

**Case is attached using** M2 x 4mm x 3.8mm OD brass heatset insert, M2 x 20mm countersunk screw.

**Battery pocket:** a local recessed pocket under the battery footprint on the inside of the bottom wall of bottom case (battery is the tallest bottom side component at ~5mm, taller than the general 6mm clearance zone needs). Battery wires are direct soldered to the BAT/GND test points, no connector.

## Bill of Materials
See [`BOM.csv`](./BOM.csv) for the full parts list with references, footprints, product links, and important notes.

### Summarised version:

| Component | Quantity | Total Price |
|---|---|---|
| 1N914 Diodes | 68 | ₹ 159.80 / $1.69 |
| SK6812MINI-E LEDs | 70 | ₹ 619.20 / $6.56 |
| 8.2k Resistor | 2 | ₹ 10.26 / $0.11 |
| 10k Resistor | 2 | ₹ 10.08 / $0.11 |
| Bourns Slide Potentiometer | 1 | ₹ 286.78 / $3.04 |
| Alps EC11E Rotary Encoder | 1 | NA (reused from kit) |
| Kailh Hotswap Sockets (all sizes) | 68 | ₹ 350.00 / $3.71 |
| MX-style Switches (all sizes) | 68 | ₹ 2,598.00 / $27.51 |
| Keycaps – 1u | 60 | ₹ 1,020.00 / $10.80 |
| Keycaps – 1.75u | 4 | ₹ 180.00 / $1.91 |
| Keycaps – 1.5u | 2 | ₹ 180.00 / $1.91 |
| Keycaps – 1.25u | 2 | NA (3D printed) |
| MCP23017 GPIO Expander | 2 | ₹ 539.00 / $5.71 |
| XIAO nRF52840 (modified) | 2 | ₹ 2,418.00 / $25.60 |
| LiPo Battery 500mAh | 2 | ₹ 476.98 / $5.05 |
| PCB (2-layer panel) | 5 | ₹ 5,003.00 / $52.97 |
| Heatset Insert | 8 | ₹ 108.65 / $1.15 |
| Case Screw | 8 | (included above) |
| 3D Printed Parts (case, plate, frame, knob, keycap) | 7 | ₹ 1,956.06 / $20.71 |
| **GRAND TOTAL** | | **₹ 15,915.81 / $168.51** |

## Assembly
1. Solder components to both PCB halves (or have them assembled), separate the panel at the mousebite tabs
2. Solder battery leads to BAT/GND test points on each half
3. Insert hotswap sockets, install switches
4. Heatset the M2 inserts into each top frame's blind holes
5. Sandwich bottom case -> PCB -> plate -> top frame, secure with M2x18mm screws
6. Flahing steps still needs work.

## Flashing

The keyboard uses two Seeed XIAO nRF52840 boards, one for each half. Separate firmware files are provided for the left and right halves.

### Requirements

* USB-C data cable
* Computer
* The appropriate `.uf2` firmware file

### Flash the Left Half

1. Connect the **left-half XIAO nRF52840** to your computer via USB.
2. Double-click the XIAO's **Reset** button to enter bootloader mode.
3. A USB mass-storage drive should appear.
4. Copy `zmk_left.uf2` onto the bootloader drive (Found inside Firmware folder).
5. The XIAO will automatically reboot after the firmware is copied.

### Flash the Right Half

1. Connect the **right-half XIAO nRF52840** to your computer via USB.
2. Double-click the XIAO's **Reset** button to enter bootloader mode.
3. A USB mass-storage drive should appear.
4. Copy `zmk_right.uf2` onto the bootloader drive (Found inside Firmware folder).
5. The XIAO will automatically reboot after the firmware is copied.

### Firmware Source

The firmware is built using **ZMK** with the Seeed XIAO nRF52840 target.

The provided firmware files are:

```text
Firmware/
├── zmk_left.uf2
└── zmk_right.uf2
```

The firmware currently represents the development stage prototype. Both left and right firmware builds complete successfully; physical flashing and keyboard testing will be performed once the PCBs and components are available.

---

<p align="center">
  <img width="120" alt="nemo" src="https://github.com/user-attachments/assets/b7678182-ac80-43ee-81a7-a9201e3da078" />
</p>
