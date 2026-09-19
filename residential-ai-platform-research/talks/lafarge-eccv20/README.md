# Florent Lafarge — Data Structures for Piecewise-Planar Geometry

Slides and frames from the ECCV 2020 invited talk.

- **Watch:** [youtube.com/watch?v=2EL-0tDJtZk](https://www.youtube.com/watch?v=2EL-0tDJtZk)
- **Workshop:** [Holistic 3D @ ECCV 2020](https://holistic-3d.github.io/eccv20/) · 23 Aug 2020, 13:30–14:00 UK
- **Speaker:** Prof. Florent Lafarge, Inria / Université Côte d’Azur
- **Length:** 30 minutes

Open this README. Pictures that are already on GitHub or hotlinked will render inline.

---

## Official YouTube frame (real slide from the talk)

**Headline:** Step 1 — shape detection  
A mechanical assembly is split into colored planar primitives. This is the official preview frame of the video.

![Shape detection](https://img.youtube.com/vi/2EL-0tDJtZk/hqdefault.jpg)

---

## What the talk argues

1. Buildings, rooms, and machines are mostly planar. Dense triangle soups hide that structure.
2. Detect planar primitives first. Do not build a foam mesh and then simplify it.
3. Do not slice every supporting plane. Grow the detected planes until they collide (kinetic data structure).
4. Cut a watertight polygonal surface out of the resulting polyhedral partition (min-cut).
5. The 2D rehearsal is KIPPI (CVPR 2018). The 3D method is Kinetic Shape Reconstruction (ACM TOG 2020).

---

## Frame captions (from the recording)

### Frame A · Step 1: shape detection
**Headline:** Detect the planes before you build a mesh.  
Input scan on the left. Colored planar parts on the right. Later steps only assemble these parts.

### Frame B · Related work: shape reconstruction
**Headline:** Kinetic growth is the alternative to exhaustive slicing.  
Cubes expand until they collide. That picture is the 3D intuition for the whole talk.

### Frame C · Results on satellite images
**Headline:** The 2D version already works on city-scale imagery.  
KIPPI-style polygonal partitions on satellite photos — fewer cells, façades kept.

### Frame D · Paper teaser
**Headline:** Buildings and rooms as planar solids.  
Scan / photogrammetry on top. Concise piecewise-planar mesh underneath.

Local copies of these frames live in the zip (`yt-hq.jpg`, `yt-1.jpg`, `yt-2.jpg`, `yt-3.jpg`, `frame-00-paper-teaser.jpg`). Drag them into this folder if you want them to render on GitHub without hotlinks.

---

## Study slides 01–16

These 16 cards reconstruct the argument. Image files `01.png` … `16.png` are in the zip. After you drop them here they will render below.

| # | Headline | One or two lines |
|---|---|---|
| 01 | Title | How range images, laser scans, and multi-view stereo become simple planar models. |
| 02 | Workshop context | Holistic 3D wants planes and regularity, not million-triangle soups. |
| 03 | The problem | Input: points. Output: a watertight mesh of large planar facets. |
| 04 | Failure mode | Foam-then-simplify either keeps too many faces or destroys the planes. |
| 05 | The idea | Grow the planes at constant speed. Stop at collisions. |
| 06 | Kinetic DS | Guibas 2004: certificates and a collision queue. Time is events. |
| 07 | KIPPI | 2D: detect line segments, grow them until they meet. CVPR 2018. |
| 08 | 2D uses | Polygons are a domain for labeling: contouring and footprints. |
| 09 | 3D step 1 | Detect planar shapes. Detection quality bounds everything later. |
| 10 | 3D step 2 | Grow shapes until they collide. Growth fills missing data. |
| 11 | Events | Vertex–edge and vertex–face collisions. Sliding vertices are expensive. |
| 12 | 3D step 3 | Min-cut labels cells inside/outside. The cut is the surface. |
| 13 | Results | Buildings stay planar. Freeform shapes get a compact stand-in. |
| 14 | Efficiency | About 10× more shapes than prior assemblers. |
| 15 | Applications | Airborne buildings, indoor rooms, later urban-mesh repair. |
| 16 | Takeaway | Do not slice every plane. Grow, collide, cut. |

![01](01.png)

![02](02.png)

![03](03.png)

![04](04.png)

![05](05.png)

![06](06.png)

![07](07.png)

![08](08.png)

![09](09.png)

![10](10.png)

![11](11.png)

![12](12.png)

![13](13.png)

![14](14.png)

![15](15.png)

![16](16.png)

---

## Papers

| Paper | Venue | Link |
|---|---|---|
| KIPPI: KInetic Polygonal Partitioning of Images | CVPR 2018 | [HAL](https://inria.hal.science/hal-01740958v1) |
| Kinetic Shape Reconstruction | ACM TOG 39(5), 2020 | [HAL](https://hal.science/hal-02924409/) · [DOI](https://doi.org/10.1145/3376918) |
| Planar Shape Detection at Structural Scales | CVPR 2018 | Fang, Lafarge, Desbrun |
| Repairing geometric errors in 3D urban models | ISPRS 2022 | Yu, Lafarge et al. |

Author page: https://www-sop.inria.fr/members/Florent.Lafarge/
