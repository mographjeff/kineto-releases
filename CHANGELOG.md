# Brio Changelog

The short version of each entry also appears in the app: **Help ▸ What's New in Brio…** (Kineto became Brio in 0.5.0.)

## 0.5.0 — September 17, 2026

Kineto is now Brio. This release brings the store online, a full particle system, the complete layer-style set, shape layers that select like layers, an importer for After Effects projects, and a long list of timeline, Library and 3D work from the September testing rounds.

### Brio

- **The app is Brio.** Every name, menu, file and dialog says Brio now — *con brio*, the musical direction for "with spirit". Your projects, presets, settings and licence are untouched by the rename, and installs update in place.
- A new app icon, drawn on the macOS icon grid. The site is [brio.art](https://brio.art).

### Buying a licence

- **Brio is $299, once.** Every 1.x update is included, free and forever; Brio 2 will be a separate purchase. Nothing expires and there is nothing to renew.
- **Settings ▸ Licence** takes your key and activates this computer. A licence covers two computers; **Deactivate This Computer** frees a seat so you can move it. **Check Now** re-confirms with the store, and Brio keeps working offline between checks.
- **The trial never locks you out.** A trial that has ended keeps opening, editing and saving; only renders carry a watermark until a key is entered. The render dialog says so before it starts, with a link to the Licence pane.

### Particles

- **A particle layer.** Emitters, physics and forces, with trails, bursts on death and puffs on bounce as auxiliary systems. Particles can be 2D shapes with softness, **sprites made from any layer**, or **3D meshes** with instanced shadows, lit billboards and light emitters.
- **Soft particles** fade into the surface behind them instead of cutting a hard line; **shadowlets** let billboards and sprites cast their silhouette; **volumetric particles** fill a volume with fog that the scene's lights ray-march through.
- **A path emitter** births particles along a shape or text layer's outline.
- **Every simulation parameter keys**, animated fields update the moment you set a keyframe, and **over-life graphs** shape each particle's size, opacity and colour across its life. Orientation follows motion or stays fixed in the world.
- **The Library's Particles tab** holds a 33-preset pack with hover loops, and the Library's sprites and objects are ready to use as particles.

### Layer styles

- **The full set:** Drop Shadow, Inner Shadow, Outer Glow, Inner Glow, Bevel & Emboss, Satin, Colour Overlay, Gradient Overlay and Stroke, each with blend modes and undo, an eyedropper for colours, and a master switch. The Colour Overlay alpha bug is gone.
- **Glows gain a Bloom technique** that falls off like real light, and bloom in 3D comps is realistic by default. Effect and style rows use the same pill switch and dim when off.

### Shape layers

- **Select the layer, edit every shape.** Click a shape layer and an edit reaches all of its shapes; pick groups and individual shapes as a real selection when you want just some. **⌘G groups shapes.**
- **A group can be painted.** A fill and stroke on the group draws over its shapes merged into one path; the paint is remembered when switched off and seeded from what's on screen. Fill and Stroke twirl closed, and a painted group shows only its own paint.
- **Booleans keep their exact curves**, and a Pie reaches the edge of its shape. Name a shape by double-clicking it; the shape list reads top-down like the layers do.
- Aligned strokes no longer tear at a deep concave corner, and a contour that returns to its start is treated as closed the way Illustrator draws it.

### Import from After Effects

- **File ▸ Import from After Effects…** reads a file written by the **BrioExport** script, which ships inside Brio. Comps arrive with their layers, keyframes and easing, masks, mattes, effects and layer styles, built in dependency order. It's an early cut — tell us what it misses.
- A `.brio.json` dropped on the window or picked from **File ▸ Import…** opens the same dialog.

### Timeline

- **Markers.** ⇧M adds one at the playhead; drag to move, ⇧-drag to snap to the playhead, layer in and out points and keyframes; a right-click menu, undo, and **Lock Markers**. Only a left-click removes a comp marker.
- **U and P/S/R/A/O show and hide rows the After Effects way:** each shows only its property, ⇧ adds it to the rows already showing, and each toggles its own row without closing the others.
- **Property rows show their value at the playhead** and scrub it; edits reach every selected layer, and Scale has a link button. Drag across twirls, or the toggle columns, to set many rows at once. Drop a layer anywhere below the last row to send it to the bottom.
- The timeline and graph editor **scroll when a drag reaches their edge**, at the same speed on any refresh rate. **Time Remap** sits in a clip's right-click menu. Vector drawing layers show their drawing-frame blocks. The audio bar says Waveform.

### Library

- **A Motion tab.** Save a layer's transform animation from its keyframes as a Motion preset, and apply it to other layers.
- **Text presets that play on hover**, including new Spring and Bounce presets; double-click applies one to a selected text layer, and **My Presets** saves your own text animators. New text layers from the Library say Hello World.
- Library tabs are icons, and Environments are HDRIs. The Geometry Operators panel puts presets first and keeps both add buttons in view.

### 3D and geometry operators

- **Operators gain depth.** Offset Z, Rotate X/Y and Scale Z on geometry operators; Wiggle and Falloff work in depth; extruded shapes draw their operators, effectors and trim. Bakes keep each copy's Z position, rotation and Color operator result.
- **Every stack has a master switch** — Effects, Geometry Operators and Effectors each get their own — plus **Copy**, **Paste** and **Reset** for a whole stack, and **Remove All Effects** at the top of the Effects menu. Effectors get their own header.
- The falloff gizmo is a sphere, and each one has its own colour. Operator depth rows appear in 3D comps. A donut is called Donut. The Scene layer hides in a 2D comp, and the camera tool's cursor shows its sub-tool.

### Text and animation

- **A Range visualizer** draws the text, the range and its curve on one axis, with a Reverse button. Spring and Bounce curves for text selectors; Spring on a reveal pops up and then wobbles.
- Canvas text editing draws its own caret on the letters you see. Multi-line text: line breaks stop counting as characters and blank lines keep their place. The Properties text field keeps line breaks.
- **Blend Colours Using 1.0 Gamma** is a project switch, on by default, for linear-light blending. Fades and colour animation change at After Effects' rate. Ease In and Ease Out no longer flatten the other half of a custom curve.
- Drag a layer you haven't selected, even when it has keyframes; the motion path draws live as you go. Blend-mode hover previews fold into one undo step.

### Export

- **Lottie export carries transform keyframes**, and shape groups get the transform item lottie-web needs to render at all. A finished Lottie job in the render queue gets a **Preview** button that opens it in the previewer.
- SVG import: a raster embedded in the file becomes a footage layer where the file put it.

### Devices

- **Snaps and finished renders tap the MX Master 4** and the trackpad. The Logi Options+ plugin ships inside Brio; the haptic settings live in Settings ▸ Appearance.

### Fixes

- **Renders stop writing stale frames, and text stops glitching on PCs.** A GPU that keeps failing now logs three lines instead of seven million, which was what silently dropped frames.
- Deleting the last comp empties the project instead of refusing; undoing past the root comp no longer takes the app down with it, and a command that panics is rejected instead of aborting the app.
- Removing an effect removes its keyframes too; Copy Effect carries the edits you can see; deleting or reordering the first shape no longer eats the layer's effect keyframes.
- Deleting a collapsed-row keyframe also deletes Scale Z, and deleting a separated scale's keyframes keeps its value. Spring and Bounce Scale Up run 36 frames at the comp's rate.

## 0.4.1 — September 9, 2026

A Figma frame becomes a Kineto composition, with the designer's layer tree intact rather than a flat picture of it. Kineto also runs on Linux for the first time.

### Import from Figma

- **File ▸ Import from Figma…** takes a link from Figma's **Share ▸ Copy link**. A frame arrives as a composition built the way it was designed: every frame and group a layer group, every text box an editable text layer in its font, size, weight and colour, every shape a shape layer with its fills, strokes and gradients. Import one frame, or every frame in the file at once, each as its own comp.
- **Photos come across as footage**, fitted the way Figma fits them and cropped to their shape, so rounded photo cards keep their corners. A drop shadow becomes the layer's Drop Shadow style, a layer blur a Gaussian Blur, and a Figma mask a hidden layer that the layers above it use as their track matte.
- **Reads are never spent twice.** Figma limits how often a file can be read — a free-plan file allows six reads a month — so every response is kept on disk. Importing the same frame again, or the rest of the file after the first look-up, costs nothing, and the dialog shows how many reads you have spent.
- **What can't come across is counted and shown** after the import runs, rather than quietly going missing: text in a font you don't have arrives editable in the default face and is named, background blurs and inner shadows are listed, and auto-layout never comes across.
- Your Figma personal access token goes in **Settings ▸ Integrations**, beside the assistant key.

### Linux

- **Kineto runs on Linux**, as an AppImage or a `.deb`. Built on Ubuntu 22.04, so 22.04 / Debian 12 and newer are the bar.
- **It needs an Xorg session, not Wayland.** On Wayland the renderer paints over the whole interface and the window looks blank, so Kineto says so on launch and tells you how to switch: log out, pick an Xorg or X11 session at the login screen, and start it again. Worth knowing before you download — Ubuntu 24.04 and Fedora default to Wayland on most hardware, while Mint and Cinnamon default to X11.
- This is the first Linux build, so it is a download only: Linux copies do not update themselves yet. A later release will turn that on once this one has been confirmed working.

### Fixes

- **SVG imports keep their blend modes.** A layer exported from Figma or Illustrator with Multiply or Screen used to arrive as Normal.

## 0.4.0 — September 1, 2026

The 3D look-development pass reaches its end, time remap arrives for video and audio, and a week of tester feedback lands as about fifty interface fixes.

**A new name is coming.** The app is being renamed shortly. It is the same app and your projects are unaffected, but the download and the icon will change name — this is the warning before they do.

### 3D look development

The arc that began in 0.3.4 is complete. A new scene arrives lit rather than flat.

- **Area lights with real softness**, and an `Emit light` option on surfaces so a bright plane lights its neighbours instead of only looking bright.
- **Contact shadows** where objects meet, and a shadow bias measured as a world distance — which is what lets area lights cast at all.
- **Light rigs.** Applying a rig replaces the comp's lighting as a set, in its own folder, rather than leaving two lighting setups to reconcile by hand.
- **Environment contrast.** The default environment has range in it now instead of an even grey.
- **Clicking a 3D object selects the object you clicked.** Picking used to hit-test flat cards, so a mesh was selectable by its bounding box rather than its shape. It ray-casts the real geometry now, and hovering shows the silhouette before you commit.
- **Materials and the Library.** Texture sets can be imported from a folder or a ZIP and reused across projects, alongside environments, objects and light rigs.

### Time

- **Time remap for video footage.** Arm the stopwatch on Time Remap and a clip plays to whatever curve you draw. The layer bar shows one tick per source frame — bunched where it races, spread where it crawls — so a retime is legible without scrubbing it.
- **Audio follows the remap**, in the preview and in the export. A retimed clip is resampled by position rather than by rate, so it does not drift.
- **A precomp runs on its own clock.** Nested comps were sampled at the parent's time, so a precomp with its own speed or remap drew the wrong frame — and effects inside one never animated at all. Both are fixed, in the viewer and in exports.
- **Exports sample what they should.** Effect keyframes, forked precomp time and remaps were all missed on the way out.

### Interface

- **Shy layers.** Mark a row shy and the timeline's new Shy button hides it, in both the timeline and the layers panel. A row filter only: nothing about what renders changes.
- **Blend modes show themselves.** Move down the list and each mode appears on the frame as you pass it; leave without choosing and the original comes back. The whole pass is one undo entry.
- **Onion skinning gets its options** — frames each side, strength, and a colour per side. The colours had been in the file since onion skinning shipped and never reached the screen.
- **Fill, stroke and width edit what is selected**, rather than only setting the style of the next shape, and are available with the Move and Edit Path tools.
- **Layer numbers** in both panels, **lock and solo** in the timeline, and selecting a layer scrolls both panels to it.
- **⌘↑ / ⌘↓** step the selection through the stack; **⌥-wheel** zooms the time axis under the cursor; **⇧** constrains the pen to an axis and holds a graph keyframe at its time.
- **Chain buttons** for rectangle width/height, ellipse radii and cube width/height, preserving the ratio rather than squaring the shape.
- **Tool help moved behind a `?`** instead of sitting permanently across the options bar.
- **Workspaces** can be saved over and renamed.

### Fixes

- **Snapping only considers layers you can see.** It pulled to layers hidden by solo, layers outside their in/out range, matte sources drawn into another layer, and cameras.
- **The anchor point tool no longer moves a layer whose position is keyframed.** The compensating move was written as a base value, which a keyframe outvotes.
- **Locking a layer locks it in the timeline.** Slide, trim, razor, reorder and keyframe drags all ignored the lock.
- **A copied effect brings its keyframes.** Effect parameters animate on the layer, so a copy cloned the effect and left every curve behind.
- **Files dropped on the Project panel stay there** instead of also landing in the open comp.
- **New solids match the comp size** rather than a fixed 400×300.
- **Align moves a keyframed layer**, by keyframing it.
- **Every vector import gets its own comp**, not only multi-layer ones.
- **Adding Trim Paths no longer makes the shape disappear.**
- **A duplicate lands above its original and stays in its group**; a paste lands above the selection rather than on top of the stack.
- **The Background layer draws in a 3D comp again.**
- **Middle-drag pans from every tool**, and the ruler gets its mousedown back.
- **The playhead rests on the last frame**, not one past it.
- Eighteen tooltips stopped telling Windows users to press ⌥, the Settings tab strip wraps so Windows keeps its last tab, and six controls asked for a theme token that was never defined.

## 0.3.5 — August 25, 2026

Same-day fix for 0.3.4.

- **Opening the Graph Editor no longer blanks the window.** In 0.3.4 the panel took the whole interface down the moment it appeared — every panel vanished while the viewer image stayed on screen, because that image is drawn behind the interface rather than inside it. Nothing was ever lost: the project was untouched, and saving and reopening worked throughout. Pressing G, or opening any workspace that includes the Graph Editor, is safe again.
- **A panel that hits an error now fails on its own.** Instead of taking the window with it, it shows a notice in its own frame with a Try again button, and everything around it keeps working — so a future bug in one panel costs you that panel, not the session.
- **Scaling a 3D object in Z exports the way it looks.** Depth scale reached the viewport but was dropped on the way out, so a sphere squashed or stretched in Z rendered correctly while you worked and came out round in the export. Nested precomps were already correct; this was the top-level comp only.
- **Scale's stopwatch keyframes depth along with X and Y in 3D comps.** Animating Scale used to leave depth pinned at its static value, so an object was only the right shape on the frames where the two happened to agree. Splitting Scale into Separate Dimensions also hid the Z field entirely — it has its own row there now, and an animated Scale Z gets a proper label and colour in the graph editor and timeline instead of an unnamed curve.
- **Dragging keyframes on the timeline takes depth with them.** Moving a diamond, or sliding a whole layer, used to move every transform channel except depth scale — which pulled an animated depth out of step with the X and Y keyframes it was built against.

## 0.3.4 — August 25, 2026

The largest release since 0.2.0: a 3D look-development pass that changes what a new scene looks like out of the box, crash recovery for work you have never saved, a native macOS menu bar, and a long round of interface work driven by tester feedback.

**Crash recovery**

- **Untitled projects are autosaved now.** Work you have never saved to disk used to be the one thing a crash could take completely; it is autosaved to Kineto's own folder, and the next launch offers it back as a new tab — Recover, Not Now, or Discard. Nothing is deleted unless you pick Discard, so dismissing the prompt is always safe.
- Recovery files are named per session, and work belonging to another copy of Kineto that is still running is never offered back.

**3D — lighting and look**

- **A new 3D comp finally shows what the renderer can do.** The default environment, exposure, render quality and material settings were all pitched too low; a fresh 3D comp now arrives lit, grounded and shaded the way the engine is actually capable of, instead of needing a tour of the settings first. Existing projects keep the values they were saved with.
- **Studio Setup builds a lit, grounded stage in one click** — key, fill and rim over a floor, ready to drop an object onto. New 3D objects also rest on that floor instead of appearing at an arbitrary height.
- **Spot lights.** The first fixture that has falloff *and* casts shadows: a directional light is constant across a surface and point lights never cast, so a three-point rig used to render a backdrop as a perfectly even wash. Cone angle, softness and falloff live in the light panel.
- **A 3D comp takes eight lights, up from four.**
- **Plane and Cyclorama primitives** — something to stand a scene on, including a curved floor-to-wall sweep with no visible seam.
- **Scene exposure and a Filmic tone curve.** Exposure is in stops and is applied while the render is still floating point, so a negative value can bring a blown highlight back — unlike the Exposure effect, which runs after the 3D scene has been flattened to 8 bits.
- **An Environment Contrast dial** pulls the dim fill down and lets the key stand up, deepening the environment's own shadow with it; below 1 it flattens toward an even, shadowless wash.
- **HDRIs and the built-in skies cast a shadow.** A scene lit entirely by an environment, with no light layers at all, used to sit in a flat wash. The environment's dominant direction now shadows the ambient term in proportion to how much of the sky's energy arrives from it — a sharp sun shadows nearly all of it, an overcast dome almost none. Enabling it never brightens the scene.
- **Edge anti-aliasing for the 3D scene.** Render Quality now applies multisampling alongside supersampling, so silhouettes stop stair-stepping against high-contrast backgrounds — the default Normal setting is cleaner than the old Ultra was. The Render Quality labels now describe what both dials do.
- **Effects run on 3D layers.** The mesh is isolated, the effect chain runs, and the result composites back depth-aware, so a glow or a blur on a 3D object sits correctly against everything around it. The 3D effect halo also stops carving holes in backdrops drawn after it.
- **3D anchor points move in depth**, with Front / Center / Back presets in the Align panel.
- Flat cards take the same lighting and shading path as meshes, so a card and an extruded shape in one comp finally agree.
- Lights render from where the panel says they are, and the light gizmo shrank to a compact indicator that yields to the XYZ handles.
- Glow gained a Blend dropdown — Add, Screen, Normal, Multiply or Glow Only.

**3D — materials and textures**

- **28 built-in materials** — chrome, brushed metals, plastics, acrylic, rubber, concrete, plaster, woods, felt, canvas, neon and softbox emitters — reachable from a Preset menu on any 3D layer, with Copy, Paste and Reset alongside.
- **A repeating texture is one size across a whole object.** A checkerboard on a cube, an extruded shape or extruded text used to come out square on the front and stretched about four to one down the sides, and each letter of a word wore it at a different size; every face now matches. ⚠ This changes how existing textured 3D work renders — reopening an older project shows the corrected mapping. Untextured scenes are unaffected.
- **The flat ends of a cylinder or cone take a texture properly.** With any bevel on the edge — which is the default — a texture on the end cap came out as a dartboard of pie wedges instead of landing flat on the circle.
- **Models imported without texture coordinates can be textured at all.** An .obj with no UVs used to paint the whole model one flat colour whatever you assigned to it, with no way to tell why; Kineto now generates a mapping on import. Models that bring their own UVs are untouched.
- **Normal, roughness and metalness maps are read as data, not as colour.** They were being sRGB-decoded, which quietly wrong-footed every material that used one.
- Material libraries (.mtl) read correctly when they are indented or use Windows-style paths, and a one-value colour or texture coordinate no longer knocks everything after it out of alignment.
- Importing a texture used to leave every material map picker showing only "None", and an extruded shape's material had no heading and no Copy / Paste / Reset.

**Interface**

- **A native macOS menu bar.** Kineto's menus are real system menus, workspaces moved into the Window menu, and Panels merged into Window on every platform.
- **Help ▸ Keyboard Shortcuts** opens a cheat sheet of every binding, generated from the app itself so it cannot drift from what the keys actually do.
- **A dockable Search panel** — the ⌃Space command palette, docked, so it can live in a workspace.
- **A de-boxing pass across the chrome:** timeline toggles, paint kinds, hex and gradient buttons, swatches, panel-bar toggles, the operator/geometry/modifier stacks, the shape properties panel and the Align panel all lost their boxes.
- **Layer rows say what they are** — folder, null and adjustment icons, the eye ahead of the label, and a label colour per layer kind. A row only shows a disclosure arrow when there is something to expand.
- Errors stay up for 15 seconds instead of vanishing before you can read them.

**Timeline**

- **Parenting moves to the timeline.** A Parent column with a pick whip: drag it onto a row to parent, and the whip draws a dotted line and lights up the target as you go.
- **Track mattes get their own column** — a hover +Matte chip, a source dropdown and text-labelled alpha/luma toggles, with the full matte stack behind "+". Clearing a matte actually releases the source layer, and that makes the pick undoable.
- **Toggle columns paint on drag:** press eye, solo, lock or mute and sweep across rows.
- **Retimed layers are marked with a dot pattern** on the bar, and a stretch drag moves the bar live instead of jumping on release. Speed drags stop eating frames.
- **A multi-layer selection gets one real bounding box**, and scales and rotates as a set.
- Effect pills reorder by drag, and enabling, disabling or reordering an effect is undoable.
- Locking or soloing a group covers its members.

**Animation**

- **Motion paths grew handles.** Position keyframes carry spatial bezier tangents you can drag right in the viewer, and animated shape points and mask points draw their trajectories too.
- **Keyframe loop modes** — Cycle, Ping-Pong and Continue — carry an animation past its last keyframe instead of holding it.
- **An Animation menu:** Offset Layers, Offset Keyframes, Order Layers and Loop.
- **Easing presets follow After Effects semantics** now — Ease In eases *into* the keyframe — and they reach mask and shape channels from the timeline.
- **Mask Path keying is fixed:** clicking a keyframe no longer disarms the channel, and the layered path row owns its own keying, with Key All and Remove All.
- **Four separate ways a keyframe Delete could silently do nothing** are fixed.
- Graph editor value drags render live instead of snapping on release, and keyframe copy/paste carries every selected layer rather than just the largest.

**Gradients**

- **Gradients gained a blend space and per-stop transition midpoints**, so a ramp can bend toward one stop instead of always splitting evenly.
- **Ramp editors show honest previews**, with a Blend row and midpoint diamonds.
- A path gradient's offset reads as a looping percentage, and the two paint editors stop overwriting each other's changes.

**Text & shapes**

- **Extruded text, per character, with animators intact** — glyph-level animation on a 3D extrusion.
- **Double-click a text clip in the timeline to edit it.** Starting a new text edit commits the one already open, clicking empty timeline commits an edit, and Layer ▸ New Text Layer starts you typing — and cleans up after itself if you don't.
- **Donut** — a real ring primitive, with a hole radius and start/end angles for arcs.
- **Skew and Pie** as vector geometry operators.
- **Tapered stroke**, with numbers that move when you drag them.
- **⇧⌘-drag a path edge to bend it into a curve**, and selected path points get a bounding box.
- Star roundness can target the outer points, the inner ones, or both, and fill paints over stroke on shapes you draw.

**Viewer & workflow**

- **Freeze Frame.**
- **Composition and layer markers**, addable from the keyboard.
- **Reload and Replace Footage**, and dropping a file onto New Composition.
- **An isometric grid**, drawn and snapped to.
- **Snapping options, grid spacing and guide presets** behind a right-click.
- **Playback controls moved into the viewer as a HUD.**
- Clips stagger, take a custom speed and reveal; primitives place with a tap.
- Right-click to create a layer, with Duplicate and Reveal in the project menu.
- Arrow keys step value fields, and clicking empty space commits a rename again.

**Fixes**

- **Trim Paths could freeze the app** — a re-entrant playhead lock.
- **Motion blur reaches image-sequence exports**, and frame 0 no longer samples before time zero.
- The hue slider works on a white swatch, and colour swatches show their colour again instead of the checkerboard behind them.
- The work area survives loads and comp switches, and nulls stop adopting the selection.
- Adjustment layers get a comp-sized selection box, lights are selectable in the viewer, and groups drag as one with boxes that tell the truth.
- Browser accelerators are blocked, select-all is honest, sorting is natural, and nudges are live.
- More things undo: imports, folder create/rename/delete, the Edit Path conversion loop, eye and mute, switching a light's type, and assigning a texture map.
- **Windows:** the lock, autosave and temporary save files are properly hidden — a leading dot hides a file on macOS and Linux but not on Windows.

## 0.3.3 — August 19, 2026

**3D & camera**

- **3D camera tools.** The camera slot now holds Orbit, Dolly X/Y and Dolly Z (C cycles between them). Left-drag runs the selected tool, right-drag always trucks, and the scroll wheel dollies toward the cursor. Adding a camera to a 2D comp makes it 3D on the spot.
- **Bevels grew styles** — Inner (the classic), Round, Chamfer and Step — and the cube, cylinder and cone primitives take a bevel too, not just extruded shapes.

**Saving**

- **Open projects autosave in the background**, so a crash, a force-quit or a power cut no longer costs you the session. Reopening the project finds the newer autosave and asks whether to take it. (Projects you have never saved to disk are covered from 0.3.4.)
- **Saving is atomic.** A crash or power cut in the middle of a save used to be able to leave a truncated, unopenable .mfp; the new file is written alongside and swapped into place only once it is complete, so the worst case is the previous save, never a broken one.
- **Projects opened in two places warn you.** Opening a .mfp that another Kineto window — or another machine on a shared drive — already has open now says so before the two of you overwrite each other's saves, and offers to open it anyway.

**Interface**

- **The toolbar reorganized:** Anchor Point tucks behind Move and Zoom behind Hand (click and hold to pick), the drawing tools sit together, and the 3D buttons grey out until the comp is 3D instead of disappearing.
- **Esc cancels any value scrub, cleanly.** The value returns to where it started and no undo entry is left behind — even on animated properties, where the scrub's own keyframe is removed rather than left as a stray diamond.
- The hand tool and middle-mouse panning work everywhere.

**Import**

- **Paste SVG code straight to editable layers.** Copy SVG from Illustrator's Copy As SVG, a code editor or the web inspector, and ⌘V brings it in as shape layers through the normal import dialog.

**Animation & timeline**

- **Property links reach shape and text properties** — drive width, height, corner radius, stroke width, font size or any fill colour channel from another layer's property, per element.
- **Timeline power tools:** Time-Reverse selected keyframes in place, ⌘⇧V pastes them mirrored, ⌘] and ⌘[ reorder layers, arrow keys nudge them in the viewer, drops land at the cursor time, comps trim to the work area, and any framerate is valid in composition settings.
- **Path editing, second pass:** select several points at once and save point groups to come back to.
- **Masks run before effects**, the way After Effects orders them.
- **Levels got a real shader and a histogram**, and text takes gradients.

**Render**

- **The render queue parks jobs:** Add to Queue holds them, Render runs everything, and PNG/EXR sequences now render motion blur like MP4 always did.

**Undo**

- Creating a comp, locking and soloing layers, and multi-layer deletes all undo properly now — and deleting a group takes its members with it instead of leaving ghost rows.

**Windows**

- **EPS and AI import finds per-user Inkscape, Scoop, Chocolatey and winget installs**, and the error message finally tells the truth about what is missing.
- Video no longer plays back black after pressing Space, and middle-click autoscroll is gone.

## 0.3.2 — August 15, 2026

**Gradients & colour**

- **Gradient strokes:** give any stroke a linear or radial ramp with the same stop editor fills use, drag its axis right on the canvas, and switch back to solid without losing the ramp. Fill and stroke gradients each get their own gizmo.
- **Colour animates as ONE keyframe now** — a single diamond per colour instead of four channel rows — and fill and stroke each gained a separate animatable Opacity, so a colour sweep and a fade are independent.
- **Background layers grew a full gradient ramp** (stops, linear or radial, reverse) with draggable on-canvas start and end handles — and dropped the transform and lighting controls they never used.

**Import**

- **.ai and .eps files import as layered comps.** Illustrator layers arrive as separate shape layers inside a comp container, with gradients, clips and colours intact — and on a machine without a converter, the import tells you exactly what to install.

**Paths & viewer**

- **Inner- and outer-aligned strokes render exactly now:** no more fold-over artifacts at sharp corners or faceted curves at heavy widths.
- **Path editing:** Delete removes the selected point — including every keyframe of an animated point — and the Points toggle shows geometry points for all layers, not just the selection.
- **Viewer flow:** press ⌥ mid-drag to leave a copy behind, ⌥-drag a guide to duplicate it, ⇧-drag a guide to snap it to ruler ticks, and right-click a guide to delete just that one. Rotation snaps to 15°, scale can be proportional or corner-anchored, and shapes can be drawn from the centre.
- **Multi-item drag and marquee selection** across the Project, Layers and Timeline panels, and properties-panel edits apply to the whole selection instead of one layer.

**Render & window**

- **Renders never overwrite silently** — output names auto-increment (Comp_001) past existing files and queued jobs.
- The app remembers its window size and position between sessions.

## 0.3.1 — August 14, 2026

Video export, fixed for real.

- **Video plays in exports.** Comps with video footage used to render the whole clip as a single frozen frame; footage now streams frame-by-frame into MP4, MOV, GIF and SVG, honouring trims, speed, reverse and looping.
- **Every video layer decodes on its own stream.** Overlap two copies of one clip at different times — a picture-in-picture echo, a staggered wall — and each shows its own frames, in the viewer and in the file.
- **The preview finally respects where a clip sits.** Footage moved, trimmed, split or retimed shows the same frames while you scrub and play that the export will write.
- **Splitting, duplicating, sliding or trimming a video layer updates the picture immediately** instead of freezing until the next scrub — and splits play straight through without a stutter.
- **Rendering to a file that already exists asks before replacing it**, instead of silently overwriting.
- The welcome screen opens with a proper intro video, and rectangles grew a corner-roundness widget right on the canvas.
- **Timeline care:** work-area edits are undoable, guides persist with the project, and keyframe selection in the graph editor behaves the way your hands expect.
- Panel menus — animator presets, + Property and friends — can no longer be clipped by their own panel.

## 0.3.0 — August 13, 2026

Per-character text animators, a timeline that thinks in frames, and an early preview of true 3D rendering. This release also carries everything from the 0.2.2 tester build, which was never published on its own — so upgrading from 0.2.1 brings the whole Aug 6 feedback round with it.

**Text animators**

- **Per-character text animators:** animate glyphs individually through animator groups, with dual-handle range selectors, a live weight overlay, and an inline falloff curve editor.
- **Animator presets, with a picker on every animator** — swaps keep your timing, reveal presets come in on/off pairs, and a Smoothness control shapes the edge.
- **A Noise selector for organic motion**, with a wiggle tuned never to go dead — and variable font axes are animatable as per-character offsets, so weight can ramp across a word.
- Text animators are reorderable and collapsible, and fonts that silently fell back to the system font now render as themselves.

**The frame grid**

- **The timeline thinks in frames now.** The playhead, keyframes, in/out points, work area, razor and slide edits all land exactly on the comp's frame grid — at every frame rate, 29.97 included. The ruler draws per-frame ticks at high zoom, with a frames-mode toggle.
- **Parking on a keyframe reads as ON the keyframe:** the indicator is frame-accurate at any fps, and editing there updates that key instead of quietly minting a duplicate a few milliseconds away.

**3D — early preview**

- **3D is growing up:** bevelled extrusion, parametric primitives, OBJ import with .mtl materials, image-based lighting, shadows from every directional light, a shadow-catcher layer mode, screen-space ambient occlusion, environment rotation, and a Scene layer to drive it all — plus a Draft / Normal / High / Ultra render-quality setting. Still rough in places; poke at it and tell us what breaks.
- OpenEXR environment maps load alongside Radiance .hdr, custom HDRI backdrops no longer come out squished and tiled, rounded extrusion corners shade smooth instead of as a fan of facets, and the light gizmo works again.

**Import**

- **Layered Photoshop import:** .psd and .psb files come in as a composition, with Photoshop type layers arriving as editable text. A missing font keeps Photoshop's own picture and preserves the text underneath it.

**Mattes, links & shapes**

- **A composite matte stack** — stack more than one matte on a layer — with **property links** that drive any property from another layer's, and **Scale as separate dimensions**.
- **Boolean geometry:** a live in-stack Union / Subtract / Intersect / Exclude operator, plus Combine Shapes for a destructive merge of the selected shape layers.
- Masks render inside nested precomps and on 3D cards.

**Interface**

- **A dockable History panel** — the undo history as a list, with click-to-jump.
- **Per-layer label colours** that no longer shuffle when you reorder or delete.
- **P / S / R / O / A key transforms at the playhead**, and ⇧PageUp / ⇧PageDown.
- **Multi-select rotate and scale in the viewer**, with edge handles and anchor snapping.
- **Project panel parity:** multi-select, Delete, ⌘D and ⌘C, and recents that prune themselves.
- Transport controls in the Graph Editor, batch keyframe delete in both panels, and bounce/elastic easing with custom values and scrubbable fields.
- **Colour & swatches:** swap fill and stroke, a stroke kind row, and the eyedropper everywhere.
- Text gained an animatable stroke and font live-preview; ⌘I imports and ⌘W closes a project.
- **Windows chrome:** one hover system, menus that dismiss properly, and dock/graph fixes.

**Fixes**

- **Layer opacity was applied twice** — a layer set to 50% rendered like 25%.
- Trim Paths' offset wedge is fixed, with a full-span identity and a stitched wrap seam.
- Convert Text to Outlines resolves overrides and keyframes first, so the text no longer shrinks.
- Zooming out no longer re-aliases, and number fields round sanely instead of showing float dust.
- A round of timeline papercuts: broadcast edits, in/out fields, rename and focus fixes.

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
