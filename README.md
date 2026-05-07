# Integrated Mecanum Drive (IMD)

**This modification for GoBILDA mecanum wheels allows for direct-drive motor integration within the wheel assembly.**

## Why Build This?

<table>
  <tr>
    <td valign="top">
      Standard mecanum drives often require bulky chain, belt, or gear-driven setups inside the robot chassis. This modification integrates the motor directly into the wheel hub, offering:<br><br>
      <ul>
        <li><b>Maximized Internal Space:</b> Frees up chassis space for electronics and mechanisms.</li>
        <li><b>Rapid Serviceability:</b> Self-contained design allows for quick drive unit swaps, eliminating the need for main chassis disassembly.</li>
        <li><b>Zero Backlash:</b> Direct-drive eliminates the slop inherent in chain/belt reductions.</li>
        <li><b>Fewer Points of Failure:</b> Eliminates external belts, chains, and pulleys, reducing the overall part count and removing the need for regular tensioning.</li>
      </ul>
    </td>
    <td valign="top">
      <img src="https://github.com/user-attachments/assets/88ecc75c-6c18-4dcf-b4aa-6bffc58c79b7" alt="Classic vs IMD Design Comparison" width="300" />
    </td>
  </tr>
</table>

<img alt="CAD model 1" src="https://github.com/user-attachments/assets/ae730f42-582e-4b8e-98d2-0a5ea0b28907" />

<p align="center">
  <img alt="Real life model 1" src="https://github.com/user-attachments/assets/289cd1fa-0897-4077-aa86-7879d43f984e" width="49%" />
  <img alt="Real life model 2" src="https://github.com/user-attachments/assets/fd794e58-b919-4805-a193-9f37b1895fc0" width="49%" />
</p>

## Basic Characteristics
* **Base Wheel:** goBILDA GripForce™ Mecanum Ø104mm Wheel Set (40A Durometer).
* **Propulsion:** goBILDA 5203 Series Yellow Jacket Planetary Gear Motor (435 RPM).
* **Structural Frame:** Custom 3D printed motor mounts and precision shaft spacers.
* **Power Transfer:** Direct-drive (1:1 ratio) utilizing the heavy-duty 8mm REX™ shaft ecosystem.
* **Estimated Performance:** Theoretical top speed of ~2.3 m/s (with 435 RPM motor).

## CAD Model & Configurable Assembly
The model was designed in Onshape. You can view, interact with, and export the configurable assembly (along with the complete BOM) directly from your browser here:

