# Datasets

Access date: **19 September 2026**.  
License is the blocker more often than size. Research-only datasets cannot silently become commercial training data.

---

## Floor plans / layout

| Dataset | Size | Format | License | Commercial? | URL | Notes |
|---|---|---|---|---|---|---|
| **RPLAN** | ~80,788 Asian residential plans | 256×256×4 PNG raster | Restricted research DUA | **No**, without a new agreement | [project page](http://staff.ustc.edu.cn/~fuxm/projects/DeepLayout/index.html) | Foundation of House-GAN++ / many 2020–2026 papers. Request form required. Do not redistribute |
| **ResPlan** | 17,000 unit-level plans | Vector + typed connectivity graph, metric | Data **CC BY 4.0**, code MIT | Likely yes (CC BY) — still read the card | [github.com/m-agour/ResPlan](https://github.com/m-agour/ResPlan) | Avg 8.1 rooms, median 110 m². No furniture |
| **CubiCasa5K** | 5,000 plans, 80+ classes | Raster + SVG polygons | Paper arXiv perpetual; dataset commonly cited **CC BY-NC-SA** (Kaggle lists 3.0 IGO) | **Non-commercial share-alike** | [github.com/CubiCasa/CubiCasa5k](https://github.com/CubiCasa/CubiCasa5k), [Zenodo 2613548](https://zenodo.org/records/2613548) | Mostly Finnish RE marketing plans. Furniture symbols included |
| **LIFULL HOME’s** | ~5M raster (JP) | Raster; ~124k vectorized by Liu et al. 2017 | NII restricted | **No** | NII / LIFULL | Used by House-GAN |
| **MSD** | 5,372 Swiss floor plates / 18.9k units | Vector + graph | CC BY 4.0 (per ResPlan comparison table) | Likely yes — verify | van Engelenburg et al. 2024 | Multi-unit extraction needed |
| **Graph2Plan data** | derived | graph + boundary | Research/Education ONLY | **No** | [HanHan55/Graph2plan](https://github.com/HanHan55/Graph2plan) | |

ResPlan paper comparison (arXiv:2508.14006) is the cleanest 2025–2026 floor-plan dataset table. Use it; do not invent counts.

---

## Indoor 3D scenes / furniture

| Dataset | Size | Format | License | Commercial? | URL | Notes |
|---|---|---|---|---|---|---|
| **3D-FRONT** + **3D-FUTURE** | 18,968 furnished rooms; professional meshes | JSON houses + textured furniture meshes | Alibaba ToU — email agreement | Academic / check ToU | [Tianchi / 3dfront@list.alibaba-inc.com](https://tianchi.aliyun.com/specials/promotion/alibaba-3d-scene-dataset) | Best synthetic furnished-home set. BlenderProc has a loader |
| **Structured3D** | 3,500 houses, 21,835 rooms, 196k renders | Structure primitives + photoreal images | Non-commercial research ToU; code MIT | **No** | [structured3d-dataset.org](https://structured3d-dataset.org/), [bertjiazheng/Structured3D](https://github.com/bertjiazheng/Structured3D) | |
| **Matterport3D** | 90 buildings, 10.8k panoramas, 194.4k RGB-D | Mesh + RGB-D + panoramas | Research ToU + form; code MIT | **No** | [matterport/Matterport3D](https://github.com/matterport/Matterport3D) | 3DV 2017 |
| **ScanNet** | 1,506 scans | RGB-D + mesh | Research ToU | **No** | ScanNet project | Partial rooms, not whole homes |
| **ProcTHOR-10K** | 10k procedural houses | AI2-THOR interactive | Apache-2.0 code; generated scenes | Likely yes for the generator | [allenai/procthor](https://github.com/allenai/procthor) | Embodied AI, not photoreal architecture |
| **IKEA 3D Assembly** | 5 products | GLB+OBJ+PDF | CC BY-NC-SA 4.0 | **No** | [IKEA/IKEA3DAssemblyDataset](https://github.com/IKEA/IKEA3DAssemblyDataset) | Not a catalog |

SUNCG is **gone** (legal takedown). Do not plan around it.

---

## Geospatial / site

| Dataset | Coverage | Format | License | URL | Notes |
|---|---|---|---|---|---|
| USGS **3DEP** | CONUS elevation | LAS/LAZ, DEM, EPT | US public domain | [usgs.gov/3d-elevation-program](https://www.usgs.gov/3d-elevation-program), [AWS Open Data](https://registry.opendata.aws/usgs-lidar/) | Not Canada |
| OpenStreetMap | Global | OSM PBF / Overpass | **ODbL-1.0 share-alike** | [openstreetmap.org](https://www.openstreetmap.org) | Derived maps inherit share-alike |
| Microsoft US Building Footprints | ~129.6M US | GeoJSON | ODbL (verify current) | [microsoft/USBuildingFootprints](https://github.com/microsoft/USBuildingFootprints) | |
| Microsoft Global ML Footprints | 1.4B | GeoJSON | CDLA Permissive 2.0 | [microsoft/GlobalMLBuildingFootprints](https://github.com/microsoft/GlobalMLBuildingFootprints) | |
| Microsoft Canadian Building Footprints | Canada | GeoJSON | **VERIFY on repo** | [microsoft/CanadianBuildingFootprints](https://github.com/microsoft/CanadianBuildingFootprints) | Relevant to Surrey |
| climate.onebuilding.org TMYx | 17k+ locations | EPW / STAT / DDY | Free with citation | [climate.onebuilding.org](https://climate.onebuilding.org/) | Includes Canada CWEC + NRC future files |
| EnergyPlus weather | selected | EPW | DOE | [energyplus.net](https://energyplus.net) | |

Authoritative **BC parcels / titles** are **LTSA**, not an open dataset.

---

## Robotics / SLAM / inspection

Use standard robotics sets (TUM RGB-D, EuRoC, KITTI, ScanNet) plus ProcTHOR / AI2-THOR for indoor navigation.  
Construction-defect datasets exist in papers but licensing is inconsistent — treat each as `UNVERIFIED` until the card is read.

---

## Energy / materials

EnergyPlus example files ship with the engine.  
ASHRAE / Building Component Library measures are usable via OpenStudio.  
Embodied-carbon factors (EC3, ICE, ÖKOBAUDAT) are **separate licensed databases**, not free model weights.

---

## Practical data strategy

1. Prototype layouts on **ResPlan** (CC BY 4.0) + **CubiCasa5K** (NC) for recognition only.
2. Do **not** train a commercial generator on RPLAN / Graph2Plan / Matterport3D / Structured3D without counsel.
3. For interiors, 3D-FRONT is the best public furnished set — still ToU-gated.
4. For site context in BC: OSM (ODbL) + Canadian footprints + municipal open data + **licensed LTSA**.
5. Budget a line item for **cost data** (Craftsman or RSMeans) and **zoning data** (Regrid / LightBox). Those will not appear as GitHub zips.
