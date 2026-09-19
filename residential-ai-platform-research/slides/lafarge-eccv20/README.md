# Florent Lafarge — Data Structures for Piecewise-Planar Geometry

Reconstructed slide pack from the ECCV 2020 invited talk.

- **Talk:** [youtube.com/watch?v=2EL-0tDJtZk](https://www.youtube.com/watch?v=2EL-0tDJtZk)
- **Workshop:** [Holistic 3D @ ECCV 2020](https://holistic-3d.github.io/eccv20/)
- **Speaker:** Florent Lafarge, Inria TITANE
- **Duration:** 30 minutes

Open this README after you drop the images from the zip into this folder. Slides then render inline.

## One real frame from the video

![Official YouTube frame — Step 1 shape detection](https://img.youtube.com/vi/2EL-0tDJtZk/hqdefault.jpg)

Planes are detected on a mechanical object before they grow into a polygonal mesh.

## Slides (headlines)

1. **Title** — Data structures for piecewise-planar geometry. Florent Lafarge, Inria.
2. **The workshop** — Holistic Scene Structures for 3D Vision. Same room as House-GAN and Structured3D.
3. **The input** — Photogrammetry and LiDAR make dense meshes the default. A useful house model is still not.
4. **The old pipeline** — Poisson reconstruction, then simplify. Structure is an afterthought.
5. **The assumption** — Man-made scenes are piecewise planar. Walls, slabs, roofs.
6. **The question** — What is a good space-partition data structure?
7. **Delaunay** — Tetrahedra from the point set. Good scaffold, no walls.
8. **Arrangements** — Slice every plane through every other plane. Explodes after ~100 primitives.
9. **The kinetic idea** — Grow primitives until they collide. The partition stays light.
10. **Kinetic data structure** — A priority queue of collision events.
11. **KIPPI** — 2D kinetic polygons (CVPR 2018).
12. **Kinetic Shape Reconstruction** — Point cloud → growing planes → convex cells (TOG 2020).
13. **Extract the surface** — Inside/outside min-cut. Watertight polygonal mesh.
14. **Why it scales** — Order-of-magnitude more primitives than exhaustive assemblers.
15. **Why it matters here** — Scan → planes → IFC walls. A splat is a picture.
16. **Reuse** — KSR / KIPPI binaries exist. Do not invent a new kernel on day one.

After unzipping, the same headings embed `slide-01.png` … `slide-16.png`.

## Papers

- Kinetic Shape Reconstruction, TOG 2020 — https://hal.science/hal-02924409/
- KIPPI, CVPR 2018 — https://inria.hal.science/hal-01740958v1
- Repairing geometric errors in 3D urban models, ISPRS 2022 — BIM / CityGML / IFC
- Codes: https://www-sop.inria.fr/members/Florent.Lafarge/codes.html

We cannot download the YouTube file in this environment. The zip has reconstructed study cards plus the official thumbnail. For pixel-perfect frames run yt-dlp + ffmpeg locally.
