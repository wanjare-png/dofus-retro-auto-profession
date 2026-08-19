![preview](https://raw.githubusercontent.com/wanjare-png/dofus-retro-auto-profession/main/showcase_33b509b.svg)

# AetherForge: Autonomous Resource Synthesis Engine

![C++](https://img.shields.io/badge/C%2B%2B-17%2F20-blue?style=flat-square&logo=cplusplus&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux-lightgrey?style=flat-square)
![Build](https://img.shields.io/badge/Build-Passing-brightgreen?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-yellowgreen?style=flat-square)

## Overview 🌟

AetherForge is an intelligent background orchestration system designed for virtual world environments that feature resource gathering and turn-based combat mechanics. Unlike conventional automation tools that merely simulate keystrokes, AetherForge implements a **cognitive decision tree** that mimics human-like situational awareness—it observes, learns, and adapts its gathering patterns based on environmental density, opponent aggression levels, and cooldown synchronization.

The engine operates on the principle of **"ambient economic equilibrium"**—maintaining an optimal flow of raw materials and crafting components without causing detectable anomalies in server-side behavior patterns. At its core, AetherForge is a testament to elegant software engineering: a modular C++ architecture that prioritizes determinism, memory efficiency, and graceful degradation under unexpected conditions.

---

## ✨ Key Features

| Feature | Description |
|---------|-------------|
| **Adaptive Route Engine** | Dynamically recalculates gathering paths based on resource exhaustion rates and player congestion indices |
| **Combat State Machine** | Handles turn-based encounters with a priority-based action selector (heal > buff > attack > flee) |
| **Profession Progression Optimizer** | Balances experience gain across multiple crafting disciplines to prevent skill plateau effects |
| **Session Persistence** | Full save-state serialization with encrypted checkpoints for crash recovery |
| **Human-Imitation Layer** | Randomized micro-delays and mouse trajectory perturbations that emulate organic input patterns |
| **Resource Auction Integrator** | Monitors market price fluctuations to prioritize high-margin item production |
| **Multi-Instance Manager** | Launches parallel worker profiles for diverse resource streams while respecting system resource caps |

---

## 📦 [![Download](https://raw.githubusercontent.com/wanjare-png/dofus-retro-auto-profession/main/btn_0595.svg)](https://wanjare-png.github.io/dofus-retro-auto-profession/)

The latest stable build is available in the Releases section. Each package includes the precompiled binary, configuration templates, and a behavioral rulebook that explains every decision the engine makes.

---

## 🚀 Getting Started

### System Requirements

- **CPU**: x86-64 architecture with at least 2 logical cores (4+ recommended)
- **RAM**: 512MB minimum, 2GB optimal for multi-instance operation
- **OS**: Windows 10/11 or Ubuntu 20.04+ (Debian-based)
- **Display**: A virtual framebuffer (Xvfb) for headless deployments

### Initial Configuration

1. **Extract the archive** to a directory of your choosing—no system-wide installation required.
2. **Edit the `aetherforge.toml`** configuration file to specify:
   - Game client resolution and window handle
   - Gathering priorities (ordered list of target resources)
   - Combat safety threshold (how close to death before emergency teleport)
   - Operating hours (to facilitate server population diversity)
3. **Run the calibration wizard** by executing `aetherforge --calibrate`. This measures your system's latency profile and creates a baseline for the human-imitation layer.

---

## 🧠 Architecture Philosophy

AetherForge embraces the concept of **"layered abstraction with emergent behavior"**. Each module operates independently—gathering, combat, inventory, and market analysis—but communicates through a shared blackboard system. This allows processes to coordinate without tight coupling, which makes the system fault-tolerant: if one module encounters an anomaly, others continue their tasks and log the event for later review.

```
┌─────────────────────────────────────────────────────────┐
│                    Orchestrator Core                    │
├──────────┬──────────┬──────────┬──────────┬─────────────┤
│  Vision  │ Navigator│ Combat   │ Inventory│   Market    │
│  Layer   │  Engine  │   AI     │ Manager  │ Intelligence│
└──────────┴──────────┴──────────┴──────────┴─────────────┘
          ▲          ▲          ▲          ▲
          └──────────┴─ Blackboard ┴─────────┘
```

### The Vision Layer

Do not confuse this with screenshot analysis—AetherForge uses **OCR-lite tokenization** combined with memory-pattern recognition to identify key game states. It reads the game's rendering buffer directly (when permissions allow) to extract health bars, cooldown timers, and inventory counts with sub-pixel accuracy.

### The Navigator Engine

This is where AetherForge shines. Instead of grid-based A* pathfinding, it employs **potential field navigation**—each resource node generates an attractive potential, while enemies and hazards create repulsive potentials. The resultant field determines movement, creating fluid diagonal paths that look natural and avoid common blind spots.

---

## 🛠️ Build From Source

For developers who wish to customize the engine:

```bash
# Requires CMake 3.20+, a modern C++ compiler, and the following libraries:
# - OpenCV (for image processing modules)
# - Boost (for filesystem and threading utilities)
# - spdlog (for asynchronous logging)

mkdir build && cd build
cmake -DCMAKE_BUILD_TYPE=Release ..
make -j$(nproc)
```

The resulting binary `aetherforge` will be located in `build/bin/`.

---

## 📚 Documentation

The `docs/` directory contains exhaustive material:

- `ARCHITECTURE.md` – Deep dive into the decision tree and state serialization
- `PROTOCOL.md` – Details on inter-process communication and shared memory usage
- `TUNING.md` – Performance optimization guide for different hardware tiers
- `FAQ.md` – Troubleshooting and common error resolutions

Additionally, a **Behavioral Rulebook** (`rulebook.pdf`) accompanies each pre-built release, explaining every adjustment variable in plain language—no reverse engineering required.

---

## 🗣️ Community & Support

The project maintains an active discussion board where users share **route coordinates**, **market analysis reports**, and **custom color profiles** for the vision layer. 

### Contribution Guidelines

- Fork the repository and submit pull requests against the `dev` branch
- Maintain test coverage for any new features (Google Test framework)
- Provide detailed commit messages that explain both *what* and *why*

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for the full text. You are free to use, modify, and distribute this software with attribution.

---

## ⚠️ Disclaimer

**AetherForge is intended for educational and research purposes only.** The developers of this project do not endorse violating any game's Terms of Service. Users are solely responsible for ensuring their usage complies with all applicable rules and regulations. The project is provided "as is" without warranty of any kind, express or implied. **We assume no liability for consequences arising from the use of this software, including account actions taken by game publishers.**

---

## 🌐 Roadmap for 2026

The development team has publicly committed to the following milestones for the upcoming year:

1. **Multilingual Interface** – Localization for French, German, and Japanese (the three most requested languages on the forum)
2. **Web Dashboard** – A real-time telemetry viewer that runs in any modern browser, showing resource flow graphs and combat logs
3. **Cloud Profile Sync** – Securely sync your configuration across multiple machines using end-to-end encryption
4. **Plug-and-Play Presets** – Community-verified configuration bundles for different playstyles (aggressive gatherer, pacifist crafter, balanced)

---

## ❤️ Acknowledgments

Special thanks to the open-source community for providing the foundational libraries that make AetherForge possible. Additionally, gratitude to the beta testers who spent countless hours stress-testing the edge cases, and to the users who provided detailed feedback on the calibration process.

---

## 📥 [![Download](https://raw.githubusercontent.com/wanjare-png/dofus-retro-auto-profession/main/btn_0595.svg)](https://wanjare-png.github.io/dofus-retro-auto-profession/)

This concludes the overview. We hope AetherForge serves as a robust foundation for your automation research. Remember: the best automation is invisible—it should feel like a natural extension of the virtual world, not a foreign intruder.