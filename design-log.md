# Design Log

This document tracks my progress, reflections, and technical notes as I develop 3D CAD projects using Fusion 360.

---

## Overview

| Date       | Project           | Activity/Update                              | Key Tools Learned                       |
|------------|-------------------|----------------------------------------------|-----------------------------------------|
| 2025-07-4  | Charge_Head        | Modeled a USB charge head block with rounded edges | Extrude, Fillet, Chamfer, Revolve |
| 2025-07-11 | Map_of_Turkiye    | Created 3D map by sketching over canvas image| Canvas, Sketching, Extrude              |
| 2025-07-11 | Keychain_Tag      | Designed custom keychain with engraved text  | Text Tool, Constraints, Fillet, Extrude |
| 2025-07-28 | Perfume_Bottle    | Created a multi-profile bottle with thread and loft | Loft, Offset Planes, Guide Rails |

---

## Notes & Reflections

### Charge Head
- Practiced basic block modeling with symmetry and port cutouts.
- Used fillets and chamfers to soften the design like a real charger.

### Map of Türkiye
- Imported an image of the country using the **Canvas** feature.
- Drew the outline manually on a sketch plane.
- Used **Extrude** to give it depth and experimented with different heights.
- Learned how to align imported images and trace accurately.

### Keychain Tag
- Practiced applying **sketch constraints** to keep shapes controlled.
- Used **Text Tool** to engrave my name, then **Extruded** the cut.
- Added a 5 mm circular hole and applied **Fillets** to the corners.
- This was my first fabrication-ready design — could be printed directly.

### Perfume Bottle
- Designed with 8 main profile sketches across offset planes.
- Used **Loft** for an organic bottle shape.
- Learned the difference between **centerline** and **guide rails**.

### My Fusion Notes
- Prefer modeling fillet over sketch fillet in general. However, if you're using loft or sweep, you must use sketch fillets instead.
- You can draw sketches in mid-air using a construction plane.
- When creating an offset plane from another offset plane, changing the parent plane will shift the child plane too. For more consistent positioning, always offset from the origin planes instead.
- The revolve tool was used to model a symmetrical soda bottle, but for asymmetrical shapes, the loft tool is more appropriate.
- Inside the Sketch > Create > Project/Include menu, the Intersect tool is helpful when you want to create guide rails that precisely intersect the sketch plane (especially for loft).
- Use spline handles and snap them to a line to ensure smooth curvature continuity between the spline and the line.
- Use Sketch Mirror to duplicate any geometry symmetrically across a centerline.
- Apply fillets before using the shell command to avoid errors or distorted edges.
- The shell command works on a single, continuous solid body.
- Threads in Fusion 360 are visual-only and won’t appear in exported STL files or 3D prints.
- Shell command needs to operate on the whole body.
- Threads are only images and are not included in exports and prints.
- Choose “Compute Type” as Optimal if you want the fastest editor experience when doing rectangular patterns.
- Always use constraints over dimensions when possible.

---
