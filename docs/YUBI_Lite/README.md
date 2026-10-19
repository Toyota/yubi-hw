# YUBI Lite

## Overview

YUBI Lite is a simplified, lower-cost variant of the original YUBI Glove.
It is designed to make fabrication, sourcing, and assembly easier while
retaining as much of the original YUBI functionality as possible.

The design reduces the number of printed and purchased parts, removes
heat-set inserts and finger bushings, simplifies the electronics, and is
intended to be manufactured using a commonly available FDM 3D printer.
The primary printing material is PLA.

## Design Goals

- Make the glove easier for general users to fabricate and assemble.
- Reduce the number of printed and purchased parts.
- Reduce machining and assembly complexity.
- Avoid specialized parts where practical.
- Eliminate heat-set threaded inserts.
- Eliminate finger shaft bushings.
- Simplify the electronics and wiring.
- Use readily available screws and components.

## Changes from Original YUBI

### Directly Supported Finger Shafts

The four `JZF8-5` bushings used by the original YUBI Glove have been removed.
The YUBI Lite finger shafts are supported directly by the printed plates.

### Integrated Lower Plate and Handle

The handle is integrated into the lower plate. The separate `GRIP` printed
part, handle adjustment hardware, and related nut and groove features are no
longer required.

### Integrated Upper Plate and Quest Holder

The Quest controller holder is integrated into the upper plate for each hand.
The separate `HOLDER_Quest_R` and `HOLDER_Quest_L` parts and their mounting
screws are no longer required.

The standard YUBI Lite upper plate is designed for the lower-cost Innomaker
camera and is identified by the `_Innomaker` suffix. Upper plates for the
original YUBI camera are retained as compatibility options; they are not
additional parts required for the standard build.

The obsolete ESP32, universal PCB, and cable-cover mounting features have also
been removed from the upper plate.

### Simplified Electronics

The original ESP32C6, AS5601 board, universal PCB, pin headers, and associated
wiring have been replaced by an ENCUSB USB encoder board based on the AS5600.
See the [ENCUSB project](https://github.com/CH1H160/encusb) for board and
firmware information.

### Direct-Thread Fastening

The heat-set brass inserts used between the upper and lower plates have been
removed. Three M2.5 x 12 mm screws fasten directly into printed pilot holes in
the lower plate. M2.5 x 16 mm screws can also be used, but M2.5 x 12 mm is the
standard YUBI Lite length because it is easier to source.

### Simplified Covers and Grip Surface

The separate PCB and cable covers are no longer required. The original HYPER V
sheet is replaced by a more readily available commercial anti-slip sheet. See
the [YUBI Lite BOM](../BOM/YUBI_Lite_BOM.md) for the selected product.

## Hardware Configuration

Each YUBI Lite glove consists of:

- one hand-specific `_Innomaker` upper plate with an integrated Quest holder;
- one lower plate with an integrated handle;
- two hand-specific geared fingers;
- one right flap and one left flap;
- one hand-specific Meta Quest Touch Plus controller;
- one ENCUSB board and radial magnet;
- one [selected Innomaker USB camera](https://amzn.asia/d/05MBWu53);
- fasteners, an anti-slip sheet, and a rubber band as listed in the BOM.

## Required Printed Parts

The following table lists the printed parts required for one glove.

| Printed part | Right-hand glove | Left-hand glove |
| --- | ---: | ---: |
| Upper plate + Quest holder, right-hand (`_Innomaker`) | 1 | - |
| Upper plate + Quest holder, left-hand (`_Innomaker`) | - | 1 |
| Lower plate + handle | 1 | 1 |
| Finger with gear, `t30_R` | 1 | - |
| Finger with gear, `t20_L` | 1 | - |
| Finger with gear, `t30_L` | - | 1 |
| Finger with gear, `t20_R` | - | 1 |
| `FLAP_R` | 1 | 1 |
| `FLAP_L` | 1 | 1 |

The handle and Quest holder are integrated features and do not have separate
STL files.

## Original YUBI Camera Compatibility Option

The standard YUBI Lite build uses the Innomaker-camera upper plate. To reuse
the camera specified for the original YUBI, replace the standard upper plate
with the matching hand-specific compatibility part:

- `YUBI_Lite_R_UpperPlate_QuestHolder_OriginalCamera`
- `YUBI_Lite_L_UpperPlate_QuestHolder_OriginalCamera`

The optional STEP files are located in
`STEP/glove/lite/option parts/original camera/`, and the optional STL files are
located in `STL/glove/lite/option parts/original camera/`. Select exactly one
upper plate for each glove: either the standard `_Innomaker` part or the
`_OriginalCamera` compatibility part. For the original camera and its mounting
hardware, follow the original YUBI BOM and assembly documentation.

## Assembly Notes

1. Select the correct hand-specific upper plate and geared fingers. Use the
   `_Innomaker` upper plate for the standard build or the `_OriginalCamera`
   upper plate when using the original YUBI camera.
2. Check printed holes and mating surfaces for debris before assembly.
3. Install the ENCUSB board using four M2 x 6 mm screws. Tighten the screws
   gradually and evenly into the printed pilot holes.
4. Attach the flaps to the fingers using four M2 x 6 mm screws.
5. For the standard build, install the Innomaker camera using two M2.5 x 4 mm
   screws. When using the original YUBI camera option, follow the original
   YUBI camera mounting instructions instead.
6. Join the upper and lower plates using three M2.5 x 12 mm screws.
7. Confirm that both fingers move freely and that the collars provide suitable
   axial clearance before connecting the electronics.
8. Connect the camera and ENCUSB directly to the host using two USB
   connections.

The M2 and M2.5 screws cut directly into printed PLA. Avoid repeated removal
and installation and do not overtighten the screws, as this can damage the
printed threads. Before using screws from an assortment pack, confirm the
diameter, length, and head clearance against the printed part.

## Printing Notes

- Material: PLA.
- Process: FDM 3D printing.
- Use the provided STL files for printing and the STEP files for inspection or
  modification.
- Use slicer settings appropriate for the selected printer and PLA material.
- Inspect the finger support holes, printed collars, thrust surfaces, and
  direct-thread pilot holes after printing.
- Do not enlarge holes or change fit-critical geometry unless the resulting
  dimensions are measured and verified.

## License and Modification Notice

YUBI Lite is a modified variant of the original YUBI Glove.

- Original copyright: Copyright 2026 Toyota Motor Corporation
- Modified by: Jumpei Arima
- Modification date: [2026-10-16]
- Source location: https://github.com/Toyota/yubi-hw
- License: CERN-OHL-W v2

Summary of modifications:

- Removed the finger shaft bushings.
- Integrated the handle into the lower plate.
- Integrated the Quest holder into the upper plate.
- Replaced the ESP32/AS5601 electronics with ENCUSB.
- Removed heat-set inserts and simplified fastening.
- Simplified the covers, wiring, and purchased components.

