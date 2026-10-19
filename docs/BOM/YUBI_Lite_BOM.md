# YUBI Lite Bill of Materials

## Scope

This BOM contains the parts required to build one YUBI Lite glove. Select the
right-hand or left-hand printed parts and Quest controller for the intended
configuration.

YUBI Lite is an additional variant and does not replace the original
[YUBI Glove BOM](YUBI%20Glove%20Assy_BOM.md). Quantities below are for one
glove unless otherwise noted.

## 3D-Printed Parts

| No. | Part No. | Type | Part name | Qty. | Material | Remarks | File basename |
| ---: | --- | --- | --- | ---: | --- | --- | --- |
| 1 | YUBI_Lite_R_UpperPlate_QuestHolder_Innomaker | 3D-PRINTED | Upper plate + Quest holder | 1 | PLA | Right-hand standard; Innomaker camera | `YUBI_Lite_R_UpperPlate_QuestHolder_Innomaker` |
| 2 | YUBI_Lite_L_UpperPlate_QuestHolder_Innomaker | 3D-PRINTED | Upper plate + Quest holder | 1 | PLA | Left-hand standard; Innomaker camera | `YUBI_Lite_L_UpperPlate_QuestHolder_Innomaker` |
| 3 | YUBI_Lite_UnderPlate_Handle | 3D-PRINTED | Lower plate + handle | 1 | PLA | Common to both hands | `YUBI_Lite_UnderPlate_Handle` |
| 4 | YUBI_Lite_R_Finger_R | 3D-PRINTED | Finger with gear, t30 right | 1 | PLA | Right-hand outer finger | `YUBI_Lite_R_Finger_R` |
| 5 | YUBI_Lite_R_Finger_L | 3D-PRINTED | Finger with gear, t20 left | 1 | PLA | Right-hand inner finger | `YUBI_Lite_R_Finger_L` |
| 6 | YUBI_Lite_L_Finger_L | 3D-PRINTED | Finger with gear, t30 left | 1 | PLA | Left-hand outer finger | `YUBI_Lite_L_Finger_L` |
| 7 | YUBI_Lite_L_Finger_R | 3D-PRINTED | Finger with gear, t20 right | 1 | PLA | Left-hand inner finger | `YUBI_Lite_L_Finger_R` |
| 8 | YUBI_Lite_Flap_R | 3D-PRINTED | Right flap | 1 | PLA | Required for either hand | `YUBI_Lite_Flap_R` |
| 9 | YUBI_Lite_Flap_L | 3D-PRINTED | Left flap | 1 | PLA | Required for either hand | `YUBI_Lite_Flap_L` |

For one glove, select either item 1 or 2 and the matching pair of finger parts.
Items 3, 8, and 9 are common to both configurations. In a finger filename,
the first `R` or `L` identifies the glove hand and the final `R` or `L`
identifies the corresponding finger part.

## Electronics and Purchased Components

