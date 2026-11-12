# Project 1 — AI Video Studio

Read the root `CLAUDE.md` first. This file defines the project-specific requirements for AI Video Studio.

## Objective

Turn any user-provided topic or source material into a complete, editable video with an AI-generated content plan, animated scenes, AI narration, synchronized subtitles, and optional sound design. Do not restrict this to system design.

Supported inputs include a prompt, notes, script, PDF/document, code, logs, diagram, image, screenshot, audio, or video.

## Workflow

1. Collect the topic, audience, desired duration, language/tone, format, and source materials. Sensible defaults should allow the user to start with minimal input.
2. Inspect supplied assets and create an asset manifest.
3. Generate an editable content brief, script, scene-by-scene storyboard, visual direction, narration, subtitle plan, and asset placement plan.
4. Show the outline/storyboard and a representative preview before a full render when practical.
5. After approval, generate scenes, narration, subtitles, and final output.
6. Validate the render and report its actual path and any limitations.

## Content planning

Create a clear opening, logical progression, meaningful examples or demonstrations, and a conclusion. Choose topic-appropriate visuals rather than forcing every subject into a single diagram template. Distinguish verified facts from assumptions and illustrative examples. For news and incidents, preserve sources and avoid unsupported causal claims.

## Animation engine

Use React/TypeScript components and Remotion compositions where suitable. Support:
- Animated diagrams and relationships.
- Moving objects, tokens, packets, pointers, and data flows.
- Code snippets with highlighted lines.
- Algorithm state changes and data structures.
- Charts, timelines, comparisons, and progressive reveals.
- User-provided images, screenshots, diagrams, and video segments.
- Transitions, camera movement, zoom, highlights, and annotations.

Motion must help explain the content and align with the scene timeline.

## AI narration and audio

Create a replaceable provider interface for AI narration. Detect existing integrations instead of assuming credentials or paid access exist. Document setup and costs for any provider that must be configured.

Support per-scene voice generation, preview, regeneration, replacement, and audio mixing. Background music and sound effects must be optional, independently configurable, and mixed without clipping or excessive overlap.

## Subtitles

Subtitles must be editable and aligned to actual narration audio when available. Support timing correction, style controls, embedded subtitles, and SRT/VTT export. Word-level highlighting may be offered when timing data supports it. Do not claim perfect synchronization based only on script text when actual audio timing is available.

## User media

Allow the user to assign supplied media to scenes. Support crop, scale, position, overlay, annotation, and video time ranges where practical. Preserve original assets, track their references, and flag missing or unsupported media.

## Editing and regeneration

Allow editing of script, narration, scene order/duration, visual settings, assets, subtitle timing, transitions, and audio settings. Regenerate only affected scenes where practical. Do not overwrite approved recordings without confirmation.

## Export profiles

Support:
- Landscape: 1920×1080 at 30 FPS.
- Vertical: 1080×1920 at 30 FPS.
- Individual scene renders.
- Complete long-form video.
- Optional SRT/VTT.
- Editable project configuration and asset manifest.

Vertical compositions must be intentionally recomposed for portrait viewing, not simply scaled down from landscape.

Provide independent controls for narration, subtitles, music, and sound effects. Turning narration off must not silently remove subtitles unless the user chooses that behavior.

## YouTube safeguards

Before marking a video publication-ready, review originality, factual accuracy, third-party asset rights, repetition, and possible altered/synthetic-content disclosure needs. Do not mass-generate interchangeable videos that differ only in titles or superficial details. AI voice is a production method, not a substitute for meaningful original value. Do not guarantee monetization.

## Implementation phases

1. Audit the existing repository and propose a plan.
2. Build one end-to-end example with three animated scenes, configured AI narration, aligned subtitles, and a landscape render.
3. Add asset management, editing, and targeted regeneration.
4. Add vertical layouts, scene exports, and batch rendering.
5. Add validation and documentation.

## Acceptance criteria

- Arbitrary topic input works.
- Script and storyboard are editable.
- At least three distinct scenes render.
- Configured AI narration can be generated and previewed.
- Subtitle timing can be edited and checked against audio.
- Narration and subtitles can be controlled independently.
- User-supplied media is included correctly.
- A landscape render exists and passes an integrity check.
- Errors and unverified features are reported honestly.
