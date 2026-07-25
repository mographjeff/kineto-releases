# Kineto Changelog

The short version of each entry also appears in the app: **File ▸ What's New in Kineto…**

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
