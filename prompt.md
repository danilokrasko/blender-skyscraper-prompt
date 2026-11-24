You are an expert Blender 4.x technical artist. Build a supertall skyscraper in Blender using Python (bpy), step by step, so the build is visible and satisfying to watch.

GOAL
A Burj Khalifa-style tower, ~600 m tall, built floor by floor from the ground up, ending with a spire. It must look good both in the viewport and in a final render.

STRUCTURE
1. Clear the default scene. Set units to metric.
2. Base: a wide 3-level podium with a Y-shaped footprint (three wings at 120 degrees).
3. Tower: 160 floors, each floor 3.8 m high, as separate objects named Floor_001 ... Floor_160.
   - The three wings step back in a spiral as the tower rises (setbacks every 20 floors).
   - Each floor = floor slab + glass curtain wall + thin vertical steel mullions.
4. Setback terraces: orange accent bands (structural / mechanical floors) at every setback.
5. Crown and spire: tapering crown, then a slender spire to the top.
6. Organize everything into collections: Podium, Floors, Accents, Spire, Lighting.

MATERIALS
- Glass: blue reflective glass (Principled BSDF, high metallic, low roughness, slight transmission).
- Steel frame: dark brushed metal.
- Accent bands: bright orange (#FF6A1A), slightly emissive.
- Spire: polished silver.

BUILD ANIMATION (important)
- Keyframe the build so the tower grows from the ground up over 20 seconds at 30 fps: each floor scales from 0 to 1 on Z (or rises into place) one after another, with a small overshoot bounce.
- The spire appears last with a quick extend animation.

CAMERA AND LIGHT
- A camera that slowly orbits the tower and tilts up as it grows, ending on a low hero angle looking up at the spire.
- Sunset lighting: warm orange sun + purple/pink sky (Nishita sky or gradient world).
- City at dusk: add a simple ground plane and a few low-poly surrounding buildings with lit windows.

OUTPUT
- Render engine: Eevee, 1080x1920 (vertical, for social media), 30 fps.
- Use clean, commented code split into functions: build_podium, build_floor, build_spire, add_materials, animate_build, setup_camera, setup_lighting.
- Run each stage separately and tell me what was built after each stage, so I can watch the tower grow.
- At the end, print the stats: total floors, height in meters, object count.
