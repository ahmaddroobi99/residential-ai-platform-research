# Papers

Prioritize: foundational method → widely cited → recent SOTA → has code + data.  
Links are to arXiv or project pages. Access date: 2026-09-19.

```
PAPER → METHOD → CODE → DATASET → REPRODUCTION POSSIBILITY
```

---

## Generative floor plans / computational design

| Paper | Year | Venue | Code | Data | Notes |
|---|---|---|---|---|---|
| House-GAN: Relational GANs for graph-constrained house layout | 2020 | ECCV | [ennauata/housegan](https://github.com/ennauata/housegan) | LIFULL-derived (restricted) | Bubble-diagram → boxes |
| **House-GAN++**: Layout refinement network | 2021 | CVPR | [ennauata/houseganpp](https://github.com/ennauata/houseganpp) | RPLAN (restricted) | [arXiv:2103.02574](https://arxiv.org/abs/2103.02574). Project: [ennauata.github.io/houseganpp](https://ennauata.github.io/houseganpp/page.html). SFU + Autodesk Research |
| **Graph2Plan** | 2020 | SIGGRAPH / TOG | [HanHan55/Graph2plan](https://github.com/HanHan55/Graph2plan) | Research/Education ONLY | [arXiv:2004.13204](https://arxiv.org/abs/2004.13204) |
| RPLAN / DeepLayout (Wu et al.) | 2019 | — | toolboxes exist | RPLAN ~80k | Dataset paper behind most GAN layout work |
| CubiCasa5K | 2019 | — | [CubiCasa/CubiCasa5k](https://github.com/CubiCasa/CubiCasa5k) | 5k plans | [arXiv:1904.01920](https://arxiv.org/abs/1904.01920) |
| FloorplanGAN (Luo & Huang) | — | Automation in Construction | [luozn15/FloorplanGAN](https://github.com/luozn15/FloorplanGAN) | RPLAN subset | Vector generator + raster discriminator |
| HouseDiffusion | 2023-ish | — | reproductions exist | RPLAN | Discrete + continuous denoising of vector plans |
| ChatHouseDiffusion | 2024 | arXiv | [ChatHouseDiffusion](https://github.com/ChatHouseDiffusion/chathousediffusion) | RPLAN | [arXiv:2410.11908](https://arxiv.org/abs/2410.11908). Text-guided edit |
| ResPlan dataset paper | 2025 | arXiv | [m-agour/ResPlan](https://github.com/m-agour/ResPlan) | CC BY 4.0 | [arXiv:2508.14006](https://arxiv.org/abs/2508.14006) |
| Generative Floor Plan Design with LLMs + RLVR | 2026 | arXiv | — | RPLAN via HouseGAN++ reader | [arXiv:2605.14117](https://arxiv.org/abs/2605.14117) |
| Stanislas Chaillou, Architecture & GANs | 2019–20 | studio / Harvard | pix2pix lineage | — | Cultural foundation; not a maintained product |

---

## Indoor 3D / reconstruction / scenes

| Paper | Year | Code / data | Notes |
|---|---|---|---|
| Matterport3D | 2017 3DV | research ToU | RGB-D whole-home scans |
| ScanNet | 2018 CVPR | research ToU | RGB-D indoor |
| Structured3D | 2020 | [structured3d-dataset.org](https://structured3d-dataset.org/) | [arXiv:1908.00222](https://arxiv.org/abs/1908.00222) |
| 3D-FRONT | 2021 | ToU gated | [arXiv:2011.09127](https://arxiv.org/abs/2011.09127) |
| Raster-to-Vector (Liu et al.) | 2017 ICCV | — | Floorplan vectorization used on LIFULL |
| COLMAP SfM/MVS (Schönberger et al.) | 2016 CVPR + later | [colmap/colmap](https://github.com/colmap/colmap) | Default photogrammetry stack |
| Segment Anything | 2023 | Apache-2.0 | Foundation mask model |
| SAM 2 | 2024 | Apache-2.0 | [arXiv:2408.00714](https://arxiv.org/abs/2408.00714) |
| 3D Gaussian Splatting (Kerbl et al.) | 2023 SIGGRAPH | research license on original code | Prefer `gsplat` for Apache-2.0 training |
| ProcTHOR | 2022 NeurIPS | Apache-2.0 | Outstanding Paper. Procedural interactive houses |

---

## BIM / robotics / physics (entry points)

| Topic | Starting points |
|---|---|
| IFC → robot sim | Component-based robot prefab construction using IFC (2023+); IFC → SDF/Gazebo papers |
| BIM + ROS2 inspection | “Automating on-site object inspection with a quadruped robot and BIM” (Automation in Construction 2025) — ROS2 Iron, Nav2, IfcOpenShell, Open3D |
| OpenBIM standards | buildingSMART technical docs, ISO 16739-1:2024 |
| EnergyPlus / OpenStudio | NREL technical reports + EnergyPlus Engineering Reference |
| Ladybug Tools | Roudsari & Subramaniam Radiance/Python talks |
| GIS–BIM integration | OGC + buildingSMART IDBE paper on IFC / CityGML / LandInfra |

Search Scholar / arXiv with the category name plus `IFC`, `BIM`, `floor plan`, `digital twin`, `construction robot`. Prefer papers that ship code.

---

## Reproduction reality

| Claim | Reality |
|---|---|
| “I can retrain House-GAN++ commercially on RPLAN” | **No**, not under the public DUA |
| “Graph2Plan is production-ready” | Research/Education license |
| “3D-FRONT is a drop-in furniture catalog” | ToU-gated, not SKUs or prices |
| “NeRF/3DGS replaces BIM” | Visualization / as-built appearance, not semantic IFC |
