# GitHub repositories

Verified **19 September 2026** via GitHub API and official READMEs.  
Stars are popularity snapshots, not quality scores.  
Do not treat a repo as reusable until you read its license and last-commit date yourself.

Legend: `HIGH` = can touch a residential land→twin pipeline in 24 months.

---

## BIM / OpenBIM

| Repo | Stars | Forks | Lang | License | Updated | I/O | Relevance | Notes |
|---|---:|---:|---|---|---|---|---|---|
| [IfcOpenShell/IfcOpenShell](https://github.com/IfcOpenShell/IfcOpenShell) | 2,795 | 967 | C++/Python | LGPL-3.0-or-later | 2026-09-19 | IFC2x3 / IFC4 / IFC4x3 → parse, author, IfcConvert (OBJ/DAE/GLB/STP/SVG), BCF, IDS | HIGH | Mature OpenBIM kernel. Bonsai add-on in same monorepo is **GPL-3.0-or-later**. Site: [ifcopenshell.org](https://ifcopenshell.org/). Docs: [docs.ifcopenshell.org](https://docs.ifcopenshell.org/) |
| [opensourceBIM/BIMserver](https://github.com/opensourceBIM/BIMserver) | 1,752 | 643 | Java | AGPL-3.0 | 2026-09-17 | IFC in → CDE / query / version | HIGH | Copyleft AGPL. Last major push Mar 2026; still listed active |
| [specklesystems/speckle-server](https://github.com/specklesystems/speckle-server) | 844 | 255 | TypeScript | Apache-2.0 (confirm per package) | 2026-09-16 | Revit/IFC/Rhino/Blender/QGIS → versioned objects, GraphQL, viewer | HIGH | AEC data bus. Hosted cloud is commercial |
| [specklesystems/specklepy](https://github.com/specklesystems/speckle-py) | 137 | 50 | Python | Apache-2.0 | 2026 | Python SDK | HIGH | |
| [ThatOpen/engine_web-ifc](https://github.com/ThatOpen/engine_web-ifc) | ~1,000 | ~287 | TS/C++/WASM | MPL-2.0 | 2026-09-18 | IFC → browser/node read-write | HIGH | Use That Open Components. `web-ifc-viewer` is **LOW ACTIVITY / deprecated** |
| [xBimTeam/XbimEssentials](https://github.com/xBimTeam/XbimEssentials) | 576 | — | C# | CDDL | 2026-09-18 | IFC2x3/IFC4/IFC4.3 STEP/XML/IFCZIP | HIGH | Pair with XbimGeometry (OCCT). IDS validator is **AGPL-3.0** |
| [hypar-io/Elements](https://github.com/hypar-io/Elements) | 417 | 81 | C# | MIT | 2026-09-18 | lightweight BIM elements | HIGH | “Smallest useful BIM” |
| [hypar-io/IFC-gen](https://github.com/hypar-io/IFC-gen) | 143 | 37 | C# | check repo | active | IFC code generation | MED | |
| [buildingSMART/validate](https://github.com/buildingSMART/validate) | — | — | — | MIT | 2026-09-18 | IFC validation service | HIGH | Official |

---

## CAD / geometry

| Repo | Stars | License | Updated | Relevance | Notes |
|---|---:|---|---|---|---|
| [FreeCAD/FreeCAD](https://github.com/FreeCAD/FreeCAD) | 33,636 | LGPL-2.1 | 2026-09-19 | HIGH | Parametric CAD. BIM workbench + NativeIFC. Kernel = OpenCASCADE. 6,050 forks |
| [CGAL/cgal](https://github.com/CGAL/cgal) | ~6,100 | mixed LGPL/GPL per package | 2026-09 | HIGH | Computational geometry. **Read package license** |
| [openscad/openscad](https://github.com/openscad/openscad) | ~10,200 | GPL-2.0 | 2026-09-18 | MED | Code-as-CAD. Not BIM-semantic |

OpenCASCADE Technology (OCCT) is the kernel under FreeCAD, IfcOpenShell geometry, and xBIM Geometry. Site: [dev.opencascade.org](https://dev.opencascade.org). License: LGPL-2.1 + exception.

---

## Computer vision / 3D reconstruction

| Repo | Stars | License | Updated | I/O | Relevance | Notes |
|---|---:|---|---|---|---|---|
| [colmap/colmap](https://github.com/colmap/colmap) | 12,761 | new BSD | 2026-09-19 | images → SfM + MVS cameras/points/meshes | HIGH | Industry default photogrammetry. pycolmap on PyPI |
| [isl-org/Open3D](https://github.com/isl-org/Open3D) | ~14,000 | MIT | v0.20 on 2026-09-16 | clouds/meshes/RGB-D/splats → registration, TSDF, viz | HIGH | v0.20 adds Gaussian splat rendering |
| [facebookresearch/sam2](https://github.com/facebookresearch/sam2) | ~19,000 | Apache-2.0 | active | image/video + prompts → masks + tracking | HIGH | Paper arXiv:2408.00714. SA-V dataset CC BY 4.0 |
| [facebookresearch/segment-anything](https://github.com/facebookresearch/segment-anything) | — | Apache-2.0 | research | image + prompts → masks | HIGH historical | SAM 1 |
| [cvg/limap](https://github.com/cvg/limap) | — | check repo | — | images → line/plane SfM on COLMAP | MED-HIGH | Architectural wireframes |

`colmap/glomap` and `colmap/pycolmap` standalone repos are **archived**. Use current COLMAP + PyPI `pycolmap`.

Original Inria 3D Gaussian Splatting code is **research / non-commercial**. For commercial-capable training prefer Nerfstudio `gsplat` (Apache-2.0). Confirm license on the exact fork before shipping.

---

## Generative floor plans

| Repo | Stars | License | I/O | Relevance | Notes |
|---|---:|---|---|---|---|
| [ennauata/houseganpp](https://github.com/ennauata/houseganpp) | 256 | check LICENSE | RPLAN graph → layout | HIGH academic | CVPR 2021. Site: [project page](https://ennauata.github.io/houseganpp/page.html) |
| [sepidsh/Housegan-data-reader](https://github.com/sepidsh/Housegan-data-reader) | — | LICENSE UNCLEAR | RPLAN PNG → JSON graph | HIGH | Companion converter |
| [ChatHouseDiffusion/chathousediffusion](https://github.com/ChatHouseDiffusion/chathousediffusion) | 61 | Apache-2.0 | text + RPLAN → floor plans | HIGH academic | arXiv:2410.11908 |
| [sarvanithin/Buildify](https://github.com/sarvanithin/Buildify) | — | MIT | rooms/style → IRC-oriented plans + 3D | MED | **VERIFY** IRC-compliance claims |
| [luozn15/FloorplanGAN](https://github.com/luozn15/FloorplanGAN) | — | check LICENSE | RPLAN vector → vector plans | MED | Automation in Construction paper |
| [HanHan55/Graph2plan](https://github.com/HanHan55/Graph2plan) | — | Research/Education ONLY | graph + boundary → plan | HIGH academic | **Not commercial** |
| [CubiCasa/CubiCasa5k](https://github.com/CubiCasa/CubiCasa5k) | 589 | dataset separate | floorplan images → 80+ classes | HIGH | Model + download instructions |
| [m-agour/ResPlan](https://github.com/m-agour/ResPlan) | — | data CC BY 4.0, code MIT | 17k vector-graph plans | HIGH | Better commercial-data posture than RPLAN |

House-GAN (ECCV 2020) predecessor: [ennauata/housegan](https://github.com/ennauata/housegan). LIFULL-derived data — restricted.

---

## Building physics

| Repo | Stars | License | Relevance | Notes |
|---|---:|---|---|---|
| [NREL/EnergyPlus](https://github.com/NREL/EnergyPlus) | ~1,600 | custom EnergyPlus License (BSD-3-like + US gov rights) | HIGH | Whole-building energy + water. Site: [energyplus.net](https://energyplus.net) |
| [NREL/OpenStudio](https://github.com/NREL/OpenStudio) | 645 | BSD-style | HIGH | SDK over EnergyPlus + Radiance. C++/Ruby/Python/C# |
| [ladybug-tools/honeybee-energy](https://github.com/ladybug-tools/honeybee-energy) | — | AGPL-3.0 | HIGH | EnergyPlus/OpenStudio bridge. **AGPL SaaS implications** |
| [ladybug-tools/honeybee](https://github.com/ladybug-tools/honeybee) | — | GPL family | HIGH | Radiance daylight core |
| [LBNL-ETA/Radiance](https://github.com/LBNL-ETA/Radiance) | ~190 | Radiance License v2.0 (BSD-style) | HIGH | Official: [radiance-online.org](https://www.radiance-online.org/) |

---

## GIS

| Repo | Stars | License | Relevance | Notes |
|---|---:|---|---|---|
| [qgis/QGIS](https://github.com/qgis/QGIS) | ~14,000 | GPL-2.0-or-later | HIGH | Desktop GIS. LAS/LAZ/EPT, PostGIS, PyQGIS |
| [microsoft/USBuildingFootprints](https://github.com/microsoft/USBuildingFootprints) | ~2,300 | ODbL (verify current file) | HIGH | ~129.6M US footprints |
| [microsoft/GlobalMLBuildingFootprints](https://github.com/microsoft/GlobalMLBuildingFootprints) | — | CDLA Permissive 2.0 | HIGH | 1.4B buildings |
| [microsoft/CanadianBuildingFootprints](https://github.com/microsoft/CanadianBuildingFootprints) | — | VERIFY license on repo | HIGH | Relevant to Surrey, BC |
| [hotosm/osm-export-tool](https://github.com/hotosm/osm-export-tool) | 158 | BSD-3-Clause | HIGH | AOI → GeoJSON |

PostGIS, GDAL, GeoServer, Leaflet are the standard open GIS stack. See [APIS.md](APIS.md).

---

## Construction / quantities

| Repo | License | Relevance | Notes |
|---|---|---|---|
| [datadrivenconstruction/OpenConstructionERP](https://github.com/datadrivenconstruction/OpenConstructionERP) | AGPL-3.0 | HIGH | Self-hosted QTO / BOQ / 4D / 5D. `pip install openconstructionerp`. **AGPL** |
| [DataDrivenConstruction/QuantityTakeoff-Python](https://github.com/DataDrivenConstruction/QuantityTakeoff-Python) | GPL-3.0 | MED | CSV/BIMExcel filters |
| [simondilhas/qto_buccaneer](https://github.com/simondilhas/qto_buccaneer) | check repo | MED | IFC → QTO |

Open-source takeoff is far behind Procore / STACK / Bluebeam / Autodesk Takeoff.

---

## Robotics / digital twin / smart home

| Repo | Stars | License | Relevance | Notes |
|---|---|---|---|---|
| [home-assistant/core](https://github.com/home-assistant/core) | ~90,700 | Apache-2.0 | HIGH | Best residential ops kernel. Matter support rebuilt on matter.js (2026) |
| [allenai/procthor](https://github.com/allenai/procthor) | 472 | Apache-2.0 | HIGH | Procedural interactive houses for embodied AI |
| [ertis-research/opentwins](https://github.com/ertis-research/opentwins) | ~274 | Apache-2.0 | MED | Generic IoT + 3D twin, not house-specific |
| [jpatacas/bim2twin](https://github.com/jpatacas/bim2twin) | ~27 | MIT | LOW-MED | Prototype. LOW ACTIVITY |
| ROS 2 (`ros2` org) | — | Apache-2.0 | HIGH | Robot middleware |
| Gazebo (`gazebosim`) | — | Apache-2.0 | HIGH | OSS robot sim |

NVIDIA Isaac Sim is **not fully OSS** (NVIDIA EULA) but is the photoreal + ROS2 construction-sim default.

---

## Rendering / web 3D

| Repo | Stars | License | Relevance | Notes |
|---|---|---|---|---|
| [mrdoob/three.js](https://github.com/mrdoob/three.js) | very high | MIT | HIGH | WebGL runtime |
| [google/model-viewer](https://github.com/google/model-viewer) | ~8,200 | Apache-2.0 | HIGH | glTF/GLB embed + AR |
| [CesiumGS/cesium](https://github.com/CesiumGS/cesium) | ~15,800 | Apache-2.0 | HIGH | Globe + 3D Tiles + site context |
| [KhronosGroup/glTF](https://github.com/KhronosGroup/glTF) | — | spec | HIGH | Runtime 3D standard |

---

## Do not use / treat carefully

| Repo | Why |
|---|---|
| `xyicheng/xBim-Toolkit` | Stale CodePlex mirror |
| `ThatOpen` old `web-ifc-viewer` | Deprecated; last meaningful push ~2023 |
| `specklesystems/speckle-sharp` (legacy monorepo) | Archived 2026-05-12 |
| `colmap/glomap`, `colmap/pycolmap` standalone | Archived / deprecated |
| Unofficial IKEA API clients | Archived or ToS-hostile |
| Inria original 3DGS | Non-commercial research license |

---

## Search queries that keep paying off

```
IFC Python IfcOpenShell
BIM automation IFC
floor plan generation HouseGAN RPLAN
image to BIM OR image to CAD
quantity takeoff IFC
building digital twin BIM
LiDAR SLAM indoor
energy simulation EnergyPlus honeybee
GIS building zoning parcel
furniture layout 3D-FRONT
```
