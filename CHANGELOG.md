# Kineto Changelog

The short version of each entry also appears in the app: **File ▸ What's New in Kineto…**

## 0.2.1 — August 3, 2026

Same-day fix for 0.2.0.

- **The graph editor's easing buttons work again for keyframes selected in the timeline.** Selecting a keyframe in the timeline expands to one selection entry per channel in the graph editor, which tripped the multi-select safety rule and made every easing button (and Paste) silently do nothing. Keyframes clicked directly in the graph were unaffected.

## 0.2.0 — August 3, 2026

The largest release yet: a 49-item UX pass driven by beta-group feedback, plus a month of new surfaces.

**Keyframes & easing**

- **Keyframes draw their own easing.** A dome means ease, a square means hold, a peak means linear — the left half is how the motion arrives, the right half is how it leaves. Read an animation's timing straight off the timeline without opening the graph editor.
- Keyframes packed too tightly to read collapse into a **counted cluster badge** — drag it to move the whole run together; zoom in to edit them individually.
- Bounce and elastic presets draw their **real parametric curves** in the graph editor (bezier handles hide, since they can't affect those easings).
- Inserting a keyframe mid-curve no longer reshapes the easing around it — the segment splits exactly.
- Easing presets are available from the timeline toolbar, not just the graph editor.
- ⌥-drag a keyframe to duplicate it; ⌥-click a curve to add a keyframe at that time and value.
- Copy/paste individual keyframes (time + value) to another time or layer; deleting with only X keyframes selected leaves Y alone.
- Per-axis parameter colours and a stable property order in the graph editor; separated dimensions get their own timeline rows.

**Command palette**

- **⌃Space opens a searchable palette** covering effects, geometry operators, modifiers and menu commands. Star a result to pin it as a favourite.

**Undo**

- History holds **500 steps** (was 100).
- Colour and gradient drags land **one undo entry per drag** instead of flooding the history.
- Folder moves, layer-speed changes and Comp Settings edits are undoable.
- Undoing away a freshly drawn or duplicated layer reselects what you had selected before.

**Duplicate**

- **⌘D / ⌥-drag now carries keyframes, modifier stacks and effects** — the copy animates like the original instead of freezing at the current frame.

**Viewer**

- **Rulers + guides** (⌘R): drag guides out of the rulers, right-click for px ↔ % units, and visible guides snap layer, vertex and mask drags. Snapping includes the grid.
- Snap, Grid and Rulers (plus grid size and ruler units) remember their state across launches.
- Bigger viewer toggle icons; the comp edge no longer shows through the tab bar when zoomed in.

**Tools & text**

- **Convert text to outlines** (button in text properties).
- The text tool's options bar carries fill, stroke, font, size, style, alignment and stroke width.
- Adjustment layers **actually work now** — they apply their effects to everything below them.
- Adding a null while layers are selected parents those layers to it.
- The Geo / Effects / Mods buttons open searchable pickers instead of inserting instantly; the geometry list splits into Generators and Effectors.
- Text renders crisper, without the dark edge fringe.

**Geometry**

- **Bake to Layers** turns every repeater/scatter copy into a real, individually editable layer (the source rig stays, hidden — one undo step).

**Import & export**

- ProRes 4444 and PNG frame exports carry a **real alpha channel**.
- .tiff files import; unsupported .heic is rejected with a clear message instead of importing blank; images larger than the GPU limit downscale instead of importing blank.
- Drag a .obj file into the app to import it; imported models show full 3D position and rotation.

**Windows & diagnostics**

- Native controls (scrollbars, dropdowns) follow dark mode.
- Fixed the viewer collapsing after minimize/restore.
- The app writes a rotating log file, and **Help ▸ Show Log Folder** opens it — include the newest log with bug reports.

**Fixes**

- Deleting keyframes deletes exactly what you selected; dragging a multi-keyframe selection no longer drops it on release.
- 3D lights respect the parent chain, directional lights aim where they're rotated, and the brightest four win when a scene has more.
- The render dialog remembers your last export folder; images and PDFs no longer show a mute button.
- The effect picker no longer hides behind the timeline, dropdown menus no longer render white, and a moved keyframe no longer flashes back at its old spot.

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
