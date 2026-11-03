---
name: improve-design
description: Improve a UI through high-fidelity mockups, grayscale wireframes, or complete interactive prototypes, review them with the user, and apply their feedback. Use with existing designs or when a visual direction must be created from scratch.
license: MIT
---

# Improve design

Turn a design question into something the user can see, try, and decide on. Use high fidelity by default, including a single screen. When the user requests a wireframe, use black, white, and gray to focus on structure and interaction. Scale the interaction to the question being reviewed.

Use the user's language for the interface and review. Work within the current design task; a reviewed prototype does not authorize production implementation or deployment.

## Choose the starting point

Inspect the supplied design, product context, existing UI, assets, and confirmed decisions before asking questions. Reuse decisions from earlier reviews. Ask only for missing information that materially changes the work; continue independent work while waiting when possible.

Choose one of these modes:

- **With mockups:** a design file, screenshot, existing UI, or other visual reference already defines the intended result. Preserve it except for the specific changes being proposed. Read [the fidelity contract](references/fidelity.md).
- **Without mockups:** no visual reference defines the result. Establish a coherent direction using the product context and materialize it directly in high fidelity. Do not require the user to commission a separate mockup first. Read [the fidelity contract](references/fidelity.md), especially its section on creating a direction.

A wireframe is an explicit alternative to visual polish, not a synonym for having no reference. The second bundled example demonstrates this grayscale option. These starting points describe the available inputs. In either mode, a static mockup may be sufficient or an interactive prototype may be needed. A narrow review can use one screen. Do not inflate it into a dashboard, scenario index, or application.

## Frame a concrete improvement

Identify the user's task and the friction being addressed. Explain the proposed change briefly and preserve unaffected behavior, content, accessibility, and visual decisions. For new designs, state the few assumptions that shape the proposal. Do not present invented product facts as supplied requirements.

Choose the smallest reviewable deliverable:

- A high-fidelity mockup for a visual or content decision that needs no interaction.
- A complete interactive prototype when navigation, input, decisions, or state changes are being evaluated.

Use the available design tools and existing project stack where they fit. A self-contained HTML prototype is useful when it gives the user a convenient preview. Do not require a particular editor, framework, plugin, server, or diagram format. Avoid installing a production stack to review a design.

## Build flows that finish

Read [the flow and feedback contract](references/flows-and-feedback.md) for interactive work.

Define each scenario's starting state, intended actions, and observable end state before building it. Include every screen and state needed to complete the journey. Controls must perform the action their labels promise. Do not substitute a freely browsable collection of screens for the requested journey.

For multiple scenarios, or when the user requests the full four-stage review, provide an index. Selecting a scenario opens its context, steps, and expected result first. An explicit **Start** opens the prototype in an app-like view without the review guide or editor frame. For a single short scenario, a compact introduction is sufficient unless the user requested the full review structure.

Support the relevant inputs, validation, back/cancel behavior, confirmation, and resulting state. Preserve the user's choices as the journey progresses. The outcome must be reachable through user actions, not a shortcut that jumps to a success screen. A mock backend or in-memory model is acceptable when its boundary is clear in the review context.

Make the end recognizable. Offer an unobtrusive way to finish the review, give feedback, replay, or choose another scenario. Free exploration is optional and separate from completing the guided journey. Do not force a linear wizard onto a product whose natural interaction is different.

## Keep the proposal faithful

Use the same assets, tokens, content, and representative data across the reference and prototype. Reuse actual components when available. When translating between tools, compare the rendered result against the reference; a separate reconstruction is not evidence of fidelity.

Match typography, spacing, colors, imagery, component states, hierarchy, and responsive behavior at the agreed viewport. Implement the proposed changes consistently in the design and prototype. Do not silently substitute different data or visual components because a separate HTML implementation is convenient.

Keep construction notes, scenario instructions, and internal reasoning out of the app view. User-facing error, uncertainty, and decision information still belongs where it helps the user act. Put demonstration disclaimers and technical limitations in the review introduction.

## Review and iterate

Let the user comment on the screen or scenario they are reviewing. By default, feedback is ephemeral in the current tab. Keep it while navigating and replaying, offer a download, and explain that closing or reloading loses it. Export a Markdown file with the scenario, version, completion status, comments, and enough result context to paste as a prompt or attach to the agent. Do not add persistent storage or automatic submission unless requested. Never claim browser-only comments are synchronized or readable remotely.

Treat partial feedback as partial. When the user closes the review, record accepted decisions, changes requested, unresolved issues, and known limitations. On revision, update the design, prototype, scenario descriptions, and screenshots affected by the change. Mark superseded versions clearly without destroying unrelated work.

## Verify before delivery

Perform a bounded review after building:

1. Compare representative rendered screens with their visual references at matching viewport sizes. Fix material differences or disclose them before asking for approval.
2. For interactive work, execute **each advertised scenario from its actual entry through its final result**. Check the visible outcome and that back, cancel, and repeat actions preserve the intended state. Code inspection, screenshots, and a collection of clickable screens do not replace this walkthrough.
3. Check the relevant mobile and desktop layouts for clipping, horizontal overflow, legibility, focus, and reachable controls. Check invalid or incomplete input where the scenario requires it.
4. Confirm that feedback can be downloaded and reused as an agent prompt. Replay must not erase comments held in the current tab; explain that reload and close do.

Fix the findings in one batch and confirm the affected screens and journeys again. Avoid endless visual polishing. Report what was checked and any remaining gaps honestly. If a tool blocks verification, identify the blocked journey and do not call it verified.

Deliver a working preview or file, concise review instructions, the recorded decisions, and evidence appropriate to the deliverable. If a local preview is useful, keep it local unless the user requests broader access. Establish the actual host and port before sharing a URL. Publish, commit, or deploy only within the user's authorization.

## Examples

Read only the example relevant to the current starting point:

- [With mockups: reserve a book](examples/with-mockups/README.md).
- [Wireframe: schedule a focus session](examples/without-mockups/README.md).

Both examples include a runnable prototype with an introduction, a complete journey, an end state, and feedback. They demonstrate the interaction contract; they are not mandatory visual templates.
