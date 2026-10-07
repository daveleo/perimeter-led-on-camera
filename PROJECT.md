---
name: Perimeter LED on camera
status: maintained
priority:
version: 
deadline:
next: None. Finished public article
updated: 2026-10-07
repo: daveleo/perimeter-led-on-camera
url: https://daveleo.github.io/perimeter-led-on-camera/
---

# Perimeter LED on camera

Technical article: how PWM operation of LED displays affects on-camera performance (refresh rate vs camera shutter, banding, flicker).

## What it is for

A public, vendor-neutral technical white paper on how an LED perimeter display looks on camera: how PWM operation, system frame timing and camera exposure interact (banding, flicker, refresh rate vs. shutter), and what to expect from a system commissioned for 50 Hz. For broadcasters, venue technicians, integrators and sales who need to explain or troubleshoot LED on camera. Includes interactive tools to check a given setup.

## How to run

- Read it online: https://daveleo.github.io/perimeter-led-on-camera/
- Locally: open `index.html` in a browser; no build step.
- Tools: `tools\pwm-explorer\index.html` (PWM & Camera Check) and `tools\pwm-explorer\advanced.html` (advanced simulator).

## How to use

- **Article** (`index.html`): 19 sections plus a one-page field guide, animated PWM and scope visualisations, shutter charts, a troubleshooting decision tree and a commissioning checklist.
- **PWM & Camera Check**: enter output frame rate, content frame rate, grayscale refresh (3200–15360 Hz) and scan ratio, brightness, a photo or test pattern, and the camera's frame rate, shutter, rolling shutter and genlock. It shows "naked eye vs. this camera" side by side, a plain-language verdict, banding and flicker readings, and tips to fix it.
- **Advanced simulator**: adds PWM scheme (conventional, S-PWM, BCM), driver clock and bit-depth limits, dimming method, per-channel RGB and cine shutter angle.

Pushing to `main` updates the public site.

## What is what

- `index.html`: the interactive article.
- `PWM_On-Camera_Performance_LED_Perimeter.md`: the same content as plain Markdown (source of record).
- `tools\pwm-explorer\`: the Check tool, the advanced simulator, and embedded demo photos (`img-data.js`).

## Current state

Finished and public (2026-09-08).
