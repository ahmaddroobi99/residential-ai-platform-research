# Standards

---

## buildingSMART / OpenBIM

| Standard | What it is | Spec |
|---|---|---|
| **IFC** | Semantic building model | ISO 16739-1:2024 = **IFC 4.3.2.0 (IFC4X3 ADD2)**. Still common: IFC4 (4.0.2.1), IFC2x3. IFC 4.4 and IFC 5 in development. [technical.buildingsmart.org/standards/ifc](https://technical.buildingsmart.org/standards/ifc/) |
| **BCF** | Issue / RFI topics on a model | bcfXML + bcfAPI. Do not ship the whole IFC to talk about a clash |
| **IDS** | Machine-checkable information requirements | Pairs with IfcTester / xBIM IDS validator |
| **bSDD** | Shared dictionary of terms / properties | API-backed |
| **IDM / MVD** | Which IFC subset for which exchange | Coordination view, COBie MVD, etc. |
| **COBie** | Handover / FM asset tables | Spreadsheet + IFC MVD |
| **openCDE APIs** | Foundation, BCF, Documents, Dictionary | buildingSMART |

IfcOpenShell parse support (docs): IFC2x3 TC1, IFC4 Add2 TC1, IFC4x1, IFC4x2, IFC4x3 Add2. Extensive geometry: IFC2x3 TC1 and IFC4 Add2 TC1.

---

## Geospatial / city

| Standard | Body | Use |
|---|---|---|
| CityGML | OGC | City-scale semantic 3D |
| CityJSON | community / OGC-related | Friendlier CityGML encoding |
| LandInfra | OGC | Land + civil infrastructure |
| GeoJSON | RFC 7946 | Web GIS vectors |
| GeoTIFF / COG | OGC / community | Rasters, DEM |
| LAS/LAZ | ASPRS | LiDAR |
| WMS / WFS / WMTS | OGC | Map / feature services |

OGC + buildingSMART IDBE paper documents why IFC, CityGML, and LandInfra **overlap and disagree** (CRS, LOD, design vs observed).

---

## Energy / performance

| Standard | Use |
|---|---|
| **gbXML** | BIM → energy model. [gbxml.org](https://www.gbxml.org/) |
| EnergyPlus IDF / OSM | Simulation input |
| EPW | Typical meteorological year |
| HPXML | US residential energy audit / program data — useful pattern, not global |

---

## 3D runtime / viz

| Standard | Body | Use |
|---|---|---|
| **glTF 2.0** | Khronos, ISO/IEC 12113:2022 | Web / AR product and mesh delivery |
| **OpenUSD** | Pixar + AOUSD. Core Spec 1.0 Dec 2025 | Scene composition, sim, twin runtime |
| OBJ / STL / FBX | mixed | Mesh interchange. FBX proprietary |
| STEP / IGES | ISO | CAD solids |
| DXF | Autodesk-published | 2D/3D CAD |
| DWG | Autodesk proprietary | Default NA CAD file |

buildingSMART ↔ Alliance for OpenUSD collaboration announced **1 Oct 2024**. That is a working agreement, **not** a finished IFC↔USD product.

---

## Codes / accessibility (constraint sources, not open APIs)

| Instrument | Notes |
|---|---|
| IRC / IBC (ICC) | US model codes. **Copyrighted. No republish.** |
| NBCC | Canada model code |
| BC Building Code | Provincial adoption + amendments |
| City of Surrey zoning bylaw | Municipal PDF/HTML. No API found |
| ADA / CSA B651 / ISO 21542 | Accessibility. Copyrighted text |
| CSA / ASHRAE energy standards | Performance targets |

---

## Smart home / robots

| Standard | Notes |
|---|---|
| Matter (CSA) | Local IP smart-home interoperability |
| Thread / Wi-Fi / Ethernet | Matter transports |
| BACnet / Modbus | Building automation (more commercial buildings) |
| ROS 2 DDS | Robot middleware |
| URDF / SDF | Robot + world description |

---

## License / legal standards that bite

| Thing | Why it matters |
|---|---|
| ODbL (OSM, some footprints) | Share-alike on derived maps |
| AGPL (BIMserver, Ladybug, OpenConstructionERP) | SaaS copyleft |
| GPL (Bonsai, QGIS) | Addon / desktop copyleft |
| ICC / code text | Cannot ship the code book inside an LLM prompt cache as a product |
| RSMeans | Cannot redistribute unit costs |
