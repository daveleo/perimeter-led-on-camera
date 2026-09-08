# Perimeter LED on Camera

Technical white paper on how PWM operation, system frame timing and camera exposure
interact to determine the on-camera appearance of an LED perimeter display, and the
operating conditions expected for a system commissioned as a **50 Hz** installation.

Vendor-neutral. Hardware-specific timing is labelled *implementation-dependent*. All
waveforms and arithmetic use an explicitly simplified linear PWM model and are
illustrative, not a circuit description.

## Contents

| File | Purpose |
|---|---|
| `index.html` | Interactive single-page site — 19 sections + one-page field guide, animated PWM/scope visualisations, a PWM waveform explorer, shutter charts, a troubleshooting decision tree, a commissioning checklist and a downloadable CSV test template. Self-contained: no build step, no external JavaScript. |
| `tools/pwm-explorer/index.html` | **PWM &amp; Camera Check** — the simple, end-user tool. Output frame rate, content frame rate, grayscale refresh (3200–15360 Hz), a wide range of scan ratios, a real photo or test pattern, brightness, and camera frame rate / shutter / rolling-shutter / genlock. Shows a split "naked eye vs this camera" simulated recording, a plain-language verdict, banding / flicker readings and fix-it tips. Driver grayscale locked at 14-bit. |
| `tools/pwm-explorer/advanced.html` | **Advanced simulator** — adds PWM scheme (conventional / S-PWM / BCM), driver GCLK / bit-depth limits, OE loss, dimming-method split, per-channel RGB, cine shutter angle, a flicker spectrum with the shutter's frequency response, phase / shutter-sweep charts, a filmstrip, a driver-feasibility estimate, A/B compare and PNG / CSV / JSON export. |
| `tools/pwm-explorer/img-data.js` | Demo photographs (Lorem Picsum / Unsplash License) embedded for the Check tool. |
| `PWM_On-Camera_Performance_LED_Perimeter.md` | Plain-text source of record (same material, Markdown). |

## Publishing to GitHub Pages

1. **Settings → Pages**
2. **Source:** Deploy from a branch → `main` / `/ (root)`
3. Save. The site is served at `https://<owner>.github.io/<repo>/`.

## Revision

Rev 1.0. A vendor-specific annex (driver IC, receiving card, controller, scan file)
can be appended once the exact hardware and scan-file parameters are supplied.
