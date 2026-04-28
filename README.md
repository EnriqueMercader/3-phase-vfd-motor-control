# 3-Phase Sine-Wave PWM Variable Frequency Drive (VFD)

**High-performance motor control system built from scratch** — 1 Hz to 3800 Hz output range. Successfully drove a 3-phase BLDC motor up to 140 Hz using bare-metal PIC16F18876 firmware and custom IGBT power stage.

![VFD Hero](https://www.enrique-mercader.com/assets/images/projects/vfd/hero-vfd.jpg)  
*Real-time gate LED visualization + 7-segment frequency display on custom PCB*

## Highlights
- **Full custom firmware** from datasheet only (no libraries): 42-point sine lookup table (acting as a 84-point lookup table), sine-wave modulated PWM, main program cycle not used and available for other tasks.
- **Power stage**: 650V high-speed IGBTs with opto-isolated drivers.
- **Hardware**: Designed in EasyEDA → fabricated in China → hand-assembled. Includes push-button speed control and live PWM gate visualization LEDs.
- **Performance**: Stable operation across wide frequency range with efficient switching and minimal resources.

**Live Demo Video** → 

**Full Project Story** → [enrique-mercader.com/projects/3-phase-variable-frequency-drive](https://www.enrique-mercader.com/projects/3-phase-variable-frequency-drive) (includes development photos, motor build, and testing)

## Technical Deep Dive
- **Microcontroller**: PIC16F18876 (bare-metal C).
- **PWM Strategy**: Center-aligned sine-wave modulation with 42-point Lookup table.
- **Power Electronics**: IGBT H-bridge, optocouplers.
- **User Interface**: 7-segment display + buttons for real-time frequency control.
- **Development Tools**: MPLAB X IDE, EasyEDA, Proteus, Oscilloscope validation.

All code written with emphasis on **minimal resource usage, reliability, and best practices**.

## Repository Structure
```bash
3-phase-vfd/
├── README.md
├── Hardware/
│   ├── Schematic.pdf
│   ├── Gerber/
│   ├── BOM.csv
│   └── Photos/
├── Firmware/
│   └── VariableFrequencyDrive.X/     # Full MPLAB X project
├── Media/
│   ├── Demo_Videos/
│   ├── Oscilloscope_Captures/
│   └── Build_Photos_GIFs/
└── Docs/
    └── Design_Notes_Calculations.pdf
```
## How to Use / Replicate
1. Clone the repo
2. Open `Firmware/VariableFrequencyDrive.X` in MPLAB X
3. Program the PIC16F18876
4. Build the power stage using the schematic + Gerbers
5. Connect a 3-phase motor and enjoy!

**Warning**: High voltage project — follow proper safety practices.

## Results & Impact
- Delivered perfect performance in one of the most demanding Power Electronics courses.
- Demonstrates end-to-end capability: firmware + power electronics + PCB design + integration.
- Directly relevant to industrial automation, motor control, and embedded systems roles.

---

**Connect with me**  
[LinkedIn](https://www.linkedin.com/in/enrique-mercader/) | [Personal Website](https://www.enrique-mercader.com) | [Resume](https://www.enrique-mercader.com/resume)
