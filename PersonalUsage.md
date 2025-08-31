# 🚗 ArduPilot for Autonomous Driving with ArduRover (SITL)

[![ArduPilot](https://img.shields.io/badge/ArduPilot-SITL-blue)](https://ardupilot.org/)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-green.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python](https://img.shields.io/badge/Python-3.8--3.10-yellow)](https://www.python.org/)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-20.04%20%7C%2022.04-orange)](https://ubuntu.com/)

## 📌 Overview

This project leverages **ArduPilot** to simulate **autonomous driving** using the **ArduRover** vehicle model.  
The simulation runs in **SITL (Software In The Loop)**, enabling development and testing without physical hardware.

📖 Reference: [ArduPilot Rover SITL Docs](https://ardupilot.org/rover/docs/rover-simulation.html)

## 🚀 Installation

Clone with submodules:

```bash
git clone --recursive https://github.com/ArduPilot/ardupilot.git
cd ardupilot
```

Install required dependencies:

```bash
Tools/environment_install/install-prereqs-ubuntu.sh -y
. ~/.profile
```

Build the ArduRover SITL target:

```bash
./waf configure --board sitl
./waf rover
```

---

## ▶️ Running SITL

Start the simulation with console and map:

```bash
./Tools/autotest/sim_vehicle.py -v ArduRover --console --map -w
```

Options:

-   `-v ArduRover` → specify the vehicle type
-   `--console` → opens MAVProxy console
-   `--map` → shows live map visualization
-   `-w` → wipes previous parameters for a clean run

---

## 🛠️ Modifications

_No personal modifications yet. Reserved for future updates._

---

## 📝 Notes

-   First build may take several minutes.
-   Ensure no conflicting Python environments.
-   For advanced simulation (Gazebo, AirSim integration, etc.), see [ArduPilot SITL Docs](https://ardupilot.org/dev/docs/sitl-simulator-software-in-the-loop.html).

## 📄 License

This project follows [GPLv3](https://www.gnu.org/licenses/gpl-3.0).

👨‍💻 Maintained by: **[anggamys](https://github.com/anggamys)**
💡 Contributions & pull requests are welcome!
