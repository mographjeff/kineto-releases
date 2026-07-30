# Kineto Changelog

The short version of each entry also appears in the app: **File ▸ What's New in Kineto…**

## 0.1.9 — July 30, 2026

Stability release, driven by the first field crash reports from 0.1.8.

**Stability**

- **Fixed a crash with many shape layers.** GPU memory for shape anti-aliasing is now shared across layers instead of allocated per layer, so comps with hundreds of shape layers no longer exhaust GPU memory. This hit hardest on Windows, where dedicated video memory is a fixed budget.
- **Much lower GPU memory use while zooming** the viewer.
- **GPU errors no longer crash the app.** The frame recovers and the error is reported instead (if crash reporting is enabled).

**Fixes**

- Deleting or renaming a composition now shows a message when it can't be done (such as deleting the root comp), instead of silently doing nothing.

## 0.1.8 — July 29, 2026

**Animation & easing**

- **Rebuilt graph editor.** Drag bezier handles directly on the curve to shape custom easing, with a toolbar of one-click presets, numeric handle fields, and a drawer for saving your own presets. Custom cubic-bezier easing is reachable from the UI for the first time.
- **Multi-select keyframes** in both the timeline and the graph editor: shift-click or drag a marquee, then move them as a group or re-ease them all at once.
- **Quick-ease per side.** The ease buttons now apply to the incoming side, the outgoing side, or both.
- The graph editor shows every selected layer at once, with click-to-solo layer headers.
- Keyframes are now visible on all timeline layers, not just the selected one, and drag with a live preview.

**Performance**

- Smoother 4K playback and faster effect rendering (reader fast path, natural-size quads, texture pooling).
- Video export is roughly 1.3–2x quicker — the writer now runs on its own thread with double-buffered GPU readback.

**Keying**

- **Screen Pre-blur** cleans up speckled mattes: it feeds matte analysis only, so your output colors and despill stay sharp.
- **Screen Softness** now feathers the matte edge spatially, in pixels (0–100), instead of narrowing the key.

**New tools**

- **Motion paths in the viewer** — see and drag position keyframes directly on the canvas.
- Two new geometry operators: **Smooth** and **Round Corners**.
- The audio meter is now its own dockable panel.

**Interface**

- Redesigned welcome screen, with a link to the new Kineto Discord.
- Panel title bars now host their own controls: the timeline transport is centered with timecode and loop mode, and the graph editor's easing tools live in its bar.
- Frame-step shortcuts (⌘←/⌘→, PageUp/PageDown) and Home/End to jump to start/end.

**Windows**

- **Fixed a black screen on launch** affecting some NVIDIA machines. Kineto now defaults to the DX12 backend, which composes correctly with the WebView2 layer. Set `WGPU_BACKEND` to override.
- **Installers are now code-signed** via Azure Trusted Signing — no more "unknown publisher" warning.

**Other**

- Opt-in crash reporting. Enable it in Settings to send anonymous crash reports; it's off unless you turn it on.

## 0.1.7 — July 24, 2026

- **Automatic updates on Windows.** Kineto now updates itself in place — a passive progress-bar install, no more re-downloading installers. Installs from 0.1.6 onward pick this up automatically.
- **What's New dialog** (File ▸ What's New in Kineto…) — opens once automatically after each update.
- Update prompts now include release notes so you can see what you're getting before installing.

## 0.1.6 — July 24, 2026

**Fixed**
- Sliding a layer in the timeline now carries its keyframes with it, and they follow live while dragging.
- Deleting keyframes keeps the layer's current pose instead of snapping back to its pre-animation state.
- Rotating with the gizmo past a full turn no longer jumps by 360° or produces huge values.

**New & improved**
- Rotation displays as revolutions + degrees ("2x + 45°"), with no ±360 cap. Type either notation.
- Shift-drag while drawing a shape constrains it to a perfect square / circle.
- Shift-drag the playhead to snap to keyframes and layer in/out points.
- The keyframe stopwatch now **adds** a keyframe at the current time. Alt-click it — or right-click a keyframe in the timeline — to delete all keyframes.
- Driver/Linear modifiers can target **Scale (X+Y linked)**, driving both axes while preserving aspect.
- Selection boxes hide during playback for smoother previews.
- Linked axes (Position/Scale) show a chain-link icon instead of a padlock.
- Switching a composition between 2D and 3D is now a single undo step.

## 0.1.5 — July 23, 2026

- **First Windows build.** Kineto now runs on Windows 10/11 (x64): full editor, GPU renderer, video + audio import and playback.
- Windows installer ships unsigned for now — SmartScreen shows "More info → Run anyway".

## 0.1.4 and earlier

macOS beta releases: camera & lens upgrades (DOF quality tiers, focal-length lens presets, separate position dimensions), the timeline/text/3D-primitives UX batch, scrub & playback performance work, and the initial public beta.
