# Ten companies on this stack

**Separate research page** — companies only.  
Snapshot: **19 September 2026**. Research, not a vendor shortlist.

> Nobody sells the full loop: land → generative house → BIM → code check → cost → build → twin → robots → ops.  
> These ten ship **slices**. Treat them as adapters you study, not as a finished platform.

![Where the ten companies sit](../visuals/companies/00-pipeline-map.png)

![Pipeline cycle](../visuals/companies/pipeline-cycle.gif)

---

## How to read this page

Open this file on GitHub or in the repo folder. Images render **in place**. You do not open the `visuals/companies/` folder one file at a time.

| I want… | Go here |
|---|---|
| The ten companies | [The ten](#the-ten) |
| Official product pages | each company heading |
| Full vendor catalog | [COMPANIES.md](COMPANIES.md) |
| Process diagrams | [../visuals/process/](../visuals/process/) |
| What is missing | [../decisions/TECHNOLOGY_GAPS.md](../decisions/TECHNOLOGY_GAPS.md) |

```
LAND / ZONING     Autodesk Forma  ·  TestFit  ·  Archistar
BRIEF → PLANS     Maket.ai  ·  Finch 3D  ·  Snaptrude
PRODUCTION DOCS   Higharc  ·  Geom  ·  Autodesk Revit
AS-BUILT / TWIN   Matterport  ·  HOVER
```

---

## The ten

### 01  Autodesk — Forma + Revit + Construction Cloud

![Autodesk card](../visuals/companies/01-autodesk.png)

| | |
|---|---|
| **Site** | [forma overview](https://www.autodesk.com/products/forma/overview) |
| **Slice** | Land, climate, generative massing, BIM, construction docs |
| **What they ship** | Forma (ex-Spacemaker) does site + sun/wind/noise/energy and early massing. Revit is still the NA detailed-BIM default. Construction Cloud holds field documents. Tandem is the operations-twin product. |
| **What they do not ship** | A homeowner-language brief → code-checked single-family house. Forma is not a residential floor-plan generator. |
| **Status** | Current. Do **not** list Spacemaker as a live product. AU 2026 previewed agentic assistants across Forma / Fusion / Flow. |

Related process image:

![Land / GIS](../visuals/process/05-land-gis.png)

---

### 02  TestFit

![TestFit card](../visuals/companies/02-testfit.png)

| | |
|---|---|
| **Site** | [testfit.io](https://www.testfit.io/) |
| **Slice** | Land, zoning envelope, financial feasibility |
| **What they ship** | Real-time site configurator: unit mix, parking, typology, yield, rough pro forma. Multifamily, townhome, single-family, retail, mixed use. Forma add-on exists. |
| **What they do not ship** | Custom single-family interiors, IFC authoring, energy models, or a digital twin. |
| **Status** | Current. 10th anniversary in 2026. Stronger on deal math than on livable room graphs. |

---

### 03  Higharc

![Higharc card](../visuals/companies/03-higharc.png)

![Higharc product visual](https://cdn.prod.website-files.com/65880fe1a6298c932c229007/6a42ca28ca0c8a9c7a187014_web-image-1-transparent-tiny.png)

| | |
|---|---|
| **Site** | [higharc.com](https://www.higharc.com/) |
| **Slice** | Requirements → plans → BIM / CDs for **production homebuilders** |
| **What they ship** | Generative Building Model keeps BIM geometry, not pixels. Plan change → lot-specific estimates, sales 3D, permit-ready documents. Signature Homes case: idea to permit-ready in two weeks; claimed $30M measured ROI. |
| **What they do not ship** | Parcel GIS for a random Surrey lot, municipal code checking as a public API, or a consumer design toy. |
| **Status** | Current. Closest commercial product to “the house as data” for production builders. Series C reported 2026 — treat exact round size as **VERIFY**. |

---

### 04  Geom

![Geom card](../visuals/companies/04-geom.png)

| | |
|---|---|
| **Site** | [geom.ai](https://www.geom.ai/) |
| **Slice** | Production housing documents on the files builders already use |
| **What they ship** | AI over DWG / DXF / PDF / DWF plan sets: QC, option solving, mirroring, plot plans, community / lot-level CDs. Semantic layer (walls, doors, rooms, setbacks) without forcing a new authoring tool. Public site names Meritage; press also cites Pulte, Century Communities, True Homes — **VERIFY each logo use**. |
| **What they do not ship** | Greenfield generative design from a family brief. It starts from existing plan sets. |
| **Status** | Just out of stealth, 18 September 2026. Young. Watch the next two quarters. |

---

### 05  Finch 3D

![Finch 3D card](../visuals/companies/05-finch-3d.png)

| | |
|---|---|
| **Site** | [finch3d.com](https://finch3d.com/) |
| **Slice** | Generative plans, adjacency, BIM handoff |
| **What they ship** | Graph-based housing floor plans from a massing, live metrics, Rhino / Revit / Archicad connectivity. |
| **What they do not ship** | Parcel GIS, energy simulation, or a homeowner portal. |
| **Status** | Current. Multifamily first. Pairs with Forma more than it replaces Revit. |

Related process image:

![Generative plans](../visuals/process/10-generative-plans.png)

---

### 06  Maket.ai

![Maket.ai card](../visuals/companies/06-maketai.png)

| | |
|---|---|
| **Site** | [maket.ai](https://www.maket.ai/) · [brand kit](https://www.maket.ai/brand-kit/identity) |
| **Slice** | Natural-language requirements, residential programming |
| **What they ship** | Type or sketch a residential brief → layout options, 3D, zoning assistant. Montreal company. La Presse (2026-09-14) reported 1M+ registered users and ALL IN 2026 selection. |
| **What they do not ship** | Stamped drawings, IFC that a contractor can build from, or a code-check engine you can audit. |
| **Status** | Current. Best “homeowner language → plan” product on this list. Export depth = **VERIFY**. Canada-relevant for a Surrey user. |

Related process image:

![User brief](../visuals/process/03-user-brief.png)

---

### 07  Archistar

![Archistar card](../visuals/companies/07-archistar.png)

| | |
|---|---|
| **Site** | [archistar.ai](https://www.archistar.ai/) |
| **Slice** | Zoning, setbacks, compliant massing |
| **What they ship** | Zoning-aware generative massing. Also packaged as an Autodesk Forma 3D Generative Design add-on. |
| **What they do not ship** | Room-level residential interiors or construction documents. |
| **Status** | Current. Australian heritage, now riding the Forma site model for global AECO. |

Related process image:

![Zoning envelope](../visuals/process/07-zoning-envelope.png)

---

### 08  Snaptrude

![Snaptrude card](../visuals/companies/08-snaptrude.png)

| | |
|---|---|
| **Site** | [snaptrude.com](https://www.snaptrude.com/) |
| **Slice** | Design intelligence → conceptual BIM |
| **What they ship** | Browser conceptual BIM and fast visualization. Claims a path from text / RFP toward an LOD-ish model exportable to Revit. |
| **What they do not ship** | A validated energy model, clash-checked MEP, or field construction OS. |
| **Status** | Current. Stronger on communication speed than on openBIM checking. LOD-300 claim = **VERIFY** on a real project. |

Related process image:

![BIM / IFC](../visuals/process/14-bim-ifc.png)

---

### 09  Matterport (CoStar)

![Matterport card](../visuals/companies/09-matterport.png)

| | |
|---|---|
| **Site** | [matterport.com](https://matterport.com/) |
| **Slice** | As-built, digital twin, inspection |
| **What they ship** | Phone / camera → navigable walkthrough, schematic plan, point cloud / MatterPak. Procore and ACC embeds. Path toward IFC / RVT exists as an add-on workflow, not as “scan = BIM”. |
| **What they do not ship** | A living operations twin with sensors and physics. A pretty dollhouse is not a digital twin. |
| **Status** | Current. Owned by CoStar. Default residential / commercial reality-capture product. |

Related process image:

![Digital twin](../visuals/process/25-digital-twin.png)

---

### 10  HOVER

![HOVER card](../visuals/companies/10-hover.png)

| | |
|---|---|
| **Site** | [hover.to](https://hover.to/) · [developer API](https://developers.hover.to) |
| **Slice** | Site / as-built dimensions without a survey crew |
| **What they ship** | Phone photos → exterior / interior measurements as JSON / PDF / XLSX / SketchUp. First-class measurement API + webhooks. |
| **What they do not ship** | Title-quality survey, IFC authoring, or indoor robotics. |
| **Status** | Current. One of the few residential measurement vendors with a real public developer surface. |

Related process image:

![As-built](../visuals/process/24-as-built-vs-design.png)

---

## Official sites (click, don’t scrape)

| # | Company | URL |
|---|---|---|
| 1 | Autodesk Forma | https://www.autodesk.com/products/forma/overview |
| 2 | TestFit | https://www.testfit.io/ |
| 3 | Higharc | https://www.higharc.com/ |
| 4 | Geom | https://www.geom.ai/ |
| 5 | Finch 3D | https://finch3d.com/ |
| 6 | Maket.ai | https://www.maket.ai/ |
| 7 | Archistar | https://www.archistar.ai/ |
| 8 | Snaptrude | https://www.snaptrude.com/ |
| 9 | Matterport | https://matterport.com/ |
| 10 | HOVER | https://hover.to/ |

---

## Honorable mentions (not in the ten)

| Company | Why it matters |
|---|---|
| [Hypar](https://hypar.io/) | Programmable generative functions + MIT Elements library, IFC / Revit export |
| [Buildertrend](https://www.buildertrend.com/) | Residential builder + homeowner portal. API is partner-gated, not a public developer portal |
| [Procore](https://www.procore.com/) | Same idea at GC scale, real public API |
| [Cupix](https://www.cupix.com/) / [OpenSpace](https://www.openspace.ai/) | Construction progress twins |
| [Dusty Robotics](https://www.dustyrobotics.com/) / HP SitePrint | BIM → floor layout robots |
| [Home Assistant](https://www.home-assistant.io/) | Open ops layer after handover |
| [Coohom](https://www.coohom.com/) | Interior + brand catalogs |

Do **not** list **Spacemaker** as current.  
Do **not** list Sidewalk Labs **Delve** as current (disabled 4 May 2026). A 2026 YC company also named Delve is a different compliance startup.

---

## Images and GIFs in this folder

All cards and the cycle GIF live next to this page:

```
visuals/companies/
  00-pipeline-map.png
  pipeline-cycle.gif
  01-autodesk.png
  02-testfit.png
  …
  10-hover.png
```

Cards are original research diagrams (not vendor screenshots). The Higharc product image is hotlinked from Higharc’s public CDN for identification only. Logos and product names remain the vendors’ trademarks.

---

## Partner reading, if you are picking, not shopping

1. **Higharc + Geom** — already inside North American production homebuilding.  
2. **Forma + TestFit + Finch + Archistar** — design-feasibility cluster.  
3. **Maket** — consumer / small-firm residential brief → plan.  
4. **Matterport + HOVER** — close the as-built loop.  
5. Everything else in this research pack is still an adapter you would have to build or license.

This page does not endorse any vendor and is not investment advice.
