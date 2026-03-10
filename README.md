
#  Analog Voice-Over Circuit with Dual-Mode Functionality

This project demonstrates a fully analog implementation of a Voice-Over (Ducking) Circuit designed for efficient audio channel management. This specific version utilizes a streamlined approach focusing on amplitude detection without complex filtering, allowing for a robust and high-gain audio response.

 ## Key Features

### 🔄 Dual-Mode Priority Selection Toggle between a Direct Mic Mode for live announcements and a Recorded Playback Mode for pre-recorded loops or voices.

### 🎯 Channel Prioritization Automatically prioritizes the selected voice channel when an input is detected, ensuring background audio "ducks" seamlessly.

### ⚖️ Detection Threshold Adjustable detection threshold using the LM358 comparator to ensure precise activation based on voice intensity.

### 🔌 Purely Analog Design Developed entirely using basic analog components and ICs (LM386 & LM358), ensuring zero-latency signal processing without the need for microcontrollers or band-pass filters.

## ⚙️ Functionality

🔰 Input Mode Selection The signal path begins at the mode selector switch. This allows the user to choose the priority source: either a Direct Microphone signal or a Recorded Voice module, making the system versatile for both live and automated environments.

🔰 Pre-Amplifier (LM386) The selected voice signal is fed to an LM386 IC configured as a high-gain pre-amplifier. It boosts low-level signals to a level suitable for analysis by the subsequent control circuitry.

🔰 Peak Detector (LM358) One half of the LM358 Dual Op-Amp captures the amplitude of the voice signal. Using a specific RC timing constant ($R = 47k\Omega$ and $C = 10\mu F$), it provides a stable DC output that manages the "ducking" release time.

🔰 Comparator (LM358) The second half of the LM358 compares the peak value against a predetermined threshold set by a $10k\Omega$ potentiometer. It produces a high output when speech surpasses this threshold.

🔰 Switching & Mixing The comparator's output serves as the control signal to attenuate the background music channel instantly, allowing the priority voice channel to dominate the mix.

🔰 Main Amplifier (LM386) The final prioritized audio signal is amplified by the main LM386 power stage to drive an $8\Omega$ speaker clearly through a $220\mu F$ coupling capacitor.

## 🛠️ Components & ICs

LM386 (x2): Used for both High-gain Pre-amplifier and Main Power Amplifier stages.

LM358: Used for Precision Peak Detection and Comparator logic.

RC Timing: $47k\Omega$ resistor and $10\mu F$ capacitor for ducking decay control.

Selector: SPDT Switch for Mode selection (Mic vs. Recorded).

Coupling: $470\mu F$ speaker output capacitor.

🖼️ Visuals of the Project

<div style="display: flex; gap: 15px; justify-content: center; flex-wrap: wrap;">

<!-- PCB -->

<div style="text-align: center;">
<img src="https://github.com/gunasekaraks/Analog-Voice-Over-circuit/blob/main/SCHEMATIC.jpeg" width="220"/>
<div><strong>SCHEMATIC</strong></div>
</div>

<!-- Product Image 1 -->
<div style="text-align: center;">
<img src="https://github.com/gunasekaraks/Analog-Voice-Over-circuit/blob/main/SINGLE%20LAYER%20PCB.jpeg" width="220"/>
<div><strong>SINGLE LAYER PCB</strong></div>
</div>

<div style="text-align: center;">
<img src="https://github.com/banula33/ANALOG-VOICE-OVER-CIRCUIT/blob/main/MULTILAYER%20PCB.jpeg" width="220"/>
<div><strong>MULTI LAYER PCB</strong></div>
</div>

<div style="text-align: center;">
<img src="https://github.com/gunasekaraks/Analog-Voice-Over-circuit/blob/main/ENCLOSURE.jpeg" width="220"/>
<div><strong>ENCLOSURE</strong></div>
</div>

<div style="text-align: center;">
<img src="https://github.com/banula33/ANALOG-VOICE-OVER-CIRCUIT/blob/main/FINAL%20PRODUCT.jpeg" width="220"/>
<div><strong>FINAL PRODUCT</strong></div>
</div>

<div style="text-align: center;">
<img src="https://github.com/gunasekaraks/Analog-Voice-Over-circuit/blob/main/PROTOTYPE.jpeg" width="220"/>
<div><strong>PROTOTYPE</strong></div>
</div>
<!-- Product Image 2 + 3 combined -->


<!-- Signal Flow Diagram -->

<div style="text-align: center; margin-top: 30px;">
<img src="https://github.com/gunasekaraks/Analog-Voice-Over-circuit/blob/main/LOGIC.jpeg" width="500"/>
<div><strong>Signal Flow Diagram</strong></div>
</div>

🎓 What We Learn

Analog Signal Processing: Designing high-gain amplifiers and precision comparators.

Audio Channel Management: Handling transitions between multiple sources based on real-time amplitude detection.

Practical Circuit Integration: Merging disparate analog modules into a cohesive, functional unit.


Specializing in Analog Systems and Circuit Design

Feel free to fork this repository and contribute to further improvements!
