# Sky System for Godot

Standalone Godot 4.6 sky and weather system for general-purpose use.

## What It Includes
- Time-of-day driven sky material and lighting control
- Seasonal weather selection and blending
- Cloud layer resources and compositing helpers
- Optional weather particle scene example
- Standalone demo scene at `demo/sky_system_demo.tscn`

## Contents
- `engine3d/sky`
  Runtime scripts, data resources, and the main `SkyWeatherSystem3D.tscn`
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

## Quick Start
1. Open the repo as a Godot project.
2. Run `demo/sky_system_demo.tscn`.
3. Inspect the `SkyWeatherSystem3D` node in the scene.
4. Point it at your own `WorldEnvironment`, sun light, and moon light if you want to reuse it in another project.

## Typical Integration
1. Add `engine3d/sky/SkyWeatherSystem3D.tscn` to your scene.
2. Assign:
   - `world_environment_path`
   - `sun_light_path`
   - `moon_light_path`
3. Configure cloud layers and weather conditions in the inspector.
4. Optionally use the bundled `SkyClock` or point the system to your own clock node.

## Notes
- The system auto-creates internal helper nodes for cloud compositing and moon-surface rendering.
- Weather particle scenes are optional. The included rain scene is only a minimal example.
- The example project keeps assets local and simple on purpose. It is meant as a reusable base, not a finished vertical slice.

## Scope
This repository is intended to provide the reusable sky and weather stack only. It does not include gameplay code or project-specific scene dependencies.
