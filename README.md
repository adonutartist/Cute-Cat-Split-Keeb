# nemoPAD V1

A wireless split mechanical keyboard with per key kalih hotswap sockets, per key underglow RGB, a slide potentiometer for brightness control on the right half, and a rotary encoder for volume control on the left half. Uses a sandwich mount case (bottom case + plate + top frame) held together with heatset inserts and m2 18mm screws. The CAD features a unique design so it can join up to change into a full keeb visually. A project by Nemo made for Forge YSWS by Hackclub.

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
- Sandwich mount case: top frame + plate + bottom case, screwed together with heatset inserts and m2 18mm screws

## Images
- Full 3D model render of the assembled keyboard (both halves)
  <img width="1868" height="660" alt="Screenshot_2026-08-28_23-53-06" src="https://github.com/user-attachments/assets/1beb9fc9-1d25-4de9-b328-b8eb0f77f147" />

- PCB render/photo with components populated (both halves)
  <img width="1425" height="809" alt="Screenshot_2026-08-28_23-58-05" src="https://github.com/user-attachments/assets/23cb5420-9245-4964-9cdf-646af97ba9ca" /><img width="1398" height="844" alt="Screenshot_2026-08-28_23-58-38" src="https://github.com/user-attachments/assets/dbb1fc2f-e60e-4b54-bd47-6fb57a984e13" /><img width="1676" height="549" alt="Screenshot_2026-08-28_23-59-55" src="https://github.com/user-attachments/assets/5a5c89b3-d482-495f-84af-5bfc4ec5cd66" /><img width="1670" height="629" alt="Screenshot_2026-08-28_23-59-23" src="https://github.com/user-attachments/assets/8a2826cf-8928-458f-8f83-be6b3fa13cd8" />

- Schematic screenshots (1st image is left and 2nd image is right)
  <img width="4096" height="2896" alt="image" src="https://github.com/user-attachments/assets/44add1b8-890f-446d-80d9-4d8634af98d2" /><img width="4096" height="2896" alt="image" src="https://github.com/user-attachments/assets/e582bb9a-8771-4318-a64f-584c0f2b3515" />

- Exploded view of the sandwich mount stack (bottom case / plate / top frame)
  <img width="1319" height="802" alt="Screenshot_2026-08-29_00-12-12" src="https://github.com/user-attachments/assets/b7efc063-2d6f-40a1-8e0b-d163fa021bef" />

## From concept to CAD
<p align="center">
  <img width="42%" height="1479" alt="1dd2464e-4f92-4cd7-a45b-adbc3583a7b4" src="https://github.com/user-attachments/assets/3b827c1e-4936-42f4-9cda-f3b9f34c285b" />
  &nbsp;&nbsp;&nbsp;&nbsp;➡️&nbsp;&nbsp;&nbsp;&nbsp;
  <img width="42%" height="660" alt="Screenshot_2026-08-28_23-53-06" src="https://github.com/user-attachments/assets/4b1a8da9-74fb-4685-b732-ddd5b3463b1c" />
</p>

## Hardware design

### Sandwich mount stackup
| Layer | Thickness | Notes |
|---|---|---|
| Top frame | 6.3mm | Blind hole Ø3.2mm, 4.6mm deep for the heatset insert, no hole visible from outside |
| Plate | 1.5mm | Through hole Ø2.4mm for screw clearance |
| PCB | 1.6mm | |
| Bottom case (inner wall height) | 7mm | Clears the 3.05mm tall hotswap socket + ~3.16mm USB-C connector on the back layer with margin |
| Bottom case (bottom wall) | 3mm | Ø2.4mm x 1.2mm countersink on the underside so the screw head sits flush |

**Case is attached using** M2 x 4mm x 3.5mm OD brass heatset insert, M2 x 18mm countersunk screw.

**Battery pocket:** a local recessed pocket under the battery footprint on the inside of the bottom wall of bottom case (battery is the tallest bottom side component at ~5mm, taller than the general 6mm clearance zone needs). Battery wires are direct soldered to the BAT/GND test points, no connector.

## Bill of Materials
See [`BOM.csv`](./BOM.csv) for the full parts list with references, footprints, and quantities.

## Assembly
1. Solder components to both PCB halves (or have them assembled), separate the panel at the mousebite tabs
2. Solder battery leads to BAT/GND test points on each half
3. Insert hotswap sockets, install switches
4. Heatset the M2 inserts into each top frame's blind holes
5. Sandwich bottom case -> PCB -> plate -> top frame, secure with M2x18mm screws
6. Flahing steps still needs work.

## Flashing
<!-- TODO: firmware repo link, flashing instructions -->

---

<!-- TODO: replace logo.png with your actual logo filename -->
<p align="center">
  <img width="120" alt="nemo" src="https://github.com/user-attachments/assets/b7678182-ac80-43ee-81a7-a9201e3da078" />
</p>
