# GLaDOS-Cam

> Edge AI IoT board for vision-based applications

---

## Overview

GLaDOS-Cam is a custom PCB built around the **STM32U575VIT6** (Cortex-M33, 160 MHz) targeting battery-powered, field-deployed TinyML inference. No NPU. No cloud. Runs INT8 inference locally at 1–2 fps which is all that's needed.

---

## Hardware

| # | Component | Manufacturer | Part No. | JLCPCB |
|---|---|---|---|---|
| 1 | MCU | STMicroelectronics | STM32U575**VIT6** | C5270999 |
| 2 | PSRAM | ISSI | IS66WVH8M8BLL-100B1LI | C1349096 |
| 3 | LDO (3.3 V aux) | STMicroelectronics | STLQ020C33R | C2970558 |
| 4 | Camera connector | Hirose | FH12-24S-0.5SH(55) | C202112 |
| 5 | Camera AVDD LDO (2.8 V) | YONGYUTAI | XC6206-2.8V | C2892669 |
| 6 | Camera DVDD LDO (1.2 V) | YONGYUTAI | XC6206-1.2V | C49446790 |
| 7 | Crystal 16 MHz | YXC | X322516MLB4SI | C13738 |
| 8 | Crystal 32.768 kHz | Seiko Epson | Q13FC13500004 | C32346 |
| 9 | Reset button | XKB Connection | TS-1187A-B-A-B | C318884 |
| 10 | MicroSD slot | SHOU HAN | TF-CARD H1.8 | C7529389 |

## Toolchain

| Tool | Purpose |
|---|---|
| KiCad 9 | Schematic + PCB layout |

---

## Repo Structure

```
GLaDOS-Cam/
├── docs/                          # Datasheets, BOM references
│   ├── Component_List.xlsx
│   ├── ESP32_CAM_V1.6.pdf
│   └── NUCLEO-U575ZI-Q/
└── pcb/
    └── GLaDOS-Cam/
        ├── GLaDOS-Cam.kicad_pro   # Project root
        ├── GLaDOS-Cam.kicad_sch   # Top-level schematic
        ├── GLaDOS-Cam.kicad_pcb   # PCB layout
        ├── cam_conn.kicad_sch     # Camera connector sub-sheet
        ├── io_headers.kicad_sch
        ├── mcu.kicad_sch
        ├── microsd.kicad_sch
        ├── power.kicad_sch
        ├── psram.kicad_sch
        └── glados-cam-lib/        # Project-local KiCad library
            ├── glados-cam-lib.pretty/   # Footprints
            │   └── 3d_models/           # STEP files
            └── symbols/
```

---
