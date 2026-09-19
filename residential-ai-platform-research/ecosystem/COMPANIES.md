# Companies and commercial products

Research snapshot: **19 September 2026**.  
Product capabilities are taken from official sites and reputable trade press.  
**Internal architectures, unpublished APIs, and exact list prices are UNVERIFIED unless a primary source is linked.**  
Third-party price quotes are labelled indicative.

---

## Site / feasibility / generative design

| Company | Product | Role | Integrations | Notes |
|---|---|---|---|---|
| Autodesk | [Forma](https://www.autodesk.com/products/forma/overview) | Early-site massing, sun/wind/noise/carbon, site automation | Revit live sync, Rhino, Dynamo, APS APIs, Archistar / TestFit add-ons | Formerly **Spacemaker** (acquired 2020, brand retired May 2023). Do not list Spacemaker as current. Indicative standalone price cited at ~$185/mo — **VERIFY on Autodesk** |
| TestFit | [TestFit](https://www.testfit.io/) | Real-estate feasibility: units, parking, typology, pro forma | Revit export, Forma extension | Strong pre-acquisition loop. Multi-family > single-family interiors |
| Archistar | [Archistar](https://www.archistar.ai/) | Zoning-aware generative massing | Forma 3D Generative Design add-on (2025+) | AU heritage; now packaged inside Forma for global AECO |
| Finch3D | [Finch3D](https://finch3d.com/) | Graph-based multi-family floor plans from a massing | Revit, Rhino | Starts from massing, not from raw parcel |
| Hypar | [Hypar](https://hypar.io/) | Cloud generative **functions** (C#/Python) | IFC export, Revit | Open [Elements](https://github.com/hypar-io/Elements) library (MIT) |
| Snaptrude | [Snaptrude](https://www.snaptrude.com/) | Browser conceptual BIM + fast viz | Revit, SketchUp | Stronger on communication than code checking |
| Maket.ai | [Maket.ai](https://www.maket.ai/) | NL / sketch → residential plans + zoning assistant | DXF/DWG/SKP/PDF (per vendor comparisons) | Residential-focused. Export depth = **VERIFY** |
| Sidewalk Labs Delve | Delve | Urban generative planning | — | Treat as **historical / limited availability**, not a current default |
| Giraffe / Digital Blue Foam / Hektar | various | Planning / feasibility | — | Mentioned as Forma-class alternatives; evaluate per market |

---

## BIM / CAD authoring (incumbents)

| Company | Products | Why it matters |
|---|---|---|
| Autodesk | Revit, AutoCAD, Civil 3D, Navisworks, Construction Cloud, Forma | Default NA architecture + coordination stack. AEC Magazine (2026-09) reported Autodesk positioning Forma as a long-term Revit successor — treat as **strategy signal**, not a migration plan |
| Graphisoft (Nemetschek) | Archicad | Strong openBIM / IFC reputation |
| Bentley | MicroStation, OpenBuildings, iTwin | Infrastructure + twin platform |
| Trimble | Tekla, SketchUp, Connect, Sefaira | Structure + sketch + energy plugin |
| Nemetschek | Allplan, Vectorworks | Regional BIM strength |
| Bricsys | BricsCAD BIM | DWG-native BIM alternative |
| Solibri (Nemetschek) | Solibri Office | Model checking + BCF. 2026 notes: point-cloud vs model clash |

---

## Construction management / takeoff / cost

| Company | Product | Fit | API | Notes |
|---|---|---|---|---|
| Procore | [Procore](https://www.procore.com/) + [Takeoff](https://www.procore.com/fc/takeoff) | Mid/large GC, commercial + some residential | First-class REST, OAuth2, [developers.procore.com](https://developers.procore.com) | RFIs, submittals, drawings, inspections, AI count |
| Buildertrend | [Buildertrend](https://www.buildertrend.com/) | Residential builders / remodelers | Public API depth **LIMITED / UNVERIFIED** | Selections, change orders, homeowner portal, QuickBooks/Xero |
| Autodesk | Construction Cloud + Takeoff | ACC-centric firms | [APS](https://aps.autodesk.com) | 2D + 3D quantities |
| STACK | STACK Takeoff & Estimate | Trade / mid-market estimating | vendor site | Frequently paired with Buildertrend |
| Bluebeam (Nemetschek) | Revu / Bluebeam Cloud | PDF markup + takeoff | — | Field default for drawings |
| PlanSwift / CostX / Buildxact | various | SMB estimating | — | CostX is RIB / Schneider |
| Gordian | [RSMeans](https://www.rsmeans.com) | Unit-cost database | licensed enterprise API | **No redistribution.** Cannot embed in a product without a license |
| Craftsman Book | National Estimator + APIs | Residential cost data US/CA | [data licensing](https://craftsman-book.com/data-licensing/) | More reachable than RSMeans for housing |

Indicative list prices seen in 2026 review sites (Procore from $375/mo, Buildertrend from $99/mo, Autodesk Takeoff ~$1,290/user/yr) are **indicative only**.

---

## Reality capture / digital twins

| Company | Product | Capture | Output | Notes |
|---|---|---|---|---|
| Matterport (CoStar) | [Matterport](https://matterport.com/) | Camera / phone | Walkthrough, MatterPak, schematic plan, OBJ/cloud | Real-estate + construction. Procore / ACC embeds |
| Cupix | [Cupix](https://www.cupix.com/) | 360° video, lidar, drone | 4D twin, BIM overlay, measurements | Construction progress vs design |
| HOVER | [HOVER](https://hover.to/) + [developer API](https://developers.hover.to) | Phone photos | Exterior/interior measurements JSON/PDF/XLSX/SKP | First-class measurement API + webhooks |
| OpenSpace | OpenSpace | 360 site walk | Progress comparison | Construction documentation |
| Beamo | Beamo | 360 capture | Facility twin | Competing capture platform |

---

## Interior / furniture / visualization

| Company | Role | Catalog reality | Notes |
|---|---|---|---|
| Coohom | Plan → 3D + brand catalogs + hi-res render | Real SKUs (vendor claim) | Closest FFE-procurement viz |
| Homestyler / Planner5D / Foyr Neo | Consumer/pro web planners | Mixed | Not code-compliant BIM |
| RoomGPT / InteriorAI / Collov / Spacely | Photo → restyle image | Hallucinated products common | Inspiration only. No measured CAD |
| IKEA | Furniture | **No official public product/3D API** | Community clients archived. Scraping = ToS/legal risk |
| Wayfair / Houzz | Marketplaces | Partner APIs only, UNVERIFIED public 3D+price+stock bundle | Treat as partnership problem, not an integration you can assume |
| Poly Haven | CC0 PBR assets + API | Not retail SKUs | Best legally clean prototype furniture/HDRI source |
| Kenney Furniture Kit | CC0 low-poly GLB | Not photoreal | Prototype only |

---

## Robotics / site automation

| Company | Product | What it actually does | Residential relevance |
|---|---|---|---|
| Boston Dynamics | Spot + Orbit | Quadruped inspection, lidar/360/thermal | HIGH for inspection, not for building the house |
| Dusty Robotics | FieldPrinter | BIM/CAD → full-scale floor layout print | HIGH layout, commercial interiors > SF homes |
| HP | SitePrint | CAD/BIM → robotic layout | MED, competes with Dusty |
| JLG Canvas | drywall finish robot | Spray + sand | MED, commercial interiors |
| Built Robotics | autonomous earthwork / solar pile | Utility-scale solar pivot | MED for housing sites |
| Leica + BD | BLK ARC on Spot | Autonomous laser scan | HIGH as-built path |
| NVIDIA | Isaac Sim / Omniverse | Photoreal robot + USD sim | HIGH sim, not a field robot |

---

## Smart home / operations

| Company / project | Role | Notes |
|---|---|---|
| Home Assistant / Open Home Foundation | Open hub + Matter server | Best OSS operations kernel. Matter rebuilt on matter.js (2026) |
| Apple / Google / Amazon / Samsung | Matter controllers | Interop via Matter, not via one vendor lock-in if you stay local |
| openHAB | Alt open hub + Matter binding (5.0+) | Smaller community than HA |
| CSA Matter | Protocol standard | Wi-Fi / Ethernet / Thread, local IPv6 |

---

## GIS / parcel / zoning data vendors

| Vendor | What you buy | Coverage note |
|---|---|---|
| Regrid | Parcel polygons, ownership, standardized zoning | US + some Canadian provinces — **VERIFY Metro Vancouver / LTSA overlap** |
| LightBox | Zoning API: district, setbacks, FAR, height, use | Commercial |
| Shovels | Building permits as GIS layers; Regrid partnership | US permits |
| Esri | ArcGIS Online / Living Atlas / Feature Services | Municipal layers often live here |
| LTSA (BC) | Authoritative title + parcel for British Columbia | Licensed, not OSS. **This is the source of truth for Surrey lots** |

---

## How to read this list

There is **no company** that sells the full land → generative house → BIM → code check → cost → build → twin → robot loop.

Closest *partial* stacks:

- Site feasibility: Forma + TestFit + Archistar
- Design authoring: Revit / Archicad / FreeCAD+Bonsai
- Coordination: Navisworks / Solibri / Speckle
- Field: Procore or Buildertrend
- Reality: Matterport / Cupix / HOVER / Spot
- Ops: Home Assistant + Matter

The product strategy question is which **slice** you own versus which you integrate. See [../decisions/TECHNOLOGY_GAPS.md](../decisions/TECHNOLOGY_GAPS.md) and [../decisions/OPEN_QUESTIONS.md](../decisions/OPEN_QUESTIONS.md).
