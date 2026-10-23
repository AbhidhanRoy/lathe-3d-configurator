# Lathe – Parametric 3D Model Generator

An interactive, browser-based configurator that generates real 3D geometry (vases, pen cups, bowls, towers) in real time and exports it as **STL** and **OBJ** for 3D printing.

**Live demo:** https://abhidhanroy.github.io/lathe-3d-configurator/

## Features
- Live sliders: height, base/belly/rim radius, belly position, ridges, ridge depth, twist, wall and floor thickness, mesh smoothness
- Presets and a randomiser
- Hollow or solid body
- Watertight mesh check, size, triangle count, volume and estimated PLA weight
- One-click export: binary STL (Z-up, slicer-ready), OBJ, and a JSON of the parameters, bundled as a .zip

## Tech
- JavaScript (vanilla), HTML5, CSS3
- Three.js (r128) for WebGL rendering and lighting
- Custom orbit/zoom controls (mouse, wheel, touch/pinch)
- Procedural mesh generation (surface of revolution with radial modulation) built directly as indexed `BufferGeometry`
- Hand-written STL/OBJ exporters and a minimal ZIP writer (CRC-32, no libraries)
- Edge-manifold check to verify the mesh is closed before printing

## Run locally
Open `index.html` in a browser. No build step.
