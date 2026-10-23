1. \# 🚗⚡ L298N Motor Driver (KiCad)

# 

# A motor driver board designed in \*\*KiCad\*\* around the \*\*L298N dual H-bridge\*\* driver. Use it to control the speed and direction of DC motors from a microcontroller such as an ESP32 or Arduino. 🤖

# 

# \---

# 

# \## 📸 Screenshots

# 

# Screenshots of the schematic, PCB layout and 3D view are in the \[`screenshots`](screenshots/) folder.

# 

# \---

# 

# \## ✨ Features

# 

# \- 🔄 Dual H-bridge: drive \*\*two DC motors\*\* independently

# \- ↔️ Forward / reverse control for each motor

# \- 🎚️ Speed control using PWM on the enable pins

# \- 🔌 Screw terminals or headers for power and motor outputs

# \- 🧠 Logic-level inputs for a microcontroller

# 

# > ✏️ Edit this list to match what your board actually includes.

# 

# \---

# 

# \## 📁 Repository Structure

# 

# ```

# Motor\_Driver\_Kicad/

# ├── L298N\_design/

# │   ├── L298N\_design.kicad\_pro   🗂️ KiCad project file

# │   ├── L298N\_design.kicad\_sch   📐 Schematic

# │   └── L298N\_design.kicad\_pcb   🟩 PCB layout

# ├── screenshots/                 🖼️ Images of the design

# ├── .gitignore

# └── README.md

# ```

# 

# \---

# 

# \## 🛠️ Tools Used

# 

# | Tool | Purpose |

# |------|---------|

# | 🧰 KiCad | Schematic capture and PCB design |

# | 🌱 Git \& GitHub | Version control |

# 

# \---

# 

# \## 🚀 How to Open the Project

# 

# 1\. 📥 Clone the repository:

# &#x20;  ```bash

# &#x20;  git clone https://github.com/Shubhampoddar960/Motor\_Driver\_Kicad.git

# &#x20;  ```

# 2\. 📂 Open KiCad and choose \*\*File → Open Project\*\*.

# 3\. 🗂️ Select `L298N\_design/L298N\_design.kicad\_pro`.

# 4\. 👀 Open the schematic or PCB editor from the project window.

# 

# \---

# 

# \## 🔌 Pin Connections

# 

# | Signal | Description |

# |--------|-------------|

# | `IN1`, `IN2` | 🔁 Direction control for Motor A |

# | `IN3`, `IN4` | 🔁 Direction control for Motor B |

# | `ENA`, `ENB` | 🎚️ PWM speed control for Motors A and B |

# | `VS` | 🔋 Motor supply voltage |

# | `GND` | ⏚ Common ground |

# | `OUT1`–`OUT4` | ⚙️ Motor outputs |

# 

# > ✏️ Adjust the names to match the labels in your schematic.

# 

# \---

# 

# \## ⚠️ Notes

# 

# \- 🔥 The L298N drops about 2 V per bridge and can get hot, so add a heatsink for higher currents.

# \- 🔗 Always connect the microcontroller ground to the driver ground.

# \- 🧪 Check the design carefully before ordering or manufacturing a PCB.

# 

# \---

# 

# \## 🗺️ Future Improvements

# 

# \- \[ ] 🧩 Add a 3D model preview

# \- \[ ] 📦 Export Gerber files

# \- \[ ] 💡 Add status LEDs

# \- \[ ] 🛡️ Add protection circuitry

# 

# \---

# 

# \## 👤 Author

# 

# \*\*Shubham Poddar\*\*

# 🔗 GitHub: \[@Shubhampoddar960](https://github.com/Shubhampoddar960)

# 

# \---

# 

# \## 📄 License

# 

# No license has been added yet. 📝 Add one if you want others to reuse or modify the design.

# 

# \---

# 

# ⭐ If you find this project useful, consider giving it a star!

#-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
#-----------------------------------------------------------------------------------------------------------------------------------------------------------------|

2. ⚙️ TB6612FNG Motor Driver Board

A compact dual DC motor driver board designed in **KiCad**, built around the **TB6612FNG** driver IC. It includes reverse polarity protection and proper supply filtering, which makes it a good fit for robotics projects such as line followers and small robots. 🤖

---

## ✨ Features

- 🔌 Drives **2 DC motors** independently (Channel A and Channel B)
- 🛡️ **Reverse polarity protection** using a PMOS (Q1)
- 🔋 Motor supply filtering (10 µF + 0.1 µF)
- 🧠 Logic supply decoupling (0.1 µF)
- 🌍 Large **GND copper pour** for good return paths and noise reduction
- 📌 Simple headers: one for signals, one for power and motors
- 🔄 Standby (STBY) pin to put the driver to sleep and save power

---

## 🧩 Specifications (TB6612FNG)

| Parameter | Value |
|---|---|
| ⚡ Motor supply (VMOT) | 4.5 V – 13.5 V |
| 🧠 Logic supply (VCC) | 2.7 V – 5.5 V |
| 🔁 Continuous current per channel | 1.2 A (3.2 A peak) |
| 🎚️ PWM frequency | Up to 100 kHz |

---

## 📌 Pinout

### 🔹 J1 – Signal Header (7 pins)

| Pin | Signal | Description |
|---|---|---|
| 1 | AIN1 | Motor A direction input 1 |
| 2 | AIN2 | Motor A direction input 2 |
| 3 | PWMA | Motor A speed (PWM) |
| 4 | BIN1 | Motor B direction input 1 |
| 5 | BIN2 | Motor B direction input 2 |
| 6 | PWMB | Motor B speed (PWM) |
| 7 | STBY | Standby (HIGH = enabled) |

### 🔹 J2 – Power & Motor Header (7 pins)

| Pin | Signal | Description |
|---|---|---|
| 1 | VMOT | Battery / motor
