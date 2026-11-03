# improve-design

[Español](README.es.md)

Improve an interface through high-fidelity mockups and complete interactive
prototypes. Review the result, collect feedback, and keep the design, prototype,
and screenshots aligned as decisions change.

## Use cases

These two runnable examples show the available starting points. With existing
mockups, preserve their visual decisions. Without mockups, create a coherent
direction directly in high fidelity. Either mode can produce a single static
mockup when interaction is unnecessary.

The examples use Spanish interface copy and fictitious data. Run these prompts
from this repository's root. In another project, change the paths and use that
project's design references. These are usage prompts, not transcripts of an
independent generation run.

### 1. With mockups: reserve a book

Preserve the library's editorial appearance while completing a reservation.
The chosen collection window must appear in the final receipt.

#### Prompt

```text
Use $improve-design with examples/with-mockups/mockup.jpg as the reference.
Preserve its typography, colors, spacing, content, and Spanish interface copy.
Build the complete book reservation flow: view availability, choose a collection
window, review, confirm, and see the reservation receipt.
Show the scenario information before Start, then let me use the app without
review instructions over it. Let me give feedback after reaching the end.
Save the proposal under review/book-reservation/.
```

#### Screenshots

| Reference mockup | Completed reservation |
| --- | --- |
| <img src="examples/with-mockups/mockup.jpg" width="260" alt="Library book detail with a reserve button."> | <img src="examples/with-mockups/result.jpg" width="260" alt="Confirmed reservation with the chosen Saturday collection window."> |

[Example details](examples/with-mockups/README.md) ·
[Prototype file](examples/with-mockups/index.html)

The reference is a fixture created from the example's initial state, using the
same content and components. It is not an independent translation from an
external design tool. The later screens extend that visual direction.

### 2. Without mockups: schedule a focus session

Create the visual direction and a complete flow. The scheduled session must
preserve the selected activity, duration, and date.

#### Prompt

```text
Use $improve-design to design a simple focus-session planner.
I have no mockups. Create a coherent high-fidelity interface with Spanish copy.
Let me choose an activity, adjust the duration and date, review the details,
confirm, and see the scheduled session before giving feedback.
Include useful validation and back navigation that preserves my choices.
Save the proposal under review/focus-session/.
```

#### Screenshots

<img src="examples/without-mockups/result.jpg" width="260" alt="Scheduled writing session with a duration of 40 minutes and the selected date.">

[Example details](examples/without-mockups/README.md) ·
[Prototype file](examples/without-mockups/index.html)

For a smaller visual question, ask for a single high-fidelity mockup instead:

```text
Use $improve-design to improve the hierarchy of this account card.
A single high-fidelity mockup is enough. I do not need navigation or a scenario index.
```

## Installation

Use Node.js 22.20 or later and npm, as required by the
[skills CLI](https://github.com/vercel-labs/skills#install-a-skill).
From your project, run:

```bash
npx skills add jerolan/improve-design
```

Select the skill and the agents to install it for. Installation is project-local
by default. To install only this skill for Codex across projects:

```bash
npx skills add jerolan/improve-design --skill improve-design -a codex -g
```

To inspect the available skills without installing:

```bash
npx skills add jerolan/improve-design --list
```

See the [CLI installation reference](https://github.com/vercel-labs/skills/blob/main/docs/commands.md#skills-add)
for other agents and options.

## Usage and review

Invoke `$improve-design` and describe the interface, the user task, and the
decisions to preserve. Supply any existing design files, screenshots, or assets.

A multi-scenario prototype opens with an index. Selecting a scenario shows its
context, steps, and expected result. **Start** opens an app-like view without
review instructions. The user completes the journey, sees its outcome, and gives
feedback. Free exploration can be an additional option.

A single screen or short scenario does not need an index. High fidelity is
required in both modes; the amount of interaction depends on the review.
Before delivery, compare the visual result with the reference and walk every
advertised flow through its final result.

Partial feedback remains partial. Accepted decisions survive revisions.
Approving a design does not authorize production implementation or deployment.

## Run the examples locally

Download or clone this repository and open each example's `index.html`.
No application dependencies or external services are required.

If Python is already installed, you can also serve the repository locally:

```bash
python3 -m http.server 8765 --bind 127.0.0.1
```

Open [the example with mockups](http://127.0.0.1:8765/examples/with-mockups/) or
[the example without mockups](http://127.0.0.1:8765/examples/without-mockups/).
Stop the server with `Ctrl+C`. This address works only on the serving computer.
Phone access requires an authorized local-network setup.

The examples simulate their operations in memory. They save feedback in the
browser when storage is available and let the user download it. Feedback does
not reach the agent or another device automatically. If browser storage is
unavailable, export comments before closing the page.

## Compatibility and verification

The skill does not require a specific editor, framework, or plugin. It uses
the tools available in the project. Rendering, browser interaction, and screenshot
checks require tools that support them; blocked checks must be reported.

Both example flows were walked through to their outcomes.
[VALIDATION.md](VALIDATION.md) records the checks and their limits in Spanish.
The examples do not create real library reservations or calendar events.

## License

[MIT](LICENSE), Copyright 2026 jerolan.
