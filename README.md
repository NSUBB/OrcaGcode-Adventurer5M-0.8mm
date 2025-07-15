# OrcaGcode-Adventurer5M-0.8mm
Custom G-Code for Orca Slicer for the FLashforge Adventurer 5M 0.8mm Nozzle Printer Profile

# OrcaGcode-Adventurer5M-0.8mm

🎯 **Custom Start G-Code for Orca Slicer** tailored for the **Flashforge Adventurer 5M** equipped with a **0.8mm nozzle**.

---

## 📌 Overview

This G-code snippet replaces the default machine start sequence in Orca Slicer for the Adventurer 5M when using a 0.8mm nozzle. It improves nozzle purging and prime line behavior to match the wider filament flow requirements of the 0.8mm hardware.

The code is saved with a `.001` extension to enable syntax highlighting in **VS Code**, which recognizes `.001` as G-code.

---

<img width="1163" height="603" alt="image" src="https://github.com/user-attachments/assets/96a1f106-7970-4329-a39f-0a65bf2572f0" />

## 🔧 Installation Steps

1. **Select the proper printer profile** in Orca Slicer:
   - Use the drop-down menu in the left-hand parameter pane.
   - Choose the profile that matches your Adventurer 5M and installed nozzle diameter.

2. **Edit the profile:**
   - Click the ✏️ **Edit icon** next to the printer drop-down.
   - In the pop-up window, switch to the **Machine G-code** tab.

3. **Replace the Start G-code:**
   -  Click the ✏️ **Edit icon** above the code window from the "Machine start G-code" section.
   - Delete all existing text from the "Machine start G-code" field.
   - Paste the contents of `OrcaGcode-Adventurer5M-0.8mm.001`.

5. **Save the profile:**
   - Click the 💾 **Disk icon** at the top to save your modified printer preset.
   - Note: You must save under a new name — default profiles cannot be overwritten.

---

## ⚠️ Nozzle Compatibility Notes

- This start G-code is optimized for **0.8mm nozzles**.
- Attempting to reuse the default start G-code from a 0.4mm profile with larger nozzle sizes may result in improper extrusion due to incompatible flow rate and extrude values.
- ⚙️ If adapting for **0.6mm**, consider reducing `E` values proportionally to match volumetric flow.

---

## 📜 Included G-Code Logic Highlights

- **Preheat Commands:** Heat bed and nozzle without waiting.
- **Nozzle Purge Routine:** Moves to purge position and performs extrusion/retraction for clearing.
- **Prime Line Sequence:** Lays down filament along the Y-axis and resets the extruder.
- **Positioning Modes:** Sets absolute positioning and relative extrusion.

---

🧠 Creator Notes
This code was created by DesignWeaver with attention to nozzle size requirements and hardware idiosyncrasies of the Adventurer 5M 0.8mm default printer preset. It aims to minimize startup issues and improve first-layer consistency.
