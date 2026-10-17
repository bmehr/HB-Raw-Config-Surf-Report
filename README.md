# HB Raw Config Surf 🏄‍♂️
### Local Ground-Truth Telemetry & Shore Operations · In Memory of Rick "Rockin' Fig" Fignetti (1955–2021)

HB Raw Config Surf is an unvarnished progressive web application built for Huntington Beach locals. By merging real-time physical ocean sensor telemetry (CDIP Buoys, NOAA Tides, Open-Meteo) with ground-truth field dispatches submitted directly by trusted surfers on the sand, it provides an authentic look at the shoreline without commercial tourist spin.

---

## ⚡ Core Features

- **Ground Truth Shore Dispatches:** Surfers on the sand log observed wave heights, shape, and reality notes. The freshest report of the day for each break is automatically elevated to the **Featured Hero Card**.
- **Spot-Isolated Shore Log:** Choose between **South HB**, **The Pier**, **North HB**, and **Bolsa Chica**. The lower feed isolates dispatches for that specific break and de-duplicates the active Hero post so the same report is never duplicated on screen.
- **The "Fig-O-Matic" Local Handle Generator:** Tap the shuffle die (🎲) to generate authentic local beach handles, or enter and persist your own custom nickname.
- **Dynamic Rockin' Fig Voice Engine:** When a break awaits a fresh community scout, the system synthesizes daily commentary matching Rockin' Fig's iconic style, directly reacting to live wind heading, swell period, and tidal state.
- **Animated Coastline Wind Visualizer:** Calibrated to Huntington Beach's $215^\circ$ Southwest coastal angle, differentiating offshore Santa Ana grooming from onshore side-chop with live vector animation.
- **Hot/Cold Data Management Tier:** Live operations run on a rolling 30-day window to keep mobile loading fast and protect Firestore free-tier quotas, with permanent cold-storage export hooks for future historical modeling.
- **Exclusive Invite Flow ("Pass the Wire"):** Share an authentic invite link via SMS/WhatsApp with trusted locals who contribute real eyes to the sand.
- **PWA & Android History Trap:** Built-in home screen installation support with an Android `popstate` back-button trap that prevents iframe redirects.

---

## 🌊 Telemetry Sources

1. **Offshore Swell:** CDIP 092 (San Pedro Channel) & Open-Meteo Marine API.
2. **Harmonic Tides:** NOAA CO-OPS Station 9410580 (Newport Beach / HB Entrance) running 6-hour predictive curves.
3. **Water Temperature:** Physical temperature sensor at NOAA Station 9410580.
4. **Nearshore Aerology:** 10m coastal meteorological stations computing wind vectors against HB's coastline angle.

---

## 🔒 Firestore Security

The app runs on strict server-side Firestore security rules:
- Public read access for community dispatches.
- Strict create-only constraints (size-capped text, handle length limits, Base64 payload limits under ~500 KB).
- Client-side updates and deletions are disabled to prevent data tampering.
- 3-minute anti-spam cooldown per device using `localStorage`.

---

## 🏄 "Direct telemetry verified by local eyes on the sand."