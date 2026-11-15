# MicroDock V2 for Bambu Lab A1 Mini

A printable, experimental adaptation of [Vottivott's MicroDock V2](https://github.com/Vottivott/microduck-playground/tree/main/hardware/microdock-v2) for the Bambu Lab A1 Mini. The base is split into sliding sections, and the panel uses three rear snap-fit catches and two alignment guides. The AprilTag is a printed sticker.

## Download and print

Two Bambu Studio projects are available:

- **[MicroDock_A1_Mini_PLA.3mf](MicroDock_A1_Mini_PLA.3mf)** — recommended: supports are configured, including inside both female base channels.
- **[MicroDock_A1_Mini_PLA_NoSupports.3mf](MicroDock_A1_Mini_PLA_NoSupports.3mf)** — the same parts with supports disabled for manual setup. Bambu Studio reports unsupported areas on plates 1–5 and 7. Do not print those plates as-is without checking the preview and adding appropriate supports or changing the orientation.

Both projects are set up for the A1 Mini, a 0.4 mm nozzle, 0.20 mm layers, textured PEI plate and Bambu PLA Basic. Select the appropriate profile and reslice if you use a different filament or build plate. The [STL files](STL/) contain only geometry, without generated supports.

| Plate | Contents | Estimated PLA | Estimated time |
|---|---|---:|---:|
| 1–4 | Four base sections | 129.3 g | 3 h 57 min |
| 5 | Two fit-test pieces | 11.8 g | 38 min |
| 6 | Lower panel | 47.9 g | 72 min |
| 7 | Upper panel and two base locking pins | 40.4 g | 64 min |

With the recommended supports and without the test plate, the estimate is approximately **218 g and 6 h 12 min**. Times and filament use depend on the printer and settings. The hood and keeper are not included in the project: reuse the original parts or obtain them from the [original MicroDock](https://github.com/Vottivott/microduck-playground/tree/main/hardware/microdock/stl).

Individual files are available in [STL/](STL/). If printing these separately, print **two** copies of `base_lock_pin_print_2.stl`. The 3MF already includes both pins.

## Test the panel joint first

The updated test piece removes the earlier model's nominal 0.2 mm gap between panel faces. Print plate 5 and check that the catch engages, releases and returns without excessive force. If you already printed the earlier lower test piece, it is unchanged and can be reused. Check for support residue, whitening, cracks or permanent deformation before printing the full panel.

## Assembly

![Exploded view of the base](images/base_assembly.png)

1. Slide the two rear base sections together, then slide the two front sections together.
2. Slide the front group sideways onto the rear group. Align the holes and press in the two pins. Check the fit without forcing them.
3. Insert the upper panel vertically into the lower panel. The two rigid guides align the halves; the three rear catches retain them.
4. To release the panel, press the three catches through the rear openings toward the panel while gently lifting the upper half. A small blunt tool may help; do not force the printed arms.
5. Insert the panel into the base, then install the original hood and keeper as shown in the [original assembly manual](https://github.com/Vottivott/microduck-playground/blob/main/hardware/microdock-v2/media/microdock_v2_assembly.pdf).

![Exploded view of the panel](images/panel_assembly.png)

The images show actual CAD geometry with components separated and coloured to make assembly easier to follow.

## AprilTag sticker

Print [AprilTag_36h11_ID0_60mm.svg](AprilTag_36h11_ID0_60mm.svg) in black on white adhesive paper at **100% / actual size**, without fitting to page. Measure the outside square: it must be **60 × 60 mm**. Preserve the white border and the orientation; this is AprilTag 36h11 ID 0, not a QR code.

Place the sticker flat and centred horizontally on the front of the upper panel. Its centre is **39 mm below the top edge**; a 60 mm sticker therefore starts approximately 9 mm below the top and 25 mm from each side. Camera recognition with the sticker has not yet been tested.

## Supports and validation

Both panel faces are oriented toward the bed. The sticker face does not need support underneath it; the tested slicer setup generated no support for the lower panel and some support on the back of the upper panel and on the base. The recommended project enables supports on model surfaces as well as the build plate for the rear and front female base sections (plates 2 and 4). This creates support inside their channels. Inspect the preview and remove support carefully around the guides and flexible catches.

The panel meshes were checked for closed geometry and assembled clearances. Bambu Studio 02.09.01.70 sliced all seven plates of the supported project without warnings; the support-free project produced floating-region warnings on six plates. The user reported a successful print with internal support on the rear female base; the front female section has the same support approach but has not yet been physically verified. The updated joint, long-term PLA strength, sticker recognition and the complete dock still require physical testing. The base is 2 mm thicker than the original and has a modified ramp; robot approach on that ramp has not been verified.

## Attribution and license

This project adapts [MicroDock V2 by Vottivott](https://github.com/Vottivott/microduck-playground). The hardware designs are distributed under [CC BY-NC-SA 4.0](LICENSE-HARDWARE), which restricts commercial use. This adaptation includes modified base and panel geometry and print layouts.
