# RONEL-FLIGHT-SIMULATOR
A modern, self-contained 3D flight simulator written in C++17 with **Qt 6** and **OpenGL 3.3 core**.
Everything is generated procedurally: the jet, the terrain, the airport, the sky and the sound. There are no asset files to install.
## Screenshots
<img width="1602" height="939" alt="fs" src="https://github.com/user-attachments/assets/f497129d-7cb4-460a-9909-c9ba99357555" />
<img width="1602" height="939" alt="f2" src="https://github.com/user-attachments/assets/44eba065-7976-4f9a-872f-086505ec1f53" />
<img width="1602" height="939" alt="fs3" src="https://github.com/user-attachments/assets/80c8b97c-cf7f-42fb-83c7-b11bb051ad2d" />
<img width="1602" height="939" alt="f4" src="https://github.com/user-attachments/assets/8b6ce0dc-d687-4f6f-9e8a-0a65d60d97c5" />

## Features

**Aircraft (3D, fully animated)**
- Detailed twin-fin supersonic jet built from ~8 000 triangles in 25 separate parts
- Moving ailerons, flaps, all-moving stabilators, twin rudders, airbrake panels
- Retracting nose and main landing gear, glass canopy, afterburner flame, navigation lights, strobe and beacon

**Flight model**
- 6-DOF rigid-body dynamics at 240 Hz, ISA atmosphere, thrust lapse, Mach effects
- Lift/drag polar with flap and gear drag, stall with buffet, AoA limiter
- Spring-damper landing gear, wheel brakes, nose-wheel steering, hull and sea contact (crash detection, landing report)
- Fly-by-wire assist (rate command / flight-path hold, turn coordination, auto-flare on landing) that can be switched off for raw control
- Autopilot: altitude, heading and speed hold
- Wind, turbulence, fuel burn

**World and rendering**
- Infinite procedural terrain: coast, forests, farmland, mountains with rock and snow, villages
- Streaming 4-level terrain LOD with skirts and fragment-level hole cutting
- Coastal airport with runway markings, taxiways, tower, hangars, approach lights and PAPI
- Animated ocean with Fresnel reflection and sun glint, procedural sky, stars, sun disc, soft billboard clouds
- Day/night cycle with sunset colours, moonlight, glowing runway lights, landing light, ground shadow
- Four cameras: chase, cockpit, orbit, tracking fly-by (mouse look and zoom)

**Cockpit and UI**
- Fighter-style HUD: pitch ladder, flight-path marker, speed/altitude tapes, heading tape, AoA, G, Mach
- Systems panel, autopilot panel, heading-up terrain minimap, warnings (stall, pull-up, gear, overspeed, fuel)
- Landing grading, pause and help overlays, menu bar, fullscreen
- Procedural audio (turbine, afterburner, wind, tyre rumble, stall horn) if Qt Multimedia is installed

## Controls

| Key | Action |
|---|---|
| Up / Down | Pitch (Up = nose down, Down = nose up) |
| Left / Right | Roll |
| A / D | Rudder, nose-wheel steering |
| W / S (or Shift / Ctrl) | Throttle up / down |
| Z / X | Full throttle (afterburner) / idle |
| Space | Wheel brakes |
| G | Landing gear |
| F / V | Flaps down / up |
| B | Airbrake |
| L | Landing light |
| E | Fly-by-wire assist on/off |
| K | Autopilot (then PgUp/PgDn altitude, `,` `.` heading, Home/End speed; W/S change speed target) |
| C or 1-4 | Cameras (mouse drag looks around, wheel zooms) |
| R / N | Reset on runway / air start |
| P or Esc | Pause |
| [ / ] , T | Time of day, let time pass |
| F5 / F6 / F7 | Clouds, visibility, wind preset |
| M, Tab, F11, H | Minimap zoom, hide HUD, fullscreen, help |

## Demo Videos
https://youtu.be/8bt8HuMchK8
