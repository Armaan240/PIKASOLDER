# PIKASOLDER
⚡ Pikachu PCB: Auto LED &amp; Motor Circuit A Pikachu-shaped PCB that lights up LEDs in the dark using an LDR and turns on both LEDs and a vibration motor when a button is pressed in daylight. Powered by a CR2032 coin cell and controlled via a BC547 transistor.

---
### **SLACK ID U091M21518T**
### **SLACK USERNAME @Amu**


### **What This Circuit Does**  
1. **Single-Button Control** (Keychain Switch):  
   - Press the button to **turn on 2 LEDs and the vibrating motor simultaneously**.  
   - Release to turn everything off.  

2. **Automatic Light Sensor (Optional LDR Mode)**:  
   - If you included an LDR, the LEDs can also turn on **automatically in darkness**.  

3. **Compact Design**:  
   - Powered by a **small battery (e.g., coin cell or 3V CR2032)** for portability.
  
   - **Images of The Project**
![PCB Preview](https://github.com/Armaan240/PIKASOLDER/blob/main/Screenshot%20(26).png)
![PCB Preview](https://github.com/Armaan240/PIKASOLDER/blob/main/Screenshot%20(28).png)
![PCB Preview](https://github.com/Armaan240/PIKASOLDER/blob/main/Screenshot%20(24).png)
![PCB Preview](https://github.com/Armaan240/PIKASOLDER/blob/main/Screenshot%20(25).png)
![PCB Preview](https://github.com/Armaan240/PIKASOLDER/blob/main/Screenshot%20(22).png)

---

## 📦 **Bill of Materials (BoM) – Pikachu PCB Project**

| **#** | **Part Name**               | **Label** | **Value/Type**     | **Package / Footprint**                             | **Qty** |
| ----- | --------------------------- | --------- | ------------------ | --------------------------------------------------- | ------- |
| 1     | NPN Transistor              | Q1 ,Q2    | BC547              | TO-92 (TO-92\_Inline)                               | 2       |
| 2     | Light Dependent Resistor    | LDR       |GL5528 (typical)    | Resistor\_THT\:R-2.5 (or similar photoresistor pad) | 1       |
| 3     | Resistor                    | R1        | 10kΩ               | R\_Axial\_DIN0207\_L6.3mm\_P7.62mm\_Horizontal      | 2       |
| 4     | Resistor                    | R2        | 100Ω – 470Ω        | Same as above                                       | 1       |
| 5     | Red LED                     | L1        | 5mm LED            | LED\_THT\:LED\_D5.0mm                               | 1       |
| 6     | Red LED                     | L2        | 5mm LED            | LED\_THT\:LED\_D5.0mm                               | 1       |
| 7     | Tactile Push Button         | SW1       | 6x6 mm Push Button | Button\_Switch\_THT\:SW\_PUSH\_6mm\_H5mm            | 1       |
| 8     | Coin Vibration Motor        | M1        | 3V Vibration Motor | Connected via header (Conn\_01x02\_Male)            | 1       |
| 9     | Coin Cell Battery Holder    | BT1       | CR2032 Holder      | Battery\_Holder\_Keystone\_3002\_1x20mm             | 1       |
| 10    | Generic Header (Motor Pads) | J1        | 2-pin male header  | Conn\_01x02\_Male or TestPoints                     | 1       |

---

Would you like me to export this BoM in `.csv` or `.xlsx` format ready for JLCPCB/assembly quoting?


### **Design Choices & Challenges**  
#### **Why This Design?**  
- **Keychain Use Case**: You wanted a simple, one-handed operation (no need for two-button safety).  
- **Minimalist Parts**: Reduced components to fit a small enclosure (e.g., keychain or pocket-sized).  

#### **Challenges Faced**  
- **Power Management**: Ensuring the battery can drive both LEDs and motor without draining too fast.  
   - *Fix*: Use low-current LEDs (e.g., 2mA) and a efficient motor (3V pager motor).  
- **Space Constraints**: Fitting everything into a tiny keychain form.  
   - *Fix*: SMD components or tightly arranged through-hole parts.  

#### **What I Learned**  
- **KiCad Tips**:  
  - Use **global labels** (e.g., `+VCC`, `GND`) to avoid messy wires.  
  - **ERC Checks** catch missing power connections early.  
- **Circuit Simplification**: Fewer parts = fewer points of failure.  

---

### **Advice for Beginners**  
1. **Start Simple**:  
   - If this is your **first PCB**, try a **single-LED + button circuit** before adding motors/sensors.  
2. **KiCad Learning Curve**:  
   - Watch tutorials on **schematic symbols** vs. **footprints** (common confusion).  
3. **Test on Breadboard First**:  
   - Verify the circuit works before designing the PCB.  

---

### **Optional Upgrades**  
1. **Add a Timer (555 IC)**:  
   - Make the motor vibrate for **10 seconds after button press**.  
2. **Low-Power Mode**:  
   - Use a **toggle switch** to disable the motor but keep LEDs.  

---
