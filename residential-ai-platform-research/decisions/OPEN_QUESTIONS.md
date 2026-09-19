# Open questions

Questions that need primary-source follow-up before architecture lock-in.

---

## Jurisdiction (Surrey, BC)

- Exact current year of BC Building Code in force, and which Surrey amendments apply to new detached / multiplex homes.
- LTSA product + price for parcel polygon + title/easement on a single lot.
- Regrid / LightBox actual Metro Vancouver coverage and refresh cadence.
- City of Surrey open-data layers: zoning, flood, utilities — which are downloadable vs map-only.
- School district, servicing, and development-cost-charge data sources.

## Codes as data

- Is there any licensed machine-readable IRC/NBCC/BCBC extract a startup can actually buy?
- Can IDS + bSDD encode enough residential checks to be useful without the full code text?
- Who is liable if an AI says a plan is “code compliant”?

## Generative design

- Can ResPlan (CC BY) replace RPLAN for a commercial generator at acceptable quality?
- Multi-storey + stairs + garages + sloped sites: which research code even attempts this?
- How to keep a human architect in the loop without turning the tool into “pretty massing”?

## BIM kernel

- FreeCAD+Bonsai vs IfcOpenShell headless vs Hypar Elements vs Revit-via-APS for *authoring* residential IFC from a graph?
- IFC4 vs IFC4.3 for a greenfield residential schema?
- How much furniture belongs in IFC vs glTF catalog sidecars?

## Physics

- Is a single-family EnergyPlus model worth it at schematic stage, or is a reduced-order model enough?
- Moisture / thermal-bridge checking: which engine is realistic for housing, not labs?

## Money

- Craftsman vs RSMeans vs local quantity-surveyor table for Metro Vancouver 2026?
- How to model Canadian mortgages (stress test, CMHC, uninsured) without giving financial advice?
- What is the unit-economics story: charge homeowners, architects, or builders?

## Catalogs

- Which manufacturer will sign a SKU+3D+price feed for a prototype?
- Is Coohom / a regional dealer catalog a faster path than chasing IKEA?

## Twin + robots

- For a single-family product, is the “twin” just Home Assistant + a glTF, or is USD-level sim required?
- Is Spot-class inspection in-scope for housing, or only for multi-family / production builders?

## Product

- First buyer: architect, production home builder, or land developer?
- First geography: Metro Vancouver only, or US IRC states?
- What is explicitly out of scope for 12 months?

---

These questions are the backlog for the modular Google Deep Research runs in [../prompts/GOOGLE_DEEP_RESEARCH.md](../prompts/GOOGLE_DEEP_RESEARCH.md).
