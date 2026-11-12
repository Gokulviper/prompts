# Project 3 — Interactive Animation Studio

Read the root `CLAUDE.md` first. This project is a hands-on visual editor for manually controlled animations and personal narration.

## Objective

Let the user create and reuse interactive animations for any technical or educational topic, then click, drag, move, step through, and modify the animation while speaking in their own voice.

Examples include DSA arrays/pointers/trees, AI pipelines, process timelines, distributed systems, incident sequences, data transformations, and other subjects. These examples are not restrictions.

## Workspace and canvas

Provide:
- Canvas with select, move, resize, delete, zoom, and pan.
- Add-object and add-connection controls.
- Alignment guides/grid where useful.
- Undo/redo where practical.
- Object properties and multi-selection where practical.
- Save, duplicate, load, and version scenarios.

Support reusable object types such as text/labels, shapes, containers, directional connections, images, video elements, nodes, packets, tokens, pointers, arrays, lists, trees, graphs, charts, and timelines. The user must be able to edit properties such as position, size, color, label, opacity, and animation behavior.

## Real interaction

Controls must change application state and cause meaningful visual changes. Examples:
- Click a packet to move it to the next node.
- Advance a pointer to the next array element.
- Change a value and observe a state update.
- Trigger a failure and then recovery.
- Step through an algorithm or process one event at a time.

Support play, pause, resume, reset, step forward/backward, speed control, duration, delays, keyframes or an equivalent timeline mechanism, object paths, highlights, appearance/disappearance, and event markers.

Do not implement decorative buttons that do nothing.

## Reusable components

Allow configured object groups or animations to be saved and reused. Store editable properties, inputs, events, animation presets, and required asset references. Support duplication and versioning. Avoid hardcoding a complete new animation for every topic.

## Personal voice recording

Provide microphone permission handling and record/pause/resume/stop/preview/re-record controls, plus upload of existing audio. Keep audio separate from animation state. Provide editable timing markers to align narration with events and a clean presentation mode that hides editor controls.

Never discard or replace a recording without confirmation. Do not assume that browser microphone recording is available until permission and browser support are verified.

## Export

Support editable project saving and reopening, standalone HTML packaging where feasible, and recording/capture of a canvas. Use Remotion for deterministic video export when appropriate. For repeatable rendering, save explicit scenario states and event/timeline data rather than relying on live clicks alone.

Optional outputs may include audio, subtitles, and sound effects when requested. Support landscape and portrait video export when implemented.

## User-provided media

Allow images, diagrams, screenshots, and video segments on the canvas. Support positioning, crop, scale, layering, annotation, highlights, and video ranges. Preserve source assets and save references in the project configuration.

## YouTube safeguards

Interactive originality helps demonstrate a creator's contribution but does not guarantee monetization. Avoid reusing the same demonstration with only superficial changes across many videos. Encourage distinct explanations, meaningful examples, and accurate claims. Review third-party asset rights and possible synthetic-content disclosure needs before publication.

## Implementation phases

1. Build a working canvas with movable objects, connections, and editable properties.
2. Add timeline playback and event-triggered animation.
3. Add reusable components and scenario save/load.
4. Add personal voice recording and presentation mode.
5. Add export/capture and documentation.

## Acceptance criteria

- User can create, save, and reopen a scene.
- Objects can be added, selected, moved, edited, and connected.
- Click actions trigger real animation behavior.
- Play/pause/step/reset work.
- Saved components can be reused.
- User can record or import their own voice.
- A clean presentation mode is available.
- At least one saved scenario can be exported or captured and verified.
- Supplied media is incorporated correctly.
