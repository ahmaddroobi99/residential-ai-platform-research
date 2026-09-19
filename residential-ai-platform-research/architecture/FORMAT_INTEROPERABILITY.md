# Format interoperability matrix

| Format | Domain | In | Out | Open? | Tools | Conversion notes |
|---|---|---|---|---|---|---|
| IFC (ISO 16739) | BIM | Authoring apps, IfcOpenShell | Other BIM, viewers, QTO | Yes | IfcOpenShell, xBIM, web-ifc, Bonsai | Canonical semantic building graph |
| BCF | Issues | Clash tools | PM / CDE | Yes | IfcOpenShell bcf, Solibri, Navisworks | Do not send the whole model |
| IDS | Requirements check | Spec writer | Pass/fail | Yes | IfcTester, xBIM IDS | Tightens IFC quality |
| COBie | FM handover | BIM | Spreadsheet / FM | Yes | xBIM CobieExpress | End of construction |
| gbXML | Energy | BIM | EnergyPlus / others | Yes | Honeybee, vendor exporters | Geometry cleanliness is the failure mode |
| CityGML / CityJSON | City | GIS / city models | Urban twin | Yes | 3DCityDB, QGIS plugins | Envelope overlap with IFC; CRS pain |
| GeoJSON | GIS vectors | Overpass, Regrid, municipal | Site model | Yes | GDAL, PostGIS | Not 3D BIM |
| GeoTIFF / COG | Rasters / DEM | USGS, satellites | Site elevation | Yes | GDAL | |
| LAS/LAZ | LiDAR | 3DEP, scanners | Clouds, DEM | Yes | PDAL, QGIS, Open3D | As-built + terrain |
| OpenUSD | Scene / sim | DCC, Omniverse | Twin runtime | Yes | usdview, Isaac Sim | Needs AEC schema to keep IFC meaning |
| glTF / GLB | Runtime 3D | IfcConvert, catalogs | Web / AR | Yes | model-viewer, Three.js | Loses BIM semantics |
| OBJ / STL | Mesh | converters | Viz / print | Yes | everywhere | No semantics |
| STEP / IGES | CAD solids | MCAD | CAD | Yes | OCCT, FreeCAD | Poor building semantics |
| DXF | CAD drawings | CAD | CAD / takeoff | Published | GDAL, CAD apps | 2D-heavy |
| DWG | CAD | AutoCAD world | CAD | Proprietary | Autodesk / Teigha-class | License trap |
| EPW | Weather | climate.onebuilding | EnergyPlus | Yes (files) | Ladybug | |
| URDF / SDF | Robots | ROS / Gazebo | Sim | Yes | ROS2 | BIM→SDF is research |
| Matter / HA | Devices | Smart home | Ops | Mixed | Home Assistant | Map via room IDs, not geometry |

buildingSMART ↔ AOUSD (2024-10-01) is a collaboration, not a finished IFC↔USD product.