**[Open IMD in Onshape](https://cad.onshape.com/documents/8f367a5f6d2e58f122acd332/w/d92d81f4d48a76e09882f61c/e/26f170c9af19b0b97c028cc4?configuration=default&bomType=structured&renderMode=0&leftPanel=false&rightPanel=BOMPanel&uiState=69f9285e0bdfad3c58fb90e0)**

## Example Applications (Drivebases)
To help you integrate these modules into your robot, I have included CAD models for two example drivebases in the `Drivebase_Examples` folder:
1. **goBILDA U-Channel Chassis:** Demonstrates how to mount the modules using standard goBILDA structural components.         
**[View goBILDA U-Channel Chassis in Onshape](https://cad.onshape.com/documents/8f367a5f6d2e58f122acd332/w/d92d81f4d48a76e09882f61c/e/bcba49029b301266226bcfa4)**
2. **Custom Plate Chassis:** Demonstrates how to mount the modules using custom-machined plates and standoffs for a more compact footprint.
**[View Custom Plate Chassis in Onshape](https://cad.onshape.com/documents/8f367a5f6d2e58f122acd332/w/d92d81f4d48a76e09882f61c/e/f1c13dd2a2df37d270d419c0)**

<p align="center">
  <img alt="goBILDA Chassis CAD model 1" src="https://github.com/user-attachments/assets/b353e71b-cdf1-40f3-9fd2-dad34ba7a79d" width="49%" />
  <img alt="Custom Chassis CAD model 1" src="https://github.com/user-attachments/assets/a9986950-731c-406e-b2f5-aae164622a2f" width="49%" />
</p>

## 3D Printing Recommendations
These custom parts handle the structural weight of the robot and the motor's torque, so part strength is critical. 

* **Recommended Setup (Tested):** Nylon (PA) with 4+ perimeters/walls and 50% infill (Gyroid or Cubic). 
* **Alternative Materials:** PETG, ABS, ASA, or Polycarbonate.
* **A Note on PLA:** While standard PLA is generally not recommended for competition robotics due to impact brittleness, prototype testing proved that 100% infill PLA successfully handled up to an 80kg static load without failing.

## Bill of Materials (BOM)
To build **one** complete wheel module, you will need the following parts:

| Item | Quantity | Name |
| :--- | :--- | :--- |
| 1 | 1 | 104mm Mecanum Wheel (Ø104mm, 40A Durometer Rollers) 3625-0202-0104 [`goBILDA`](https://www.gobilda.com/gripforce-mecanum-wheel-set-o104mm-40a-durometer-rollers/) |
| 2 | 1 | 1309 Series Sonic Hub (8mm REX® Bore) 1309-0016-4008 [`goBILDA`](https://www.gobilda.com/1309-series-sonic-hub-8mm-rex-bore/) |
| 3 | 1 | 1401 Series 2-Side, 2-Post Clamping Mount (43mm Width, 36mm Bore) [`goBILDA`](https://www.gobilda.com/1401-series-2-side-2-post-clamping-mount-43mm-width-36mm-bore/) |
| 4 | 1 | 1611 Series Flanged Ball Bearing (8mm REX ID x 14mm OD, 5mm Thickness) 1611-0514-4008 [`goBILDA`](https://www.gobilda.com/1611-series-flanged-ball-bearing-8mm-rex-id-x-14mm-od-5mm-thickness-2-pack/) |
| 5 | 1 | 5203 Series Yellow Jacket Planetary Gear Motor (13.7:1 Ratio, 24mm Length 8mm REX Shaft, 435 RPM, 3.3 - 5V Encoder) 5203-2402-0014 [`goBILDA`](https://www.gobilda.com/5203-series-yellow-jacket-planetary-gear-motor-13-7-1-ratio-24mm-length-8mm-rex-shaft-435-rpm-3-3-5v-encoder/) |
| 6 | 4 | Hex nut grade A & B M4x0.7 |
| 7 | 4 | Hex socket countersunk head screw M4x0.7 x 12 |
| 8 | 1 | Hex socket head cap screw M4x0.70 x 14 |
| 9 | 4 | Hex socket head cap screw M4x0.70 x 30 x 20 |
| 10 | 1 | Motor mount [`3d Printed`](https://cad.onshape.com/documents/8f367a5f6d2e58f122acd332/w/d92d81f4d48a76e09882f61c/e/5f703f59c31e528baac41de4)|
| 11 | 1 | Shaft spacer [`3d Printed`](https://cad.onshape.com/documents/8f367a5f6d2e58f122acd332/w/d92d81f4d48a76e09882f61c/e/1af7b1871e39168f8384e6b7)|
| 12 | 1 | Wheel Spacer [`3d Printed`](https://cad.onshape.com/documents/8f367a5f6d2e58f122acd332/w/d92d81f4d48a76e09882f61c/e/5f703f59c31e528baac41de4)|

## Assembly instructions
<img width="4961" height="3508" alt="Integrated Mecanum Drive (IMD) Assembly instructions" src="https://github.com/user-attachments/assets/1cb9ba51-6167-4341-a4bd-43b892eef80c" />

Integrated Mecanum Drive (IMD)  © 2026 by Gabriel Pieniek is licensed under CC BY-NC-SA 4.0. To view a copy of this license, visit https://creativecommons.org/licenses/by-nc-sa/4.0/
