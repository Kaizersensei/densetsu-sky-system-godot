# Densetsu Sky System

Standalone Godot 4.6 sky and weather system extracted from the Densetsu project.

## What It Includes
- Time-of-day driven sky material and lighting control
- Seasonal weather selection and blending
- Cloud layer resources and compositing helpers
- Optional weather particle scene example
- Standalone demo scene at `engine3d/tests/Mesh Tester.tscn`

## Contents
- `engine3d/sky`
  Runtime scripts, data resources, and the main `DensetsuSkySystem3D.tscn`
- `shaders/sky`
  Sky and cloud shaders
- `assets/sky`
  Cloud textures used by the example setup
- `assets/textures/Sky`
  Moon texture used by the demo
- `assets/textures/weather_icons`
  Basic weather icon textures for the sample conditions
- `assets/weather`
  Minimal rain particle scene used by the demo

## Requirements
- Godot `4.6`
- No `Terrain3D` dependency
- No gameplay framework dependency

## Quick Start
1. Open the repo as a Godot project.
2. Run `engine3d/tests/Mesh Tester.tscn`.
3. Inspect the `DensetsuSkySystem3D` node in the scene.
4. Point it at your own `WorldEnvironment`, sun light, and moon light if you want to reuse it in another project.

## Typical Integration
1. Add `engine3d/sky/DensetsuSkySystem3D.tscn` to your scene.
2. Assign:
   - `world_environment_path`
   - `sun_light_path`
   - `moon_light_path`
3. Configure cloud layers and weather conditions in the inspector.
4. Optionally use the bundled `DensetsuSkyClock` or point the system to your own clock node.

## Notes
- The system auto-creates internal helper nodes for cloud compositing and moon-surface rendering.
- Weather particle scenes are optional. The included rain scene is only a minimal example.
- The example project keeps assets local and simple on purpose. It is meant as a reusable base, not a finished vertical slice.

## Scope
This repository is intended to provide the reusable sky and weather stack only. It does not include Densetsu gameplay code, terrain systems, or project-specific scene dependencies.
