# Beyond the Horizon

A single-file, fully procedural Three.js (r160) world: a farmhouse, a drivable station wagon, five furry kittens, a cornfield, a windmill, a mirror-still stream, and a gigantic ray-traced black hole on the horizon.

Open `index.html` in a modern desktop or mobile browser. No build step, no assets.

## Controls

| Action | Desktop | Touch |
| --- | --- | --- |
| Look | Click the scene, then move the mouse | Drag |
| Move / run | WASD / Shift | Left joystick |
| Pick up · put down a companion, enter · leave the car | E | Hand / car button |
| Pet a held companion | Hold R or right mouse | Heart button |
| Feed a treat (held: from your fingers · on the ground: crouch, palm out) | F | Bowl button |
| Refill the food bowl (near the bowls or the sack) | E | Hand button |
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
- **Water reflections** (Medium and up) render the world mirrored in the stream at reduced resolution; grass joins the reflection from High.

## What lives here

- **Kittens** are sculpted from signed-distance fields (marching cubes) and covered in shell-rendered fur, with eyelids, irises, whiskers, toe beans and a bendable tail. They wander, groom, sulk, beg at an empty bowl, eat, flee a moving car, follow you, and walk back to the porch to sleep when night falls.
- **Hands** are modelled per pose (hold, pinch, open palm) with nails; holding, petting and hand-feeding each use their own pose.
- **Food**: kibble empties from the bowl as they eat and can be refilled from the sack; the water bowl ripples when they drink.
- **Car** collision uses the full body box against trees, shrubs, rocks, posts, fences, the house, the cornfield and the kittens.
- **Farm**: corn with ruffled, sheathed leaves, ears in husks with silk, tassels and brace roots; a washing line with shirt, jeans, tea towels, socks and a sheet held by wooden pegs; a scarecrow; the windmill and tank.
