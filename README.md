# Scan-line-camera-v1

A browser prototype for testing the visual logic of the planned moving linear-CCD camera before building the hardware.

## What it does

- Uses the iPhone rear camera.
- Samples only the **vertical line at the centre** of the camera image.
- Repeats that sample at a selectable **scan rate**.
- Treats every sampled line as one strip of a new photograph.
- Simulates camera movement with a **virtual movement speed**.
- Lets you change spatial scaling and export the result as PNG.

## Important

This is not a real linear CCD. The iPhone still captures a normal 2D rolling-shutter image. The app simply extracts its centre line repeatedly so the resulting image behaves conceptually like a line-scan camera.

Camera access requires HTTPS.

## Suggested experiment

1. Set **Scan rate** to 30 lines/s.
2. Start the camera and start scanning.
3. Move the phone sideways across a scene at a steady speed.
4. Pause.
5. Repeat at the same scan rate while moving approximately 2×, 3× and 5× faster.
6. Compare how the spatial geometry changes.
7. Then change the scan rate while keeping your physical movement approximately constant.

The point is to understand the relationship between **line acquisition frequency** and **physical movement**, which will later become the core calibration problem of the real camera.

## GitHub Pages

This repository contains a single static `index.html`, so it can be hosted directly with GitHub Pages. After enabling Pages for the repository, open the HTTPS Pages URL on the iPhone and allow camera access.
