# ESP32 Power Controller
ESP32 power controller with 6 relays and 6 GPIO


## Revision Notes

### Rev. 0

1. **X1 Crystal footprint correction**    
   - Manufacturer part number: `830108208709`.
   - Footprint drawn from bottom view.
   - Part rotated 90 deg.
   - **Required change:** Corection of footprint.

2. **POWER GOOD signal routing**  
   - The **POWER GOOD** pin of **U3** is currently supplied from **VDD (5V)**.  
   - This 5V is routed through a **150kΩ resistor** to the **ESP32 `CHIP_UP` pin**.  
   - **Required change:** Supply **POWER GOOD** from **3.3V** instead of **VDD (5V)**.

3. **PCB size**
   - Board is too short
   - DM72-100-14-100Z(H) enclosure need 2mm PCB on both sides which are insertet in sides of enclosure
   - **Required change:** Add 2mm on both sides of PCB
   
4. **Error in ESP32 connection**
   - !!! warning: gpio 34, 35, 36 and 39 are input only pins. These pins do NOT have internal pull-up or pull-down resistors.
   - Rerouting relays and GPIO pins

### Rev. 1