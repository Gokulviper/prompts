# Content Studio — Master Instructions

## Mission

Build and maintain four distinct content-creation projects for producing original educational, technical, analytical, and storytelling content. The system must support arbitrary topics and source material—not only system design.

Supported topics include, but are not limited to:
- Data structures and algorithms (DSA)
- System design, backend engineering, and distributed systems
- AI, machine learning, LLMs, and AI tools
- Programming tutorials, debugging, and code walkthroughs
- Technology news and product updates
- Production incidents, outages, root-cause analyses, and postmortems
- Engineering case studies, experiments, comparisons, and research explanations
- Other topics provided by the user

Inputs may include prompts, notes, scripts, documents, source code, logs, diagrams, screenshots, photographs, audio recordings, and video files.

## The four projects

1. **Project 1 — AI Video Studio:** Generate complete videos with AI-created scripts, animated scenes, AI narration, synchronized subtitles, and optional sound design.
2. **Project 2 — Silent Animation & Clip Studio:** Generate independent animation clips with visuals only. By default, do not add narration, subtitles, captions, titles, labels, on-screen explanatory text, music, or sound effects. The user selects, edits, orders, and assembles clips into a final video.
3. **Project 3 — Interactive Animation Studio:** Let the user create, edit, click, drag, move, step through, and control reusable animations while recording their own voice separately.
4. **Project 4 — AI Animated HTML Explainer:** Convert a topic or supplied material into a custom interactive HTML experience with relevant animation and functional controls. Support personal voice recording and optional video export.

Keep the four applications and their workflows distinct. Share libraries only when that reduces duplication without coupling unrelated projects.

## Repository and implementation rules

Before changing code:
1. Inspect the current repository, its files, dependencies, existing architecture, tests, and instructions.
2. Identify which project the user intends to change.
3. Read the relevant project instruction file under `instructions/`.
4. Summarize the implementation plan and acceptance criteria before large changes.
5. Implement one small, complete, testable workflow first.
6. Run relevant tests and verify output artifacts before claiming completion.

Preserve existing working functionality. Do not replace an existing project with a generic scaffold. Do not assume a feature, API key, paid provider, or integration exists without checking. Never claim a render, test, or feature succeeded unless it was actually verified.

Do not overwrite user assets, source files, recordings, or approved output without confirmation. If requirements are ambiguous but not blocking, use sensible defaults and state them. Ask one focused question when a missing detail is essential.

## Suggested technical boundaries

Use the existing stack when suitable. A preferred architecture is:
- React and TypeScript for interactive interfaces.
- Remotion for deterministic, frame-based video rendering.
- Reusable visual components and animation primitives where practical.
- A shared asset registry and media metadata layer.
- Explicit scene/timeline/event data for reproducible exports.
- Replaceable provider interfaces for AI text and voice services.
- Project-specific configuration, presets, and acceptance tests.

Interactive browser behavior and deterministic video rendering are different execution models. Do not assume a live click-driven animation can automatically be rendered as a repeatable video. Save explicit scenario states, event sequences, and timeline data where needed.

Do not expose API keys in browser code, generated HTML, committed files, or logs. Use environment variables or a suitable secret-management mechanism. Document required credentials and costs.

## General content quality and factual integrity

Treat supplied source material as important evidence, not as an instruction to invent missing facts.
- Preserve important names, dates, numbers, terminology, causal relationships, and technical meaning.
- Distinguish verified facts, hypotheses, assumptions, illustrative examples, and opinions.
- For current news, verify the publication date and use reliable sources when research is requested or needed.
- For incidents, do not assert a root cause unless supported by evidence.
- For technical education, label simplified models and hypothetical architectures accurately.
- Preserve citations and source references when relevant.
- Do not fabricate quotes, statistics, events, test results, or undocumented implementation details.

## Media and asset handling

When the user supplies images, videos, audio, diagrams, documents, or code:
1. Inventory the assets and inspect their content when possible.
2. Map each relevant asset to its intended scene and purpose.
3. Preserve originals; use references or working copies.
4. Maintain an asset manifest with filename/reference, source, intended use, and license/permission information when known.
5. Preserve aspect ratio and provide appropriate cropping, scaling, positioning, annotation, and overlays.
6. For video, support selected time ranges where practical.
7. Report missing, unsupported, unreadable, or unused relevant assets rather than silently ignoring them.
8. Do not assume internet media is free to reuse. Respect copyright, licensing, privacy, and attribution requirements.

