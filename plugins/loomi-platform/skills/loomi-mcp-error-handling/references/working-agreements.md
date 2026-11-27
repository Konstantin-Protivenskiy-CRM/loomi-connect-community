# Working agreements

These habits cut repeated questions and rework when you work with an AI assistant and Loomi Connect.

## Start every task with a brief

Paste this block as the first message. Fill in what you know, and write "unknown" for the rest.

```
Goal:
Scope IDs: project / scenario / campaign / any legacy scenario to stop:
Business rules I know:
Offers and their status (sendable? signed off?):
Channels and consents:
Data lags I know about:
Cost window allowed:
I will edit the draft in the UI: yes / no
Done means: (what you will read back and report)
Ask me before: (writes, full rewrites, any unknown that blocks the design)
```

## Ask for these explicitly

- "Read back every node you change, and list them."
- "Before any write, fetch the current version."
- "If a write times out, check whether it was saved before retrying."
- "Mark each number as measured, derived, or assumed."
- "Tell me what you could not verify."

## Answer blocking questions in one message

Design work stalls when a fact arrives late. When the assistant asks a blocking question, answer it in one message and state any assumption you are making. Do not wait for the assistant to find the answer itself.

## Split large work

Do one stage per turn: analysis, then design, then copy, then build. A build that follows a design the team has not approved is the most expensive kind of rework. Long single threads also make early decisions hard to find, so start a fresh conversation for each stage.

## Keep one state note

After each stage, ask for a state block: IDs, decisions with reasons, open items, and what was verified. Save it with the campaign's notes. Start a new conversation from that block when a thread gets long, instead of relying on a summary.

## When you edit in the UI

Tell the assistant what you changed and name the node. Then it fetches the current version before it writes. Without this, it may propose a fix you have already made.

## When a claim is unsourced

If the assistant gives a percentage or a share without a query behind it, ask: "Which query gives this number?" Do not put an unsourced figure in a document, a post or a decision.

## Hand-over

When a conversation ends mid-build, ask for: the scenario ID, the last successful write, anything that may be half-saved, the open items, and the test objects to delete.
