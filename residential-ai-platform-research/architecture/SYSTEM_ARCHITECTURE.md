# System architecture (research view)

This is a **reference architecture for thinking**, not a selected stack.

---

## Layers

```
┌──────────────────────────────────────────────────────────┐
│  Experience: homeowner / architect / builder / investor  │
│  Web UI · 3D viewer · chat brief · comparison boards     │
├──────────────────────────────────────────────────────────┤
│  Orchestration: agents, workflows, requirement IDs       │
├────────────┬────────────┬────────────┬───────────────────┤
│ Land/GIS   │ Generative │ BIM kernel │ Physics / codes   │
│ Zoning     │ layout     │ IFC graph  │ Energy / FEM      │
├────────────┴────────────┴────────────┴───────────────────┤
│  Cost · procurement · schedule · PM connectors           │
├──────────────────────────────────────────────────────────┤
│  Twin runtime: USD/glTF + time series + sensors          │
│  Robotics adapters (ROS2) · Smart home (Matter/HA)       │
├──────────────────────────────────────────────────────────┤
│  Data: object store · graph DB · spatial DB · versions   │
│  Speckle-like design VCS · IFC snapshots · BCF issues    │
└──────────────────────────────────────────────────────────┘
```

---

## Canonical object graph (target, not implemented)

```
PROJECT
 ├── SITE (parcel, CRS, zoning envelope, terrain, climate)
 ├── REQUIREMENTS (program, budget, constraints, weights)
 ├── OPTIONS[] (generative alternatives)
 │     ├── PLAN_GRAPH (rooms, edges, doors)
 │     ├── MASSING
 │     └── SCORES (daylight, energy, cost, code flags)
 ├── BUILDING
 │     ├── IFC model (arch + struct + MEP + furniture)
 │     ├── SIMULATION runs
 │     ├── QTO + COST
 │     └── SCHEDULE
 ├── TWIN
 │     ├── as-designed
 │     ├── as-built scans
 │     └── live sensors
 └── OPS (devices, warranties, maintenance)
```

Every requirement ID in `/requirements` should eventually write or read a node on this graph.

---

## Candidate technology *classes* (not a lock-in)

| Layer | Open class | Commercial class |
|---|---|---|
| GIS store | PostGIS + GDAL + QGIS | ArcGIS / Regrid |
| Requirements | LLM + JSON schema + solver | none mature |
| Layout gen | HouseGAN++-class / Hypar Elements | Finch, TestFit, Forma |
| BIM kernel | IfcOpenShell + Bonsai / FreeCAD | Revit / Archicad |
| Design bus | Speckle | ACC / BIM 360 |
| Physics | EnergyPlus + OpenStudio + Radiance | IES / Sefaira / cove.tool |
| Viewer | That Open + model-viewer + Cesium | Twinmotion / Enscape / D5 |
| Twin scene | OpenUSD | Omniverse / iTwin / Cupix |
| Field PM | OpenConstructionERP (AGPL) | Procore / Buildertrend |
| Ops | Home Assistant + Matter | vendor clouds |
| Robots | ROS2 + Gazebo | Spot + Isaac Sim |

---

## Suggested research prototype slice

Not a product. A way to expose integration bugs early:

1. Address → parcel polygon + DEM + footprints + EPW
2. NL brief → constraint JSON
3. Generate 5 plan graphs inside the zoning envelope
4. Author a minimal IFC (spaces, walls, slabs, doors, windows)
5. Run a coarse EnergyPlus + Radiance check
6. Extract quantities (no priced RSMeans unless licensed)
7. Publish glTF to a web viewer
8. Log every step against REQ-IDs

Stop. Measure where semantics were lost. That list *is* the architecture review.
