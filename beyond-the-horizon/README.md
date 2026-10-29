# Beyond the Horizon

A single-file, fully procedural Three.js (r160) world: a farmhouse, a drivable station wagon, a few tiny companions, and a gigantic ray-traced black hole on the horizon.

Open `index.html` in a modern desktop or mobile browser. No build step, no assets.

## Controls

| Action | Desktop | Touch |
| --- | --- | --- |
| Look | Click the scene, then move the mouse | Drag |
| Move / run | WASD / Shift | Left joystick |
| Pick up · put down a companion, enter · leave the car | E | Hand / car button |
| Pet a held companion | Hold R or right mouse | Heart button |
| Feed a held companion | F | |
| Drive | W/S throttle, A/D steer, Space brake, V switch view | Joystick |
| Cinematic director | C | Film button in the dock |
| Next wallpaper location | L | Pin button in the dock |
| Day / night | N | Sun / moon button |
| Black hole on / off | B | Settings panel |
| Wallpaper mode (hide UI) | H, Esc to leave | Tap |

Everything else (black-hole size, living day/night cycle, render distance, resolution, wind, exposure, creatures, clouds, mist) is in the settings panel (gear icon in the dock that appears at the bottom edge).

## Performance

Rendering happens entirely on the viewer's GPU, so hosting (GitHub Pages, Vercel, a local file) does not change frame rate — it only affects download time.

- **Resolution** is a manual setting and is never lowered automatically.
- **Render distance** (Low → Ultra) controls grass radius and density, shadow refresh rate, sky/black-hole render scale and ray-march steps, and MSAA. With **Auto** enabled the world steps render distance down when the frame rate drops below ~42 fps and back up when there is headroom, without touching resolution.
