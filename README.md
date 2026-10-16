# HB Raw Config Surf

> Dedicated to the memory of Rick "Rockin' Fig" Fignetti (1955–2021)  
> *"Check the waves with your own eyes — not an algorithm!"*

A private, invite-circle progressive web application delivering unvarnished, community-grounded surf observations and real-time physical ocean telemetry for Huntington Beach, California.

---

## 🌊 Core Philosophy

Commercial surf forecast platforms lean heavily on offshore model algorithms that frequently miss local sandbar bathymetry, piling refraction, and bluff sheltering. **HB Raw Config Surf** pairs raw physical sensor telemetry with timely, first-person morning shore dispatches logged by trusted local surfers on the sand.

---

## 📍 Huntington Beach Geographic Zones

The dashboard breaks Surf City down into four distinct zones from south to north:

| # | Zone | Coverage | Typical Swell Profile |
|---|---|---|---|
| **01** | **South HB** | State Beach, Brookhurst, Magnolia down to River Jetties | Funnels S/SSW groundswell directly; dredges steep wedges over cobblestone shelves on lower tides. |
| **02** | **The Pier** | Pier South Side (Piling Wedge) & North Side (Pier Bowl) | Piling deflection generates steep launch ramps on the south side; peaky lefts toward 6th St on the north. |
| **03** | **North HB** | Streets North of Pier, 17th St, Goldenwest & The Cliffs | Classic sandbar A-frames; bluffs provide natural shelter during light mid-day seabreezes. |
| **04** | **Bolsa Chica** | Seapoint Area to North Parking Lot | Gentle bathymetry creates peeling rollers tailored for single-fins and mid-lengths. |

---

## 🛠 Tech Stack & Architecture

- **Frontend:** Single-page architecture (`index.html`) styled with Tailwind CSS via CDN.
- **Typography:** Google Fonts (`Plus Jakarta Sans` for UI, `JetBrains Mono` for telemetry instruments).
- **Backend / Database:** Firebase Firestore real-time listener syncing community reports across devices.
- **Image Processing:** Client-side Canvas downscaling & compression with in-browser iPhone HEIC/HEIF conversion (`heic2any`).
- **Telemetry Feeds:**
  - *Swell / Wave Height:* Open-Meteo Marine API.
  - *Wind & Gusts:* Open-Meteo Weather API (converted to knots & compass bearings).
  - *Live Water Temp & Tide:* NOAA CO-OPS Physical Gauges (Stations 9410660 & 9410580).
- **Progressive Web App (PWA):** Standalone app manifest, crisp vector rendering, and iOS/Android home screen launch capability.

---

## 📱 Local Development Workflow

1. Open the project folder in **VS Code**.
2. Launch a local web server using the **Live Server** extension (right-click `index.html` $\rightarrow$ *Open with Live Server*).
3. Test changes locally across desktop and mobile screen dimensions before pushing to GitHub:
   ```bash
   git add .
   git commit -m "Update feature"
   git push origin main