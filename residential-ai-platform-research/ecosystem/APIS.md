# APIs and developer platforms

Primary sources preferred. If a public API is not documented on an official developer site, it is `UNVERIFIED` or `ABSENT`.

---

## Geospatial / site

| API | Official docs | Auth | Returns | Notes |
|---|---|---|---|---|
| OpenStreetMap **Overpass** | [overpass-api.de](https://overpass-api.de) | none (rate-limited) | OSM XML / JSON | ODbL share-alike |
| Mapbox / Google Maps / Esri | vendor docs | paid keys | geocode, tiles, routing | Commercial TOS |
| Regrid Parcel API | [regrid.com/parcel-api](https://regrid.com/parcel-api) | paid | GeoJSON parcels, ownership, zoning | VERIFY BC coverage |
| LightBox Zoning | [developer.lightboxre.com](https://developer.lightboxre.com/api/zoning) | paid | district, setbacks, FAR, height, use | |
| USGS TNM / 3DEP | [usgs.gov](https://www.usgs.gov/3d-elevation-program) | public | DEM, LAS, EPT | US only |
| OpenTopography | [portal.opentopography.org](https://portal.opentopography.org/datasets) | key | 3DEP / lidar | |
| Esri Feature Services | per municipality | often public | zoning, parcels, flood | Common municipal pattern; not one national API |
| ezesri | [pypi.org/project/ezesri](https://pypi.org/project/ezesri/) | none | scrape/export Esri layers | Directory of 24k+ public services |

**Absent:** a single official machine-readable zoning + building-code API for Canada or the US.

---

## BIM / AEC data

| API | Docs | Notes |
|---|---|---|
| Speckle GraphQL + webhooks | [speckle.systems](https://speckle.systems) + specklepy | Versioned AEC objects. OSS server or hosted |
| Autodesk Platform Services (APS) | [aps.autodesk.com](https://aps.autodesk.com) | Files, issues, Forma, ACC, model derivative |
| buildingSMART bSDD | [bsdd.buildingsmart.org](https://bsdd.buildingsmart.org) | Classifications / properties |
| buildingSMART BCF API | openCDE | Issue topics without shipping the model |
| IfcOpenShell Python | [docs.ifcopenshell.org](https://docs.ifcopenshell.org/) | Library, not HTTP |
| xBIM | [docs.xbim.net](https://docs.xbim.net) | .NET library |
| That Open Components | [docs.thatopen.com](https://docs.thatopen.com/) | Browser IFC |

---

## Construction / cost / measurements

| API | Docs | Notes |
|---|---|---|
| Procore REST | [developers.procore.com](https://developers.procore.com) | OAuth2. RFIs, drawings, cost codes, inspections |
| Buildertrend | vendor site | Public API **LIMITED / UNVERIFIED** |
| HOVER | [developers.hover.to](https://developers.hover.to) | Photos → measurements JSON/PDF/XLSX/SKP + webhooks |
| Matterport SDK / APIs | developer.matterport.com | Embed + model data. Confirm current product names |
| RSMeans / Gordian | licensed | **No redistribution** |
| Craftsman Book | [craftsman-book.com/data-licensing](https://craftsman-book.com/data-licensing/) | US/Canada modifiers |
| EstimationPro community | estimationpro.ai | Experimental, UNVERIFIED accuracy |

---

## Visualization / assets

| API | Notes |
|---|---|
| Poly Haven public API | CC0 models / HDRIs / textures |
| Google model-viewer | Component, not a catalog API |
| Cesium ion | 3D Tiles hosting (commercial tier) |

**Absent:** official IKEA / Wayfair / Houzz public API that returns SKU + dimensions + 3D + price + stock together.

---

## Smart home / robotics

| API | Notes |
|---|---|
| Home Assistant REST / WS | Local. Apache-2.0 |
| Matter (CSA) | Protocol, not a cloud API |
| ROS 2 topics / services / actions | Robot bus |
| Isaac Sim ROS2 bridge | NVIDIA EULA |
| Boston Dynamics Orbit / Spot SDK | Commercial, partner access |

---

## Climate / energy

| API / files | Notes |
|---|---|
| climate.onebuilding.org | Bulk EPW download, not a JSON API |
| EnergyPlus / OpenStudio CLI + SDK | Simulation engines |
| NREL developer APIs | PVWatts, NSRDB, etc. — useful for solar, not whole-house BIM |
