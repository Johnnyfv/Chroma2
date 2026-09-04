# CHROMA

A full-screen, interactive WebGL visualizer. Five procedural 3D worlds, five color spectra, hidden controls, touch navigation, an automatic journey, and optional local audio reactivity.

## GitHub Pages — no build required

The downloadable ZIP puts `index.html` at its root. Upload the extracted files, not the ZIP itself.

1. Create a GitHub repository, or open the repository you want to use.
2. Choose **Add file → Upload files** and upload `index.html` to the repository root. Commit the upload to `main`.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Choose **main** and **/(root)**, then **Save**.
6. Open the address GitHub displays after deployment completes.

For a project repository, the address will normally be `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/`. All application code is embedded in `index.html`, so subdirectory hosting works without changing paths.

GitHub's publishing instructions: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

If using this source checkout instead of the downloadable ZIP, copy `dist/index.html` into the root of your GitHub repository.

## Controls

The interface fades after 6.5 seconds. The small button in the bottom-right corner always remains available. Press **H** or tap that button to reveal the control room.

| Action | Control |
| --- | --- |
| Reveal / hide controls | H / corner button |
| Rotate the view | Drag with mouse or one finger |
| Move closer / farther | Mouse wheel / two-finger pinch / Distance slider |
| Pause visual motion | Space |
| Change dimension | 1–5 |
| Change palette | C |
| Randomize | R / Surprise me |
| Full screen | F, when supported by your browser |

Auto journey changes worlds every 38 seconds of active playback. Switch it off to stay in a world. Visual motion and audio playback have separate pause controls.

## Dimensions

- **Chromatic Orbit:** a twisted luminous knot with fine latticework and orbital rings.
- **Velvet Wormhole:** an undulating, spiraling tunnel of light.
- **Prism Bloom:** a perforated, crystalline flower sphere.
- **Liquid Infinity:** an intricate gyroid sculpture.
- **Event Horizon:** a dark core surrounded by a luminous accretion disc.

Flow adjusts speed; Intricacy changes geometry detail; Radiance adjusts glow; Distance controls the view. Color palettes are Prismatic, Solar, Glacial, Iridescent, and Electric.

## Audio

Choose **Open music** for a local audio file. Browser codec support determines which files play; MP3, M4A, and WAV are common choices. Bass swells the form and light, while upper frequencies lift its radiance. **Pause audio** pauses the track. **Disconnect** releases the source.

**Microphone** asks your browser for permission. Incoming audio is analyzed locally and is not played back, recorded, or uploaded. Tap **Disconnect** or the Microphone button again to stop access. Microphone input requires HTTPS, which GitHub Pages provides. The microphone does not capture other tabs' internal audio directly.

## Compatibility and performance

Requires a browser with WebGL and fragment high-precision support. No external libraries, fonts, services, accounts, API keys, package installation, or build tools. The visualizer can also run by opening `index.html` on a computer; microphone access may be restricted for local files.

Adaptive resolution reduces the GPU workload on slower devices. Choose Battery saver for a cooler, lower-resolution experience. Full-screen availability varies by device and browser, especially on iPhone.

The page honors your device's reduced-motion preference by starting paused with Auto journey off. Resume from the control panel when desired. Motion pauses while the tab is hidden; manually started audio can continue playing. A visible message explains unavailable WebGL or a lost graphics context.

## Validation

JavaScript syntax and a simulated interaction check passed for startup, all world and palette buttons, control visibility, scene changes, uniforms, sliders, pause/resume, zoom bounds, drag, journey toggle, and the no-WebGL fallback. GPU shader compilation, visual output, and actual microphone/full-screen behavior were not tested in a real browser in the build environment.

## Files

- `index.html` — the entire application.
- `.nojekyll` — optional instruction to serve the files as static content.
- `README.md` — these instructions.
