<div align="center">

# Sebastian Velandia

**Electronics engineer in Bogotá, Colombia**<br>
Simulation, validation and data tools for space and rocketry.

<p>
  <img src="https://img.shields.io/badge/Godot_4.6-478CBF?style=flat-square&logo=godotengine&logoColor=white" alt="Godot">
  <img src="https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white" alt="C#">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" alt="Java">
  <img src="https://img.shields.io/badge/Svelte-FF3E00?style=flat-square&logo=svelte&logoColor=white" alt="Svelte">
  <img src="https://img.shields.io/badge/MCP-000000?style=flat-square&logo=anthropic&logoColor=white" alt="MCP">
</p>

<p>
  <a href="#-exosphere">Exosphere</a> ·
  <a href="#-breathing-comets">Breathing Comets</a> ·
  <a href="#-open-source-openrocket">OpenRocket</a> ·
  <a href="#-aladin-mcp">Aladin MCP</a> ·
  <a href="#-more">More</a>
</p>

</div>

---

## 🚀 Exosphere

A space-mission simulator in **Godot 4.6 and C#**. You fly the starship vehicle from the pad through ascent, orbit, and reentry, in a double-precision model of the solar system.

<p>
  <a href="https://github.com/sebastianvelace/Exosphere"><img src="assets/starship-liftoff.png" width="49%" alt="Starship Flight 12 lifting off Starbase in Exosphere"></a>
  <a href="https://github.com/sebastianvelace/Exosphere"><img src="assets/apollo11-liftoff.png" width="49%" alt="Apollo 11's Saturn V lifting off in Exosphere"></a>
</p>

<p>
  <a href="https://github.com/sebastianvelace/Exosphere"><img src="https://github.com/sebastianvelace/Exosphere/raw/main/docs/screenshots/orbit.png" width="24%" alt="Starship in low Earth orbit"></a>
  <a href="https://github.com/sebastianvelace/Exosphere"><img src="https://github.com/sebastianvelace/Exosphere/raw/main/docs/screenshots/entry.png" width="24%" alt="Starship in aerodynamic descent"></a>
  <a href="https://github.com/sebastianvelace/Exosphere"><img src="https://github.com/sebastianvelace/Exosphere/raw/main/docs/screenshots/landing-burn.png" width="24%" alt="Starship landing burn over the ocean"></a>
  <a href="https://github.com/sebastianvelace/Exosphere"><img src="https://github.com/sebastianvelace/Exosphere/raw/main/docs/screenshots/cockpit.png" width="24%" alt="Cockpit view in low orbit"></a>
</p>

Sandbox flight from Starbase, prepared scenarios, a historical campaign from Mercury to Apollo 11, and a vehicle assembly building all use the same physics. MIT licensed. [Source](https://github.com/sebastianvelace/Exosphere).

---

## 🌠 Breathing Comets

**[breathingcomets.org](https://breathingcomets.org)** · [source](https://github.com/sebastianvelace/Breathing-Comets) · English and Spanish

NASA's SPHEREx maps the whole sky in 102 infrared colors. Breathing Comets turns that public data into something you can touch: play real exposures, blink two dates, subtract the sky at matched wavelengths, and click any position for a measured spectrum. Then follow the same data to comets that exhale CO₂ and to near-Earth asteroids sized after NEOWISE.

<p>
  <a href="https://breathingcomets.org"><img src="assets/bc-landing.jpg" width="49%" alt="Breathing Comets landing page with real SPHEREx frames of comet 3I/ATLAS"></a>
  <a href="https://breathingcomets.org"><img src="assets/bc-barnard.jpg" width="49%" alt="Difference image isolating the proper motion of Barnard's Star in SPHEREx data"></a>
</p>

- **Measured, not illustrated.** Spectra come from real SPHEREx frames, with the provenance and the downloadable stack on each comet page.
- **Checked against the literature.** The 3I/ATLAS CO₂ production rate falls inside the published range, and the page says so.
- **Honest about limits.** Systematics and saturated cores are flagged on the page instead of hidden.

---

## 🔧 Open source: OpenRocket

Two merged pull requests to [OpenRocket](https://github.com/openrocket/openrocket), the open-source model rocket simulator (3k+ stars).

| PR | What it fixes |
|---|---|
| [#3189](https://github.com/openrocket/openrocket/pull/3189) | Wind models now take the simulation's random seed, so flights with turbulence are reproducible. ([#3188](https://github.com/openrocket/openrocket/issues/3188)) |
| [#3190](https://github.com/openrocket/openrocket/pull/3190) | Tumbling is detected from a *sustained* angle of attack measured against the rocket's own pitch period, not an instantaneous one. ([#3183](https://github.com/openrocket/openrocket/issues/3183)) |

**Investigation: [issue #2489](https://github.com/sebastianvelace/openrocket-2489-weathercock).** In strong wind, OpenRocket's simulated weathercocking stops growing and can reverse sign, while RASAero II keeps growing. The write-up traces it to the body crossflow term: its coefficient (K = 1.1) is the value for an infinitely long cylinder, but the reference method it comes from scales it down for finite-length bodies. Confirmed three independent ways, including a stand-alone simulator that reproduces OpenRocket within 1–4 %.

<p align="center">
  <a href="https://github.com/sebastianvelace/openrocket-2489-weathercock"><img src="assets/openrocket-weathercock.png" width="80%" alt="Upwind distance at apogee versus wind speed for RASAero II and OpenRocket"></a>
</p>

---

## 🔭 Aladin MCP

**[aladin-mcp](https://github.com/sebastianvelace/aladin-mcp)** is an MCP server that lets Claude work with the CDS ecosystem in Strasbourg: **SIMBAD**, **VizieR**, **HiPS** survey images and **Aladin Desktop** over SAMP. Seven tools, from object lookups to color-magnitude diagrams. It was built for an astronomy workshop on the Large Magellanic Cloud and the open cluster NGC 4755.

<p>
  <a href="https://github.com/sebastianvelace/aladin-mcp"><img src="assets/aladin-ngc4755.jpg" width="49%" alt="NGC 4755 in DSS2 red with its bright stars identified in Aladin"></a>
  <a href="https://github.com/sebastianvelace/aladin-mcp"><img src="assets/aladin-cmd.jpg" width="35%" alt="Color-magnitude diagram of NGC 4755 built from Gaia DR3"></a>
</p>

---

## 📦 More

- [**rocketry-engineering**](https://github.com/sebastianvelace/rocketry-engineering): an end-to-end experimental rocketry effort covering propulsion, structures, hardware testing and data acquisition.
- [**Rocky**](https://github.com/sebastianvelace/Rocky): a local-intelligence kernel for Linux (Tauri/Rust, FastAPI, Next.js).
- [**kicad-circuit-ai**](https://github.com/sebastianvelace/kicad-circuit-ai): a circuit intelligence layer for KiCad that finds logic errors ERC/DRC cannot see.

<div align="center">

<sub>Ordinary people can choose to be extraordinary.</sub>

</div>
