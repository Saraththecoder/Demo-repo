<div align="center">

# 🔬 LabSim

### Interactive Virtual Science Laboratory

**Explore school-level Physics and Chemistry through browser-based 3D experiments, guided explanations, and circuit simulations.**

[![Platform](https://img.shields.io/badge/Platform-Web-2563EB?style=for-the-badge)](#)
[![3D](https://img.shields.io/badge/3D-Three.js-111111?style=for-the-badge&logo=threedotjs)](#)
[![Framework](https://img.shields.io/badge/Framework-Next.js-000000?style=for-the-badge&logo=nextdotjs)](#)
[![Language](https://img.shields.io/badge/Language-TypeScript-3178C6?style=for-the-badge&logo=typescript)](#)
[![License](https://img.shields.io/badge/License-MIT-22C55E?style=for-the-badge)](LICENSE)

[Experiments](#-experiments) ·
[Features](#-features) ·
[Installation](#-getting-started) ·
[Architecture](#-architecture) ·
[Roadmap](#-roadmap)

</div>

---

## 📌 Overview

**LabSim** is a browser-based virtual laboratory designed to help secondary and senior-secondary students understand science concepts through interactive 3D visualisations, adjustable experiment parameters, guided explanations, and viva-preparation support.

It is intended to **complement classroom teaching and supervised practical work**, not replace hands-on laboratory learning.

> ⚠️ **Note:** LabSim is an academic and development project. Experiment availability, device compatibility, and scientific accuracy should be verified against the current build before classroom use.

---

## 🧪 Experiments

### Physics

| Experiment | Learning Focus | Status |
|---|---|:---:|
| 🔎 Convex Lens | Focal length and image formation | 🚧 In progress |
| 🪞 Concave Mirror | Real and virtual image formation | 🚧 In progress |
| 🔌 Ohm’s Law | Voltage, current, and resistance | 🚧 In progress |
| 🌈 Glass Prism | Refraction and dispersion | 🚧 In progress |
| 📐 Glass Slab | Refraction and lateral displacement | 🚧 In progress |
| 🧰 Circuit Sandbox | Building and exploring circuits | 🚧 In progress |

### Chemistry

| Experiment | Learning Focus | Status |
|---|---|:---:|
| ⚡ Electrolytic Conductivity | Ions, electrodes, and conductivity | 🚧 In progress |
| 🧪 Acids, Bases & Indicators | Indicator colour changes | 🚧 In progress |
| 🧲 Metal Displacement | Iron and copper sulphate reaction | 🚧 In progress |

> Replace 🚧 with ✅ once an experiment is complete and scientifically validated.

---

## 🖼️ Screenshots

> Add real screenshots to `docs/images/` and update the paths below.

<div align="center">

| 3D Laboratory | Circuit Sandbox |
|:---:|:---:|
| ![LabSim 3D Laboratory](docs/images/lab-preview.png) | ![LabSim Circuit Sandbox](docs/images/circuit-sandbox.png) |

</div>

---

## ✨ Features

- 🧊 **Interactive 3D visualisation** — explore experiment setups and adjust supported parameters.
- 🎓 **Guided viva preparation** — review experiment tips, sample questions, and explanations.
- ⚡ **Circuit sandbox** — build circuits and observe simulated current behaviour.
- 📝 **Observation workflow** — record observations and generate printable reports.
- 🌐 **Browser-first access** — works in modern browsers with WebGL support.
- 🎙️ **Voice assistance** — optional speech output using the Web Speech API.
- 📱 **Responsive interface** — designed for desktop and supported mobile browsers.

### Important Limitations

- Simulations are educational models, not substitutes for physical measurements or laboratory safety training.
- WebXR/AR availability depends on the browser, operating system, and device.
- Voice output depends on browser speech support and device settings.
- Offline access works only for features and assets explicitly cached for offline use.

---

## 🧱 Technology Stack

| Layer | Technologies |
|---|---|
| Web application | Next.js, React, TypeScript |
| 3D rendering | Three.js, WebGL |
| Spatial experience | WebXR Device API, where supported |
| UI and styling | Tailwind CSS, Lucide Icons, GSAP |
| Validation and storage | Zod, Browser LocalStorage |
| Voice and audio | Web Speech API, Web Audio API |
| Scientific models | Custom TypeScript modules |

> Use `package.json` and the lockfile as the source of truth for installed dependency versions.

---

## 🏗️ Architecture

```mermaid
flowchart TD
    A[Student in Browser] --> B[Next.js / React Interface]
    B --> C[Three.js Experiment Scenes]
    B --> D[Experiment Controls]
    D --> E[TypeScript Science Models]
    E --> C
    B --> F[Guided Viva and Audio]
    B --> G[Observation Ledger and Reports]
```

Scientific calculations are kept separate from rendering logic wherever possible. This makes equations easier to test independently of the 3D interface.

---

## 🚀 Getting Started

### Prerequisites

- Node.js — use a version supported by the project’s Next.js release
- npm, pnpm, or the package manager indicated by the repository lockfile
- A modern browser with WebGL enabled

### Install and Run

```bash
git clone [https://github.com/Saraththecoder/labsim.git](https://github.com/Saraththecoder/labsim.git)
cd labsim
npm install
npm run dev
```

Then open the local URL shown in your terminal, usually:

```text
http://localhost:3000
```

### Production Build

```bash
npm run build
npm run start
```

### Environment Variables

If an optional service requires an API key, document the variable name in `.env.example`.

Never commit real API keys, tokens, passwords, or personal credentials.

---

## 📁 Project Structure

```text
labsim/
├── public/                  # Static assets
├── src/
│   ├── app/                 # Routes and experiment pages
│   │   ├── lab/             # Convex lens laboratory
│   │   ├── physics/         # Physics experiments
│   │   ├── chemistry/       # Chemistry experiments
│   │   ├── sandbox/         # Circuit sandbox
│   │   ├── observations/    # Observation ledger
│   │   └── report/          # Printable reports
│   ├── components/          # Reusable UI and 3D components
│   └── lib/                 # Scientific calculations and utilities
├── docs/
│   └── images/              # README screenshots
├── package.json
└── README.md
```

---

## 🔬 Scientific Validation

Each experiment should clearly state its assumptions, units, formulas, and limitations before being used for instruction or assessment.

Recommended validation checks:

- Unit-test optical equations, especially near the focal point.
- Verify circuit results against independently calculated voltage, current, and resistance values.
- Validate refraction and prism behaviour using Snell’s law.
- Define concentration ranges and assumptions for conductivity models.
- Test visual output across desktop and mobile browsers.
- Clearly label all simulated values as **simulated readings**, not physical measurements.

---

## ⚡ Performance and Compatibility

Performance depends on device hardware, browser version, screen resolution, scene complexity, and power settings.

| Record | Details to Include |
|---|---|
| Device | Exact phone, tablet, or computer model |
| Browser | Browser name and version |
| Scene | Experiment and rendering settings |
| Measurement | Tool, duration, and repeated-run results |
| AR support | Whether immersive AR was tested |

---

## 🗺️ Roadmap

- [ ] Add verified screenshots and a hosted demo link
- [ ] Add automated tests for scientific calculations
- [ ] Publish a browser and device compatibility matrix
- [ ] Document offline behaviour and connectivity requirements
- [ ] Improve keyboard navigation and reduced-motion support
- [ ] Add teacher-facing classroom guides
- [ ] Evaluate learning outcomes through a documented student study

---

## 📚 References

- [NCERT](https://ncert.nic.in/) — curriculum and laboratory learning resources
- [Three.js Documentation](https://threejs.org/docs/) — 3D rendering
- [WebXR Device API](https://www.w3.org/TR/webxr/) — immersive web experiences
- [Next.js Documentation](https://nextjs.org/docs) — framework setup and deployment
- Hecht, Eugene. *Optics*, 5th Edition, Pearson, 2017
- Atkins, Peter and de Paula, Julio. *Physical Chemistry*, 11th Edition, Oxford University Press

---

## 🤝 Contributing

Contributions are welcome!

Before opening a pull request:

1. Explain the problem or proposed improvement.
2. Keep scientific calculations separate from UI and rendering logic.
3. Include tests or reproducible steps for equation or experiment changes.
4. Add screenshots for significant UI changes.
5. Never include secrets, API keys, or personal data in commits.

---

## 📄 License

This project is intended to be released under the [MIT License](LICENSE).

> Add a valid `LICENSE` file before describing the project as MIT-licensed.

---

## 👨‍💻 Maintainer

**Sarath** · [@Saraththecoder](https://github.com/Saraththecoder)

---

<div align="center">

**Making science concepts more visual, interactive, and approachable.**

<sub>Built as an educational technology project.</sub>

</div>
