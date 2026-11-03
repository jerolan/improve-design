# Complete flows and recoverable feedback

## Define the journey

For each advertised scenario, keep a small contract containing its title, context, starting data, user actions, and observable end state. Include alternatives only when they materially affect the decision being reviewed. Do not mirror every internal state as a separate scenario.

For example, reserving a book starts with an available title, allows choosing a collection day, requests confirmation, and ends with a reservation receipt showing the chosen title and day. Selecting a thumbnail that opens a receipt directly does not demonstrate this journey.

## Separate preparation from interaction

Put the narrative, steps, expectation, and demonstration boundaries before **Start**. Once started, show the app rather than a phone-shaped frame surrounded by instructions. Use the available viewport and respect safe areas. A browser's native chrome may remain; do not require a browser fullscreen permission prompt to achieve an app-like view.

Keep an unobtrusive exit available. Let users reach the outcome naturally, then offer a review action. Back and cancel should follow the product's intended behavior. They should not approve a choice, erase saved feedback, or pretend that an unfinished scenario is complete.

## Model enough behavior

Represent the actions and state needed to evaluate the scenario. Inputs should change the result; selected options should appear in the confirmation; saving should update the next screen. Prevent accidental double application where relevant. Simulate only the required boundaries, such as authentication or a backend request, and identify the simulation before interaction.

For editing or replacement, compare the current value with the proposed value and preserve the current version until confirmation. Keep calculations consistent with the displayed data. A revised prototype must also revise its references and scenario descriptions.

## Collect feedback

Associate each comment with a scenario or screen and the version under review. Support partial reviews and an explicit reviewed status. Let users retain notes as they move between scenarios and replay them.

Default to temporary, in-memory feedback in the current tab. Preserve it across navigation and replay, but warn that reload or closing the tab loses it. Provide a Markdown download with the scenario, version, completion status, comments, and result context. Tell the user to attach the file to their agent or paste it as a prompt. The agent cannot read these notes automatically. Add durable storage or a submission service only when requested; describe its destination and permissions. A running prototype update must not silently destroy unexported feedback.

Do not tell a user that comments were received unless they were actually read. For device-only comments, ask for an export or use a user-authorized collection channel. Adding a server endpoint or publishing private feedback requires considering the destination and the user's authorization.

## Verify and close

Walk each scenario with the same controls the user will use. Record its entry, final result, relevant inputs, and any blocked checks. Use fictitious data in isolated prototypes. Exercise an invalid input or cancellation when the advertised scenario depends on it.

Finish with a short review record describing accepted decisions, requested changes, remaining limitations, and the next authorized action. Closing a design review does not authorize implementing the production product. Preserve original feedback and the latest coherent design rather than generating a new map for every iteration.