| No. | Part No. | Type | Part name | Qty. | Link | Remarks |
| ---: | --- | --- | --- | ---: | --- | --- |
| 10 | Meta Quest 3s(128G) | STANDARD | Meta Quest 3s(128G) | 1 | [Link](https://www.meta.com/quest/quest-3s/) | Right-hand only; select one controller |
| 11 | ENCUSB | STANDARD | AS5600-based USB encoder board | 1 | [Link](https://www.switch-science.com/products/11233) | Four M2 mounting holes; including radial magnet |
| 12 | USB_CAMERA | STANDARD | Innomaker USB camera | 1 | [Link](https://amzn.asia/d/05MBWu53) | Camera USB cable included |
| 13 | USB_CABLE_ENCUSB | STANDARD | USB-C to USB-A cable, 0.5 m | 1 | [Link](https://amzn.asia/d/0iy48tzh) | Right-angle USB-C connector recommended |

## Fasteners

| No. | Size | Type | Qty. | Joint |
| ---: | --- | --- | ---: | --- |
| 14 | M2 x 6 mm | Screw | 4 | ENCUSB to integrated mounting bosses |
| 15 | M2 x 6 mm | Screw | 4 | Flaps to fingers |
| 16 | M2.5 x 12 mm | Screw | 3 | Upper plate to lower plate |
| 17 | M2.5 x 4 mm | Screw | 2 | Innomaker camera to upper plate |

- [M2.5 screw set](https://amzn.asia/d/0eekOX0j)
- [M2 screw set](https://amzn.asia/d/0e6dPWLF)

The linked products are reference assortment sets; purchasing both sets is a
convenient way to obtain the required sizes. For one glove:

- use eight M2 x 6 mm screws from the M2 set: four for ENCUSB and four for the
  flap-to-finger joints;
- use two M2.5 x 4 mm screws from the M2.5 set for the camera; and
- use three M2.5 x 12 mm screws from the M2.5 set for the upper-to-lower plate
  joint.

Other screw sizes included in the sets are not required for the standard YUBI
Lite assembly. M2.5 x 16 mm screws may be used instead of M2.5 x 12 mm for the
upper-to-lower plate joint, but M2.5 x 12 mm is the standard size. Confirm the
screw diameter, length, and head clearance before assembly. These screws form
threads directly in printed PLA, so tighten them gradually and do not
overtighten.

## Consumables

| No. | Part No. | Type | Part name | Qty. | Link |
| ---: | --- | --- | --- | --- | --- |
| 18 | ANTI_SLIP_SHEET | STANDARD | Commercial anti-slip sheet | As required | [Link](https://amzn.asia/d/09hs7jmA) |
| 19 | RUBBER_BAND_No.16 | STANDARD | Rubber band No. 16 | 1 | [Link](https://amzn.asia/d/02ohoDKM) |

## Hand-Specific Part Selection

| Configuration | Upper plate | Outer finger | Inner finger | Quest controller |
| --- | --- | --- | --- | --- |
| Right-hand glove | `YUBI_Lite_R_UpperPlate_QuestHolder_Innomaker` | `YUBI_Lite_R_Finger_R` (`t30_R`) | `YUBI_Lite_R_Finger_L` (`t20_L`) | Right controller |
| Left-hand glove | `YUBI_Lite_L_UpperPlate_QuestHolder_Innomaker` | `YUBI_Lite_L_Finger_L` (`t30_L`) | `YUBI_Lite_L_Finger_R` (`t20_R`) | Left controller |

All configurations also require the common lower plate with integrated handle,
`FLAP_R`, and `FLAP_L`.

## Optional Camera Compatibility Parts

These parts allow the camera specified for the original YUBI to be used with
YUBI Lite. Each part replaces the corresponding standard `_Innomaker` upper
plate; it is not installed in addition to it.

| No. | Part No. | Type | Part name | Qty. | Material | Remarks | File basename |
| ---: | --- | --- | --- | ---: | --- | --- | --- |
| 101 | YUBI_Lite_R_UpperPlate_QuestHolder_OriginalCamera | 3D-PRINTED | Upper plate + Quest holder | 1 | PLA | Right-hand option; replaces item 1 | `YUBI_Lite_R_UpperPlate_QuestHolder_OriginalCamera` |
| 102 | YUBI_Lite_L_UpperPlate_QuestHolder_OriginalCamera | 3D-PRINTED | Upper plate + Quest holder | 1 | PLA | Left-hand option; replaces item 2 | `YUBI_Lite_L_UpperPlate_QuestHolder_OriginalCamera` |

The optional files are stored under
`STEP/glove/lite/option parts/original camera/` and
`STL/glove/lite/option parts/original camera/`. Use the original YUBI BOM and
assembly documentation for the original camera and its mounting hardware.

## Removed or Replaced Parts

The following original YUBI Glove items are not required by YUBI Lite.

| Original part | Original qty. | YUBI Lite change |
| --- | ---: | --- |
| `GRIP` | 1 | Integrated into lower plate |
| `HOLDER_Quest_R` / `HOLDER_Quest_L` | 1 selected | Integrated into hand-specific upper plate |
| `COVER_PCB_R` / `COVER_PCB_L` | 1 selected | Removed |
| `COVER_CABLE_R` / `COVER_CABLE_L` | 1 selected | Removed |
| ESP32C6 | 1 | Replaced by ENCUSB |
| AS5601 board | 1 | Replaced by ENCUSB with AS5600 |
| Universal PCB | 1 | Removed |
| Original pin headers and encoder wiring | Various | Removed or replaced by direct USB connection |
| `JZF8-5` | 4 | Removed; shafts supported directly by printed plates |
| `AJKTNS5-70` | 1 | Removed with separate handle assembly |
| `HNTT5-5` | 1 | Removed with separate handle assembly |
| `LRLM3-6` | 1 | Removed with old handle structure |
| `SB-264040` | 5 | Removed; direct-thread fastening used |
| `SB-304540` | 2 | Removed; direct-thread fastening used |
| `CB2.5-8` | 2 | Removed with separate Quest holder |
| `CB2.5-15` | 3 | Replaced by three M2.5 x 12 mm screws |
| `CB3-6` | 1 | Removed with PCB/cable covers |
| `CBSTNR3-5` | 2 | Removed |
| `PX-10H15_HYPER V SHEET` | 2 pieces | Replaced by commercial anti-slip sheet |
| Old encoder-board screws | Various | Replaced by four M2 x 6 mm screws |

## Vendor Link Notice

Product links are provided for convenience only.
