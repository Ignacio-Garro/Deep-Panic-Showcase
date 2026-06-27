# DEEP PANIC.

> A co-op submarine horror game built in Unity HDRP. Crew a deep-sea submarine with friends, manage failing systems, and survive what's lurking in the dark.

[![Steam](https://img.shields.io/badge/Steam-Wishlist-1b2838?logo=steam)](https://store.steampowered.com/app/3473920/Deep_Panic/)
[![Status](https://img.shields.io/badge/status-in%20development-orange)]()
[![Engine](https://img.shields.io/badge/Unity-HDRP-black?logo=unity)]()

> ⚠️ **Note:** This is a public showcase for a commercial game in active development. The source code is private. This repo documents the project, its engineering, and my role on it.

---

## About

**Pressure Inc.** is a 1–4 player co-op horror game where you and your crew operate a submarine in the crushing dark of the deep sea. Power, oxygen, navigation, and sensors all have to be managed by hand — and something outside the hull is paying attention. Built by a two-person indie studio, targeting **Steam Early Access (Nov 2026)** with an appearance at **Steam Next Fest (Oct 2026)**.

**Genre:** Co-op Horror · Submarine Sim
**Players:** 1–4 online co-op
**Engine:** Unity (HDRP)

🔗 **[Wishlist on Steam](https://store.steampowered.com/app/3473920/Deep_Panic/)** · [YouTube](https://www.youtube.com/@DeadWatersDev)

---

## 📸 Screenshots

<img width="1840" height="860" alt="capsule art2" src="https://github.com/user-attachments/assets/218b81bc-ff81-435b-b0a8-43dc49c1767d" />
<img width="883" height="883" alt="dead" src="https://github.com/user-attachments/assets/95a4a75f-bd0d-4acb-9959-8309f1b63e38" />
<img width="1920" height="1080" alt="Captura de pantalla 2026-01-26 235048" src="https://github.com/user-attachments/assets/752bc6ea-5f73-42e4-90cf-9cc4fe28af16" />
<img width="773" height="773" alt="minesroom" src="https://github.com/user-attachments/assets/e4bbafb3-f694-4d6b-a3cb-22bf6486bcd2" />


---

## 🛠️ Technical Highlights

The interesting part. As lead developer I designed and built the core engineering systems below.

### Rendering (HDRP)
- **Underwater rendering pipeline** — volumetric fog, light scattering, and depth-based desaturation to sell the pressure and darkness of the deep
- **Custom HDRP shaders** — triplanar mapping, alpha clipping, and Shader Graph materials for terrain, hull, and props
- **Security-camera night vision** and a **holographic map visualization** for in-world UI
- **Post-processing** — dynamic desaturation and a damage-overlay effect tied to ship/player state

### Simulation & Performance
- **GPU-instanced kelp and fish systems** driven by Unity's **Job System + Burst**, rendering large dense underwater environments while holding frame budget
- Data-oriented design to keep simulation off the main thread

### Audio
- **Steam Audio integration** for true 3D spatialized sound, including elevation cues — critical for locating threats and crewmates by ear in the dark

### Multiplayer
- **Online co-op netcode** Netcode for GameObjects synchronizing crew, ship state, and the submarine itself
- **Co-op submarine physics** — shared-control movement with tilt correction and collision-aware rotation so multiple players crewing one vessel feels stable

### Gameplay Systems
- **AI Director** — dynamic, tension-paced enemy spawning rather than fixed encounters
- **Proximity sensor system** feeding the sonar/alert loop
- End-of-game / results screen and supporting UI

---

## 👤 My Role — Lead Developer

I'm the lead developer and co-founder, responsible for the technical architecture and the majority of the engineering: rendering, performance-critical simulation, multiplayer, audio integration, and gameplay systems.

Roughly **1.5 years** of development to date.

---

## 🧰 Tech Stack

- **Engine:** Unity (HDRP)
- **Language:** C#
- **Multiplayer:** [Netcode for GameObjects / Fishnet]
- **Audio:** Steam Audio
- **Performance:** Job System, Burst Compiler, GPU instancing
- **Shaders:** Shader Graph, custom HLSL
- **Pipeline:** Blender, Substance Painter (3D asset workflow)
- **Platform:** Steam (PC)

---

## 🚀 Status & Roadmap

- ✅ Core systems: rendering, co-op netcode, submarine physics, AI Director
- 🔜 **Steam Next Fest** — October 2026
- 🎯 **Early Access launch** — November 17, 2026
