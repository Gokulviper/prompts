# Project 4 — AI Animated HTML Explainer

Read the root `CLAUDE.md` first. This project generates a custom interactive HTML experience from a topic and supplied source material.

## Objective

The user provides a prompt, question, document, incident report, article, code sample, diagram, images, screenshots, or video files. The application analyzes the material and generates a custom interactive HTML page with relevant animations and functional controls.

The project is topic-agnostic. Do not restrict it to system design or force every input into the same diagram.

## Input analysis and planning

Accept natural-language prompts, text, notes, documents, source code, logs, images, screenshots, diagrams, video clips, and mixed inputs. Identify the learning objective, audience, key facts, process/sequence, uncertainties, and relevant assets. Produce a concise visual plan for review when the task is complex.

Preserve factual meaning. Distinguish facts, hypotheses, assumptions, and illustrative simplifications. For news and incident material, do not invent events, causes, quotations, or metrics.

## Choose topic-appropriate visuals

Possible experiences include:
- Step-by-step algorithm execution.
- Interactive diagrams and flowcharts.
- Moving objects and relationships.
- Incident and event timelines.
- Before/after comparisons.
- Interactive charts and data exploration.
- Code walkthroughs.
- AI/data pipeline visualizations.
- Annotated images and video.
- Process simulations and optional checkpoints.

Select only the visual elements that genuinely explain the input. Do not make a static article with a few decorative animations and call it interactive.

## Functional controls

Where appropriate, support:
- Play, pause, resume, reset.
- Step-by-step progression and adjustable speed.
- Clickable components and expandable explanations.
- Editable parameters and scenario toggles.
- Filters, timeline scrubbing, and annotations.
- Failure/recovery simulation when relevant.

Every displayed control must work. Do not leave placeholder buttons or fake interactions.

## Media support

Inspect and map supplied images, diagrams, screenshots, code, and videos to relevant scenes. Support crop, positioning, zoom, annotation, highlights, overlays, comparisons, and selected video time ranges where practical. Preserve original files, maintain an asset manifest, and report unsupported or missing media. Do not silently omit relevant assets.

## HTML implementation

Prefer React and TypeScript for maintainable interactive applications. Use HTML/CSS/JavaScript for standalone output where appropriate, SVG for precise diagrams, and Canvas when beneficial. Choose the simplest suitable implementation for the topic.

Provide editable source code, required assets, configuration, and run instructions. A standalone HTML package should use local assets or clearly documented dependencies. Never embed secrets or private API keys in generated HTML or browser code.

## Personal voice workflow

Provide a clean presentation mode and support recording with microphone permission, record/pause/resume/stop/preview/re-record controls, and uploading an existing recording. Keep narration separate from animation state. Support editable markers for aligning spoken explanations to events. Avoid resetting the animation unexpectedly when recording starts.

Optional subtitles, audio, and video export may be offered, but an interactive HTML page is not automatically a finished video. Keep the HTML experience and video export as separate outputs.

## Natural-language revision

Allow requests such as changing layout, slowing a transition, adding intermediate steps, including an uploaded image, adding a code walkthrough, or changing the visual style. Apply targeted edits while preserving unrelated working sections. Keep versioned changes and a way to restore a previous working version.

## YouTube safeguards

When the experience is captured/exported as a video, review originality, accuracy, media rights, repetitive low-value output, and potential realistic synthetic-content disclosure needs. Use distinct, topic-specific visual explanations. Do not claim that AI generation or interactivity guarantees monetization.

## Implementation phases

1. Generate one interactive HTML experience from a prompt with functional controls.
2. Add supplied image, diagram, code, and video support.
3. Add personal voice recording, presentation mode, and scenario saving.
4. Add natural-language edits, versioning, and optional video export.

## Acceptance criteria

- Arbitrary topic input is supported.
- The generated page uses visuals appropriate to the topic.
- Interactive controls work.
- Supplied images and supported video can be included.
- The experience can be run, saved, and reopened.
- User can operate the animation while recording their own voice.
- Targeted changes do not destroy unrelated work.
- Output is tested and limitations are documented.