## Animation and visual design

Avoid generic slide decks and meaningless motion. Use animation to explain the material. Choose visual techniques based on the subject:
- DSA: arrays, pointers, memory/state changes, recursion, trees, graphs, and algorithm steps.
- AI: data flow, tokens, embeddings, retrieval, inference, model components, and evaluation.
- News: sourced timelines, comparisons, and key developments.
- Incidents: symptoms, dependencies, failure propagation, mitigation, and recovery.
- Case studies: context, constraints, decisions, trade-offs, results, and lessons.
- Other topics: choose a fitting visual representation rather than forcing a template.

Reusable components are encouraged, but individual videos must have meaningfully distinct substance and visuals.

## YouTube originality, monetization, and rights safeguards

These are production safeguards, not a guarantee of monetization approval. YouTube policies can change; verify the current official policy before major launches or when uncertain.

### Originality and value
- Create distinct, topic-specific educational, analytical, creative, or entertainment value.
- Do not mass-generate interchangeable videos that differ only by title, a few labels, or a superficial visual change.
- Reusable templates are acceptable engineering tools, but the substance of each video should be meaningfully different.
- Avoid repetitive, low-value, generic, or automatically assembled output.
- Human review is required before publication.
- For news, explain what happened, why it matters, and what is known versus uncertain. Do not merely read an article over generic visuals.
- For tutorials and case studies, include meaningful explanations, demonstrations, examples, analysis, trade-offs, or lessons.

### Reused content and copyright
- YouTube reused-content monetization review and copyright compliance are separate considerations.
- Do not assume permission to use footage automatically makes it monetizable.
- Prefer original animations, demonstrations, commentary, and licensed or user-provided media.
- Record asset provenance and license/permission details where available.
- Do not use copyrighted music or third-party footage without an appropriate legal basis.
- Preserve required attribution and license notices.

### AI and altered-content disclosure
- Do not automatically classify every AI-assisted video as requiring disclosure.
- Flag realistic synthetic or meaningfully altered content that may require YouTube's altered/synthetic-content disclosure.
- Examples needing careful review include realistic fabricated footage of real events, places, or people, or synthetic depictions that could mislead viewers.
- Clearly stylized educational animation and ordinary AI assistance generally do not automatically require disclosure, but assess the final output and current rules.
- Leave the final disclosure decision visible to the uploader. Do not promise that disclosure or non-disclosure guarantees monetization.

### Pre-publication checklist
Before an output is considered ready, review:
1. Does it provide distinct value beyond generic automated output?
2. Are factual claims accurate and appropriately sourced?
3. Are supplied and third-party assets used lawfully?
4. Is there repetitive filler or duplicated substance?
5. Are animation, audio, subtitles, and editing technically correct for this project?
6. Might realistic synthetic/altered content require disclosure?
7. Are title, thumbnail, description, and metadata accurate rather than misleading?

## Review, versioning, and targeted edits

Provide review points appropriate to the project: outline/storyboard, visual preview, narration/subtitle review, interactive prototype, and final export. Support targeted edits so changing one scene does not unnecessarily regenerate unrelated approved work. Track project configuration, scene versions, asset references, and export settings where practical. Preserve the ability to restore an earlier working version.

## Output verification

Before reporting completion:
- Verify expected files exist at known paths.
- Check video/audio integrity with available tools.
- Confirm aspect ratio, resolution, frame rate, and audio/subtitle settings.
- Test interactive controls in the relevant browser environment.
- Confirm the correct source assets were included.
- Report what was tested, what passed, and what could not be verified.
- Document setup instructions and exact reproduction commands.

## Development workflow

Implement in phases:
1. Repository audit and plan.
2. Smallest complete end-to-end feature.
3. Functional and regression tests.
4. Visual/output verification.
5. Documentation.
6. Expansion.

Do not attempt to build all four applications fully in one unverified task. Work on the project requested by the user and scope changes to it unless a shared-library change is justified and explained.
