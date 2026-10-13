# 🏄‍♂️ HB Raw Config Surf Report

> **Hyper-local, ground-truth surf intelligence for Huntington Beach, California.**  
> *From the Santa Ana River Jetties to Sunset Beach — real eyes on the sand, not proprietary algorithmic guesses.*

🔗 **Live Report Dashboard:** [👉 Launch Live Web App Here](https://bmehr.github.io/HB-Raw-Config-Surf-Report/) 

---

## 🕊️ Dedicated to Rick "Rockin' Fig" Fignetti (1955–2021)

> *"Check the waves with your own eyes — not an algorithm."*

For decades on KROQ 106.7 FM, at his surf shop on Main Street, and on the mic at local surf contests, Rick "Rockin' Fig" Fignetti was the heartbeat and voice of Surf City. He did what automated models will never be able to do: he drove down before dawn, checked the tide, watched the sets, and gave surfers the genuine truth without the hype.

**HB Raw Config** is built in that exact spirit: keeping Huntington Beach surf reporting raw, honest, local, and community-driven.

---

## 🎯 The Problem We're Solving

Mainstream surf forecasting platforms (like Surfline) rely heavily on macro-scale proprietary models (LOTUS). While useful offshore, they routinely miss ground-level Orange County realities:

- **Overhyped Face Sizes:** Labeling 2–3ft closed-out slop as "Fair to Good 4–5ft."
- **Bathymetry Blindspots:** Missing how high tide backwash ruins inside banks or how subtle sandbars hold punchy corners.
- **Micro-Climate Wind Shifts:** Failing to recognize when the cliffs bluff at Goldenwest provides offshore shelter while the Pier is already blown out.
- **Stale Updates:** Delivering an automated dawn forecast that sits unchanged even when conditions drastically improve mid-day or late morning.

**HB Raw Config** flips the script: combining **unfiltered open marine telemetry** with **first-hand shore observations and community photos**.

---

## 📍 Calibrated Shoreline Zones (8.5 Miles)

Instead of a generic single "Huntington Beach" rating, the shoreline is divided into five distinct micro-zones:

| Zone | Stretch | Characteristics & Bathymetry |
| :--- | :--- | :--- |
| **Zone 01** | **River Jetties / Brookhurst** | Mixed cobblestone and sandbar rivermouth; sensitive to S/SW angles and lower tide drains. |
| **Zone 02** | **HB Pier (North & South)** | Pilings refraction, steep bowls, heavy rip currents, and structural bounce wedges. |
| **Zone 03** ⭐ | **17th St ⇄ Bolsa Jetty** *(Core Focus)* | Goldenwest, 19th St, Dog Beach & Cliffs bluff. Sheltered wind pocket, outside bar A-frames, and prime mid-day push windows. |
| **Zone 04** | **Bolsa Chica State Beach** | Flatter shelf bathymetry; mellow rollers ideal for fishes, logs, and twin-fins. |
| **Zone 05** | **Sunset Beach (Anderson St to Warner)** | Proximity to deepwater trench; heavy shorebreak slams and pitching closeouts. |

---

## ✨ Features & Architecture

- **🌊 Dynamic Hyper-Zone Inspection:** Click any zone card to reconfigure the entire dashboard to that spot's bathymetry, swell angle sensitivity, and sweet-spot tide window.
- **🛰️ Live Open Marine Telemetry:** Direct API streams pulling swell height, period, direction, sea surface temperature, and wind speed/gusts calibrated directly to HB coordinates (`33.6595° N, -117.9988° W`).
- **📸 In-Browser Photo Compression:** Mobile field photos are resized and compressed on the fly (via HTML5 Canvas) to ~150KB–250KB before upload, keeping the app lighting fast and lightweight.
- **✍️ Flexible Wave Descriptors:** Preset shapes (*Peaky A-Frames, Walled-Out Closeouts, Mushy Bog*) plus a **custom field note** option (with real-time word/character limiters) for nuanced descriptions like *"Walled, but corners there for the taking."*
- **⭐ Promote to Hero:** Select and promote the most accurate shore dispatch and visual into the featured **Daily Hero** spotlight.
- **⚡ Zero-Dependency SPA:** 100% vanilla JavaScript, HTML5, and Tailwind CSS. No `node_modules`, no build steps, and zero hosting costs.

---

## 🚀 Quick Setup & GitHub Pages Deployment

### 1. Clone the repository
```bash
git clone [https://github.com/YOUR-USERNAME/hb-raw-config-surf-report.git](https://github.com/YOUR-USERNAME/hb-raw-config-surf-report.git)
cd hb-raw-config-surf-report
