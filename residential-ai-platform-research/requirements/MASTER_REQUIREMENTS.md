# Master requirements

Schema used everywhere:

```
ID | Category | Requirement | Description | User Need | Input | Output |
Dependencies | Constraint | OSS | Commercial | Dataset | API | Standard |
Priority | Maturity | Open Questions
```

Priority: `P0` must exist for any prototype · `P1` needed for a serious pilot · `P2` later.  
Maturity: `none` / `research` / `partial` / `product` — of *the capability in the world*, not of our build.

Access date for linked options: 2026-09-19.

---

## Land + site

### REQ-LAND-001 — Parcel polygon
Ingest a parcel boundary + identifiers for an address.  
**In:** address or lat/lon. **Out:** polygon, APN/PID, area, CRS.  
**Deps:** geocoder, parcel vendor or municipal GIS.  
**OSS:** OSM (weak cadastral), QGIS/PostGIS tooling.  
**Commercial:** Regrid, municipal Esri layers, **LTSA (BC)**.  
**Standard:** GeoJSON.  
**Priority:** P0. **Maturity:** product (licensed).  
**Q:** Regrid vs LTSA coverage in Surrey?

### REQ-LAND-002 — Terrain
DEM/DSM or LiDAR for the lot + context.  
**In:** bbox. **Out:** elevation raster / LAS.  
**OSS/gov:** USGS 3DEP (US), OpenTopography.  
**Canada:** federal/provincial DEM — verify product for Metro Vancouver.  
**Priority:** P0. **Maturity:** product (US), partial (CA open).

### REQ-LAND-003 — Context buildings
Neighbour footprints and roads.  
**OSS/data:** OSM (ODbL), Microsoft CanadianBuildingFootprints (ODbL, older vintage), GlobalMLBuildingFootprints (CDLA 2.0).  
**Priority:** P0. **Maturity:** product.

