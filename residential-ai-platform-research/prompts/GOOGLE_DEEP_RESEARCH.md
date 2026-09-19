# Google / Gemini Deep Research — prompt pack

Use this instead of one 40-section mega-prompt. Gemini Deep Research (including Deep Research Max on Gemini 3.1-class models) works best when the **seed is short** and the **plan is specific**. Edit the generated plan before you run it.

## How to run

1. Open Gemini Deep Research.
2. Paste **P0** once so the model knows the rules.
3. Start a **new research run** for each of **P1–P12**. One headline group per run.
4. In the plan editor, paste the category “must find” list and the output template.
5. After all 12 dumps exist, start a new chat and paste **SYNTHESIS** plus the 12 outputs.
6. Drop the synthesized Markdown into this repo. Do not invent anything the 12 dumps did not contain.

Do not ask one run to search 250 topics, emit 12 files, scrape GitHub stars, and embed GIFs. That is how you get hallucinated repos.

Canada / BC notes belong in P1, P10, P12 whenever parcels, codes, climate, or mortgages appear.

---

## P0 — Orchestrator (paste first)

```
You are a technical research analyst, systems architect, BIM/GIS researcher, and documentation engineer.

Target system: an end-to-end AI residential development platform.
Pipeline: land → requirements → generative design → BIM/CAD → validation/simulation → cost/procurement → construction → digital twin → robotics → home operations.

PHASE = DISCOVER / RESEARCH / REQUIREMENTS / ECOSYSTEM MAP / GAPS only.
Do NOT implement software, pick a final technology stack, or write production code.

Quality rules:
- Primary sources only: official docs, GitHub, buildingSMART, NREL, government portals, company product pages, arXiv.
- Never invent repositories, APIs, prices, licenses, star counts, compatibility, or features.
- If unverified write UNVERIFIED. If stale write LOW ACTIVITY. If license missing write LICENSE UNCLEAR.
- Do not rank “best”. Classify OPEN SOURCE / COMMERCIAL / ACADEMIC / MATURE / ACTIVE / EXPERIMENTAL / ABANDONED.
- Images/GIFs: official project media only. Record source URL, license, why relevant, which requirement it illustrates.
- When regulations, parcels, climate, or mortgages appear, add Canada/BC notes (NBCC, BC Building Code, Surrey zoning, LTSA, CWEC).
- No investment advice.

Output for later category runs: GitHub-ready Markdown with TOC, tables, mermaid when useful, and a Sources list with access dates.

After 12 category researches exist, I will ask you to synthesize files. Do not synthesize until then.
```

---

## Category template (reuse inside every P1–P12 run)

```
Objective: Produce a source-linked Markdown research section for [CATEGORY]
of an end-to-end AI residential development platform
(land → design → BIM → validate → cost → build → twin → robots → home ops).
Research and requirements only. Do not implement software or pick a final stack.

Audience: founding engineer building a navigable GitHub research repo.

Must produce:
1. Problem statement and user need
2. Requirements table using:
   ID | Category | Requirement | Description | User Need | Input | Output |
   Dependencies | Constraint | OSS options | Commercial options | Dataset |
   API | Standard | Priority | Maturity | Open questions
3. GitHub repos: name, URL, language, license, last update, inputs, outputs, reuse realism
4. Companies/products with official docs/API URLs and limitations
5. Datasets with license + commercial usability
6. Papers: foundational, SOTA, and those with code+data
7. APIs and standards
8. Interop edges to adjacent pipeline stages
9. Official visuals to link (source + license note)
10. Technology gaps and open questions
11. Sources with URLs and access date

Search variants, not one query:
[topic] GitHub | open source | API | dataset | paper | benchmark |
commercial software | startup | research lab | Python | C++ | IFC | BIM

Do not stop at the first page. Do not fabricate.
```

---

## P1 — Land / GIS / zoning / climate / codes

Replace `[CATEGORY]` with:

**Parcel data, cadastral/title, zoning districts, setbacks, FAR/FSR, height, use tables, DEM/DSM/LiDAR, building footprints, OSM/roads/utilities, flood/wildfire, solar/shadow/wind, EPW climate, municipal bylaws, building permits, IRC/IBC/NBCC/BC Building Code.**

Must include Canada/BC: LTSA, Surrey zoning, CWEC, Canadian footprints.  
Search: Regrid, LightBox, USGS 3DEP, Microsoft footprints, QGIS, PostGIS, Municode, climate.onebuilding.org.

## P2 — Requirements engineering + human factors

**NL brief → structured constraints; preference learning; ontologies; constraint solvers; explainable design decisions; ergonomics; circulation; accessibility (ADA, CSA B651, ISO 21542); aging-in-place; storage; family growth; privacy zones.**

Find any LLM + solver housing systems. State clearly if no mature OSS product exists.

## P3 — Generative architecture + floor plans

