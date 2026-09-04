# CHROMA II — Higher Dimensions

A self-contained, GitHub Pages-ready visualizer inspired by luminous geometric shells, layered waves, and fine neon strands.

## Publish

Extract the ZIP and upload `index.html` to the root of your GitHub repository, replacing the previous version. In Settings → Pages, select Deploy from a branch → main → /(root) → Save. No build, installation, API keys, or dependencies are needed. The optional `.nojekyll` file is included.

## What's new

- Nested tesseracts: 16 vertices and 32 edges per hypercube, rotated through 4D and projected into 3D.
- Crystal lattices: connected cubic networks with diagonal crystal bonds.
- Nested 24-cells: 24 vertices and 96 edges per four-dimensional polytope.
- Geodesic crystals: layered, subdivided icosahedral shells.
- Hopf-inspired weaves: linked-looking circular fibers rotating through 4D.
- Hyperblooms: stacked, undulating geometric contours.
- Continuous vertex morphing across all six structures, without black scene transitions.
- Touch ripples, localized bending, rotational drag, and pinch zoom.
- An audio rewrite with a persistent player, gesture-based audio activation, a connected silent microphone analysis path, sensitivity control, and a live level meter.

The tesseract and 24-cell begin with their mathematical vertices and edges. Touch, audio deformation, and the in-between morphs intentionally alter those shapes for artistic expression. Hopf Weave is an artistic construction, not a complete mathematical visualization of the Hopf fibration.

## Controls

Tap the bottom-right button or press H to open the hidden control panel. Text fades after 6.5 seconds.

- Drag: orbit the structure.
- Hold: bend and ripple the geometry.
- Pinch or scroll: travel closer or farther away.
- 1–6: choose a form; it morphs into place.
- Space: pause / resume visual motion.
- C: change spectrum.
- R: surprise me.
- F: full screen when supported.
- Continuous morph: automatically move to another form every 16 seconds, with a 10-second transition.
- Intricacy: rebuild the structure with different detail, morphing into the new form.

## Music

Open the deployed HTTPS page directly in Safari or Chrome for the most reliable audio support. An embedded preview or file viewer may restrict audio or microphone access.

Choose Open music and select an actual, unprotected audio file. A native playback bar appears. If automatic playback is blocked, press Play / resume or the player's play button. Audio decoding depends on your browser; common choices are MP3, M4A, and WAV. Streaming-service tracks and DRM-protected downloads cannot be loaded as ordinary files.

The signal meter shows the level being analyzed. Increase Audio sensitivity if the response is subtle. Bass expands the structure and upper frequencies brighten it. Visual pause and audio pause are separate controls.

## Microphone

Tap Microphone and grant access. The input is analyzed locally and routed through a silent output path; it is not recorded, uploaded, or played back. Speak or play music near your device and watch the meter. Tap Disconnect to release microphone access.

Microphone access requires HTTPS and browser permission. It does not directly capture internal audio from another app or browser tab. If denied, enable microphone permission in your browser's site settings and try again.

## Notes

No testing was performed for this revision, as requested. The audio changes are implemented but have not been confirmed on a physical device.

The experience uses WebGL and requires hardware/browser support. Render quality can be lowered for battery life. Reduced-motion preferences start the animation paused and continuous morphing off. Full-screen support varies, especially on iPhone. No external requests or dependencies are used by the application.

This ZIP contains the application and instructions only. Uploading it does not change the previously hosted CHROMA Site.
