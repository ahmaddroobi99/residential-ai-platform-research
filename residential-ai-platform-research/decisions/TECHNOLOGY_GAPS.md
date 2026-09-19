# Technology gaps

Things that do **not** currently exist as one integrated, shippable residential system.

---

## System-level

1. **No end-to-end open (or commercial) stack** that goes  
   land + zoning → code-checked generative house → IFC → energy/structure → priced BOQ → construction PM → twin → robot → Matter home.  
   Adjacent products exist. The joints are the product.

2. **GIS → BIM interoperability** is a research + vendor problem, not a solved library call. CRS, LOD, and “observed vs designed” models diverge (IFC vs CityGML vs LandInfra).

3. **Constraint-based generation that is simultaneously** spatial, structural, MEP, financial, and jurisdictional is not in any verified OSS repo. Commercial tools each own one or two axes (TestFit = yield + parking; Finch = unit plans; Forma = site climate; Solibri = model check).

4. **Lifecycle identity** — the same wall/window/SKU from sketch through as-built and warranty — is not preserved across typical file exports.

---

## Data and legal

5. **Best floor-plan training sets are research-restricted** (RPLAN, Graph2Plan, Matterport3D, Structured3D, LIFULL). ResPlan (CC BY 4.0) and CubiCasa5K (NC-SA) are the honest public options, with tradeoffs.

6. **No official public furniture API** that returns SKU + dimensions + 3D + price + inventory + lead time. IKEA has no public developer API. Scrapers collide with ToS.

7. **Cost data cannot be scraped into a product.** RSMeans forbids redistribution. Craftsman is licensed. Community unit-cost APIs are unverified.

8. **Building codes are copyrighted.** There is no national open IRC/IBC/NBCC rules API. Surrey zoning is a bylaw document. Code-checking products are rule engines plus human libraries, not a GitHub clone of the book.

9. **BC parcel/title truth is LTSA**, licensed. Regrid Canadian coverage must be verified per metro, not assumed.

---

## Technical joints

10. **IFC → real-time scene (glTF/USD)** drops semantics unless you carry a parallel graph.

11. **Generative plans → structural + MEP routing** is thin in OSS. You get rooms, not load paths or duct shops.

12. **Photo-to-interior AI** outputs pretty pixels, not measured BIM or real SKUs.

13. **Web IFC viewers fragmented.** That Open is the living line; older ifc.js viewer repos are stale.

14. **Physics stack licenses collide** (EnergyPlus permissive-ish vs Ladybug AGPL vs Bonsai GPL).

15. **Original 3DGS code is non-commercial.** Use a permissively licensed trainer if you ship.

16. **Residential construction SaaS APIs** (Buildertrend) are weaker / less evidenced than Procore.

17. **House-scale digital twin OSS** is generic IoT (OpenTwins) or prototypes (bim2twin), not BIM + physics + robots fused.

18. **Construction robots** that exist are layout printers, inspection quadrupeds, and commercial interior finishers — not a single-family home builder.

19. **Canadian mortgage / CMHC / stress-test** logic is a gap in the verified OSS mortgage repos (most are US).

20. **Human-factors “solvers”** (ergonomics, aging-in-place, privacy zones) exist as guidelines, not constraint engines.

---

## What this implies for an MVP

Do not wait for the missing platform. Own **one slice** and treat everything else as an adapter:

- Adapter: parcel + zoning + climate  
- Core: requirements JSON + plan graph + IFC stub + viewer  
- Adapter: energy check  
- Adapter: cost range (licensed table or human)  
- Explicit non-goals for v0: robot mason, full MEP, live municipal code API, IKEA checkout