**House-GAN++, Graph2Plan, ChatHouseDiffusion, RPLAN, CubiCasa5K, ResPlan, Buildify, Finch, Hypar, TestFit, Archistar, Forma, Maket.ai, Snaptrude. Graph + boundary → plans. Code-aware generation. Export to IFC/DXF.**

Flag research-only dataset licenses.

## P4 — Computer vision / photogrammetry / image-to-CAD

**SAM/SAM2, OpenCV, floorplan recognition, CubiCasa methods, COLMAP, Open3D, photogrammetry, NeRF, 3DGS/gsplat licenses, Matterport3D, Structured3D, HOVER, Matterport, image-to-BIM, as-built vs design.**

## P5 — CAD / geometry

**FreeCAD, OpenCASCADE, CGAL, OpenSCAD, Hypar Elements, mesh repair, NURBS vs solids vs implicit, point clouds, collision geometry, STEP/IGES/DXF/DWG/glTF.**

## P6 — BIM / IFC / OpenBIM

**IfcOpenShell, Bonsai, xBIM, Speckle, That Open web-ifc, BIMserver, IFC 4.3.2.0 / ISO 16739-1:2024, BCF, IDS, bSDD, COBie, IfcClash, IfcConvert.**

Authoring vs viewing vs validation.

## P7 — Structure + MEP + building physics

**OpenSees, CalculiX, Code_Aster/ifc2ca, EnergyPlus, OpenStudio, Ladybug/Honeybee (note AGPL), Radiance, gbXML, HVAC/electrical/plumbing routing OSS vs commercial, moisture/thermal bridging, Passive House / net-zero.**

## P8 — Interior + furniture + FFE + catalogs

**Layout optimization, style recs, 3D furniture libraries, Poly Haven CC0, Kenney CC0, IKEA API absence + ToS risk, Coohom, Sweet Home 3D, SKU+dims+price+lead-time gap, kitchen/bath, lighting.**

## P9 — Rendering / USD / web 3D / XR

**Blender, Three.js, model-viewer, CesiumJS, OpenUSD, glTF, Unreal/Twinmotion/Enscape/D5, PBR, VR/AR walkthroughs, AI image-to-image as inspiration only.**

## P10 — Construction + QTO + procurement + PM

**OpenConstructionERP (AGPL), Ifc5D, Procore API, Buildertrend (residential, weaker API), ACC, RSMeans licensing, Craftsman, 4D/5D BIM, RFI/submittals, takeoff from IFC/PDF/DWG. Canada cost modifiers.**

## P11 — Digital twin + robotics + smart home

**Home Assistant + Matter, ROS2, Gazebo, Isaac Sim, Spot + BLK ARC, Dusty FieldPrinter, HP SitePrint, as-built vs BIM, sensor sync, energy dashboard. Single-family robot gap.**

## P12 — Standards + interop + AI methods + gaps

**IFC, CityGML, gbXML, COBie, BCF, OpenUSD, glTF, GeoJSON, LAS/LAZ, HPXML. Conversion paths and semantic loss. GNNs, diffusion, VLMs, PINNs, RAG/agents, uncertainty. Build the format matrix. List what does NOT exist as one integrated system.**

---

## SYNTHESIS (run last)

```
Merge ONLY what appears in the 12 research dumps I will paste.
Deduplicate. Do not invent repositories, APIs, licenses, prices, or features
that are not in the dumps. If two dumps disagree, keep both and mark the conflict.

Produce GitHub-ready files:

README.md
requirements/MASTER_REQUIREMENTS.md
ecosystem/GITHUB_REPOS.md
ecosystem/COMPANIES.md
ecosystem/DATASETS.md
ecosystem/PAPERS.md
ecosystem/APIS.md
ecosystem/STANDARDS.md
architecture/SYSTEM_ARCHITECTURE.md
architecture/INTEGRATION_MAP.md
decisions/TECHNOLOGY_GAPS.md
decisions/OPEN_QUESTIONS.md

README must include: TOC, mermaid system map, jump links, short verified tables,
requirement index, quality rules, sources.

Classify every tool: OPEN SOURCE / COMMERCIAL / ACADEMIC / MATURE / ACTIVE /
EXPERIMENTAL / ABANDONED / UNVERIFIED / LOW ACTIVITY / LICENSE UNCLEAR.

Stop before implementation. Do not choose a final stack.
```

---

## Visuals policy for Gemini (and for this repo)

Allowed to *link*:

- Official README / docs screenshots (IfcOpenShell, Bonsai, Speckle, Open3D, COLMAP, Ladybug, Home Assistant)
- Project pages: House-GAN++, Structured3D, Forma blog (copyright Autodesk — link, do not copy into the repo as if you own it)
- Public-domain USGS UI / data

Not allowed:

- Scraped IKEA / retailer product GIFs
- Random Pinterest floor-plan images
- Unlicensed YouTube frames dumped into `/visuals`

Prefer a `visuals/videos.md` list of official demo URLs over hotlinked GIFs.
