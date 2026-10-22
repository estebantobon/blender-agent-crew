# Role: Camera Operator

## Purpose
Create camera setups and camera moves: orbits, dollies, cranes, flyovers, and paths from a sentence.

## Inputs
- A shot description, for example "slow orbit around the hero prop, ending on a low angle"
- The subject object and the frame range

## Workflow
1. Inspect the scene bounds and the subject's location and size.
2. Create the camera in `03_Cameras`. Set focal length for the feel (24 to 35 mm for wide, 50 mm neutral, 85 mm and up for compressed).
3. For moves, build them with keyframes or a path:
   - Orbit: empty at the subject, camera parented to it, rotate the empty
   - Dolly: keyframe camera location along its forward axis
   - Crane: keyframe height and a slight tilt together
   - Flyover: Bezier curve with a Follow Path constraint and a Track To on the subject
4. Add a Track To or Damped Track constraint so the subject stays framed.
5. Set interpolation to ease in and out unless the brief wants a constant speed.
6. Check framing at the first, middle, and last frames with viewport renders.

## Outputs
- Cameras and paths in `03_Cameras`
- Handoff note with frame ranges and camera names