### REQ-LAND-004 — Climate file
Select EPW by location.  
**Source:** [climate.onebuilding.org](https://climate.onebuilding.org/) TMYx + Canada CWEC / NRC future files.  
**Priority:** P0. **Maturity:** product.

### REQ-LAND-005 — Sun / wind / flood screening
Early environmental risk + amenity.  
**OSS:** Ladybug (AGPL). **Commercial:** Autodesk Forma.  
**Priority:** P1. **Maturity:** product.

### REQ-ZONE-001 — Jurisdiction resolve
Map coordinates → municipality + code family (BCBC vs IRC vs …).  
**Priority:** P0. **Maturity:** partial (you will hardcode a table at first).

### REQ-ZONE-002 — Zoning parameters
District, setbacks, height, FAR/FSR, coverage, use.  
**Commercial:** LightBox, Regrid Standardized Zoning, Archistar.  
**OSS:** NYC-specific repos; unofficial Municode; **no Surrey API found**.  
**Priority:** P0. **Maturity:** partial / PDF.

### REQ-ZONE-003 — Zoning → design envelope
Translate setbacks/height into a 3D buildable volume.  
**Commercial:** Forma Site Automation, TestFit, Archistar.  
**Priority:** P0. **Maturity:** product (closed).

---

## Requirements engineering

### REQ-REQ-001 — NL brief → constraint JSON
“4-bed house for 5, office preferred, 2-car, aging-in-place, budget X” → machine constraints.  
**OSS:** none mature as a product. Pattern = LLM + schema + validator.  
**Closest research:** ChatHouseDiffusion (text→plan, not constraints).  
**Priority:** P0. **Maturity:** research / DIY.

### REQ-REQ-002 — Preference weights
Multi-objective weights (daylight vs cost vs area vs privacy).  
**Priority:** P1. **Maturity:** research.

### REQ-HUM-001 — Clearances + accessibility
Circulation widths, turning spaces, CSA B651 / ADA / ISO 21542 envelopes.  
**Constraint:** code text is copyrighted. Encode *parameters*, not the book.  
**Priority:** P1. **Maturity:** guidelines, not a solver.

### REQ-HUM-002 — Adaptability flags
Aging-in-place, family growth, accessory unit.  
**Priority:** P2. **Maturity:** none as engine.

---

## Generative architecture

### REQ-ARCH-001 — Alternative floor plans
Generate multiple plans from program + envelope + adjacency.  
**OSS:** House-GAN++, FloorplanGAN, ChatHouseDiffusion, Hypar Elements, Buildify (verify claims).  
**Commercial:** Finch3D, Maket.ai, TestFit (site/units), Forma+Archistar (massing).  
**Data:** ResPlan (CC BY), CubiCasa5K (NC), RPLAN (research-only).  
**Priority:** P0. **Maturity:** research + closed products.

### REQ-ARCH-002 — Code-aware minima
Room area, egress, window/floor ratios per jurisdiction.  
**OSS:** not verified as a real checker. Buildify claims IRC — **VERIFY**.  
**Priority:** P1. **Maturity:** none trustworthy in OSS.

### REQ-ARCH-003 — Plan graph → IFC spaces/walls/doors
**OSS:** IfcOpenShell authoring API, Bonsai, Hypar IFC-gen.  
**Priority:** P0. **Maturity:** partial (you write the mapping).

---

## Computer vision

### REQ-CV-001 — Image/video masks
SAM 2 (Apache-2.0). **Priority:** P1. **Maturity:** product-grade model.

### REQ-CV-002 — Photos → 3D
COLMAP (BSD) + Open3D (MIT). **Priority:** P1. **Maturity:** product.

### REQ-CV-003 — Floorplan raster → rooms/walls/doors
CubiCasa5K models. **Priority:** P1. **Maturity:** research.

### REQ-CV-004 — Phone photos → measurements
**Commercial:** HOVER API. **Priority:** P1. **Maturity:** product.

---

## CAD / BIM

### REQ-CAD-001 — Parametric solids
OCCT via FreeCAD / IfcOpenShell / xBIM Geometry. **Priority:** P1.

### REQ-BIM-001 — Parse/author IFC4 / IFC4.3
IfcOpenShell (LGPL), xBIM (CDDL), web-ifc (MPL). **Priority:** P0. **Maturity:** product.

### REQ-BIM-002 — IFC → glTF / USD view
IfcConvert, That Open, APS, experimental USD maps. **Priority:** P0. **Maturity:** partial (semantic loss).

### REQ-BIM-003 — Clash + BCF
IfcClash; Solibri; Navisworks. **Priority:** P1. **Maturity:** product.

### REQ-BIM-004 — IDS property validation
IfcTester, xBIM IDS (AGPL). **Priority:** P1. **Maturity:** product.

---

## Structure / MEP / physics

### REQ-STR-001 — IFC structure → FEM
ifc2ca → Code_Aster; OpenSees; CalculiX. **Priority:** P2. **Maturity:** research/specialist.

### REQ-PHYS-001 — Energy
EnergyPlus + OpenStudio. **Priority:** P1. **Maturity:** product.

### REQ-PHYS-002 — Daylight
Radiance + Honeybee (AGPL). **Priority:** P1. **Maturity:** product.

### REQ-PHYS-003 — BIM → energy
gbXML or Honeybee translation. **Priority:** P1. **Maturity:** partial (garbage-in).

---

## Interior / FFE / render

### REQ-INT-001 — Style options from a photo
Commercial restyle tools. Output is **not** BIM. **Priority:** P2.

### REQ-INT-002 — Furniture layout with clearances
Research (3D-FRONT / ATISS class) + Sweet Home 3D. **Priority:** P1. **Maturity:** research.

### REQ-FFE-001 — Catalog item completeness
SKU + dims + 3D + price + lead time. **Priority:** P1. **Maturity:** **gap**.

### REQ-FFE-002 — Legal-clean 3D assets
Poly Haven CC0, Kenney CC0, licensed manufacturer feeds. **Priority:** P0.

### REQ-REN-001 — IFC → web viewer
model-viewer, That Open, Speckle, Cesium. **Priority:** P0.

---

## Construction / finance

### REQ-CON-001 — Takeoff from IFC/PDF/DWG
OpenConstructionERP (AGPL), Ifc5D, Procore, ACC Takeoff. **Priority:** P1.

### REQ-CON-002 — Priced BOQ with regional modifiers
Licensed cost tables. **Priority:** P1. **Maturity:** product (paid data).

### REQ-CON-003 — Residential builder workflow
Selections, COs, homeowner portal. Buildertrend class. **Priority:** P1.

### REQ-FIN-001 — Construction cash flow + contingency
**Priority:** P1. **Maturity:** spreadsheets / PM suites.

### REQ-FIN-002 — Mortgage amortization, jurisdiction-aware
OSS: mortgagemath (verify Canada). **Gap:** CMHC / stress test. **Priority:** P1.  
No investment advice.

### REQ-FIN-003 — Operating + energy + maintenance
**Priority:** P2.

---

## Twin / robots / ops

### REQ-DT-001 — BIM + sensors + time
No house-specific OSS product. Speckle + HA + USD is a composition. **Priority:** P2.

### REQ-ROB-001 — BIM-informed inspection path
Research papers + Spot commercial. **Priority:** P2.

### REQ-ROB-002 — As-built vs design
Cupix / Matterport / Open3D + IFC. **Priority:** P1.

### REQ-ROB-003 — Layout from BIM
Dusty FieldPrinter / HP SitePrint. **Priority:** P2.

### REQ-SM-001 — Matter/HA mapped to rooms
Home Assistant (Apache-2.0). **Priority:** P1.

### REQ-SM-002 — HVAC/energy optimization
HA Energy Dashboard + experimental HAEO. **Priority:** P2.

---

## AI / product

### REQ-AI-001 — NL → constraints (not a plan)
See REQ-REQ-001.

### REQ-AI-002 — Explained constrained generation
Trace which constraint killed which option. **Priority:** P1. **Maturity:** research.

### REQ-BIZ-001 — Buyer: builder vs architect vs homeowner
Different PM and CAD realities. **Priority:** P0 (strategy).

### REQ-BIZ-002 — MVP slice
Site + program → plan options → cost range → viewer. **Priority:** P0.
