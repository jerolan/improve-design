# Without mockups: schedule a focus session

[Español](README.es.md) · [All examples](../../README.md#use-cases)

Create a finished visual direction and let the user schedule a session.
The final result must preserve the selected activity, duration, and date.

## Prompt

Run from the repository root.

```text
Use $improve-design to create a simple focus-session planner.
I have no mockups. Design a coherent high-fidelity interface with Spanish copy.
Let me choose an activity, set duration and date, review, confirm,
and see the scheduled session before giving feedback.
Include useful validation and back navigation that preserves my choices.
Save the proposal under review/focus-session/.
```

## Screenshots

<img src="result.jpg" width="260" alt="A scheduled 40-minute writing session with the selected date.">

The example defines its own visual direction: ivory background, plum text,
lavender controls, system typography, and shared components for each state.
No separate mockup is required to start.

## Try the prototype

Download this example and open `index.html` in your browser. GitHub's
[index.html link](index.html) shows the source file. Read the introduction and
select **Iniciar recorrido**.

1. Choose an activity.
2. Enter the duration and date. Try a duration below 10 minutes to see validation.
3. Review the details and confirm.
4. Check that the result preserves the selected activity, duration, and date.
5. Select **Dar feedback**. You can also exit earlier for a partial review.

Back preserves inputs. Replay resets the simulated session and keeps comments.
Reaching the scheduled-session result completes the journey.

The session does not create a real calendar event. Feedback stays in this browser
when storage is available and can be exported. It is not sent to the agent or
another device.
