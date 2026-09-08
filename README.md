# CHROMA II 2.1 — iPhone / Safari update

A self-contained, GitHub Pages-ready visualizer inspired by luminous geometric shells, layered waves, and fine neon strands.

## Startup repair and iPhone changes

The previous source used different default precision for shared uniforms and varyings in its vertex and fragment shaders. WebGL 1 can reject that pairing during shader linking. Both stages now receive matching precision declarations, selected from the graphics device's supported fragment precision. The old generic instruction to switch browsers has been replaced with actual shader error details if startup still fails.

On touch devices this version uses 1,536 line segments (desktop: 2,304), 88 glow nodes (desktop: 160), a default 1× render scale, a 1,440-pixel long-edge cap, and a 30 fps target. High definition opts into a 60 fps target and higher resolution. Targets depend on the device's available performance. Automatic quality can lower resolution further when rendering falls behind. Geometry buffers are reused between morphs and the audio meter updates at most ten times per second.

Touch controls have larger targets, safe-area spacing, landscape support, and viewport handling for Safari's changing toolbar. The canvas releases depth and stencil buffers it does not use. Pause/resume after changing tabs resets timing and clears stale touches.

No browser tests, automated tests, or device tests were run for this revision, as requested. This is a code-level repair; successful loading on your iPhone is not yet confirmed.

## Publish

Extract the ZIP and upload `index.html` to the root of your GitHub repository, replacing the previous version. After GitHub Pages finishes updating, reload the page. If an older copy appears, open your usual address with `?v=2.1` at the end to request a fresh URL. In Settings → Pages, select Deploy from a branch → main → /(root) → Save. No build, installation, API keys, or dependencies are needed. The optional `.nojekyll` file is included.

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
