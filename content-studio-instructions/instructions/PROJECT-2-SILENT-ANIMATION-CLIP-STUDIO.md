# Project 2 — Silent Animation & Clip Studio

Read the root `CLAUDE.md` first. This file defines the project-specific requirements for the silent clip workflow.

## Objective

Create independent, short animated clips that the user can review, edit, select, order, trim, and assemble into a final video. Support any topic and relevant user-supplied media.

## Strict default output rules

The default generated video must contain visuals/animation only. Do not add:
- Spoken narration or AI voice.
- Subtitles or captions.
- Titles, labels, or explanatory text overlays.
- Background music.
- Sound effects.

Do not automatically add these elements. They may only be added if the user explicitly requests an exception. Text inherently present in a supplied screenshot, image, code sample, or source video is allowed; do not add new text overlays.

## Input and planning

Accept a topic, prompt, outline, script, documents, code, diagrams, images, screenshots, video clips, or a combination. Generate an editable clip plan with a clear visual purpose for each clip. Do not force every subject into system architecture diagrams.

## Animation quality

Use purposeful visual storytelling: movement, object transformations, algorithm steps, diagrams, comparisons, timelines, charts, highlights, camera movement, and supplied media as appropriate. Avoid static slide decks, meaningless motion, or visual clutter. Since no narration or text is present by default, make the visual sequence itself coherent and useful.

## Independent clips

Each clip must have:
- A unique ID and editable configuration.
- Its own deterministic timeline and start/end states.
- Scene duration, animation settings, transitions, and asset references.
- Preview and render status.
- Independent render capability.

Allow the user to preview, edit, regenerate, duplicate, reject, trim, and replace individual clips. Changing one clip should not unnecessarily modify other approved clips.

## Clip assembly

Provide a timeline or ordered clip list supporting:
- Reordering.
- Trimming in/out points.
- Adding, removing, and adjusting transitions.
- Optional visual intro/outro only when explicitly requested, because these can introduce text.
- Preview of the assembled sequence.
- Export of individual clips and the selected final sequence.

Avoid repeated content, abrupt unintended cuts, and inconsistent visual style. Do not add a transition when a clean cut is more appropriate.

## Media handling

Allow user-provided images, diagrams, screenshots, and video segments to be assigned to clips. Support crop, positioning, scaling, annotation, highlights, and selected video time ranges where practical. Preserve original media and maintain an asset manifest. Do not silently omit relevant supplied assets or substitute unrelated stock visuals.

## Export profiles

Support:
- Landscape: 1920×1080 at 30 FPS.
- Vertical: 1080×1920 at 30 FPS.
- Independent clip exports.
- Final assembled video.
- Editable project configuration and asset manifest.

Vertical compositions must be intentionally recomposed for portrait viewing rather than simply scaled down.

## YouTube safeguards

Silent content is not inherently disallowed, but generic, repetitive, low-value, or mass-produced output can create monetization risk. Ensure each clip and final video has a clear purpose and distinct visual substance. Do not rely on bulk stitching of interchangeable animations as the only source of value. Review media rights and possible realistic synthetic-content disclosure requirements. These checks do not guarantee monetization.

## Implementation phases

1. Render three independent silent clips with no added text or audio.
2. Add clip preview, editing, trimming, and independent regeneration.
3. Add reordering, transitions, and final assembly.
4. Add vertical output, reusable presets, and batch rendering.

## Acceptance criteria

- At least three clips render independently.
- No narration, AI voice, subtitles, captions, added titles/labels, music, or sound effects appear by default.
- Clips can be previewed and regenerated independently.
- User can select, trim, reorder, and assemble clips.
- User-provided media is included correctly.
- Landscape and vertical exports work.
- Final output is verified and the exact reproduction commands are documented.
