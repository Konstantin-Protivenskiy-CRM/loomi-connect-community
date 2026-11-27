# Gap checklist: settle these before any build or analysis

Most repeated questions in Loomi Connect work come from items on this list that were raised late. Ask them in one message at the start. Mark each answer as given, assumed or unknown. Do not design over an unknown.

## Objective and measurement

- What is the outcome, and what is the success threshold? For example, a conversion rate and the uplift you need.
- Which control group and which logging convention applies? Where does the split happen, which event name is used, and which control types exist?
- Which window counts as an outcome? State the attribution window you will report on.
- Is one change or a test being measured? If a test, what is the sample size and the minimum detectable effect?

## Scope and IDs

- Which project, and which campaign or scenario ID (live and draft)? Is there an older scenario that must be stopped?
- Which tracking key scopes the events: campaign ID, campaign name, or a custom program property? Confirm that the key is populated consistently across the full period.
- Which segments, aggregates and expressions does the flow read, by ID and by value?

## Business rules (ask before designing)

- What can a customer still do at this point in the journey?
- Which offers exist, and which can actually be sent? Check earlier decisions for offers that were rejected, and find out why.
- Which eligibility rules apply, such as plan or tier changes that are allowed, or groups that are excluded from an offer?
- What should happen to a customer who completes the goal mid-flow, or who leaves?

## Channels and consent

- Which channels are allowed (email, SMS, push per platform, banner)? Which consent gates each?
- What is the fallback when a channel is unavailable? Who exits when no channel is available?
- Is there a frequency rule, quiet hours, or interaction with other campaigns?

## Data

- How fresh is each field the flow uses in a time-based decision? Note any known lag.
- Which fields are reliable enough for a decision, and which need a wait first?
- What are the known data gaps, such as a field captured for only part of the customers?

## Cost and window

- Which time window is acceptable for analysis, given the platform's cost limit?
- Is a saved report available for the number, so an ad hoc query is not needed?

## Editing and ownership

- Will anyone edit the draft in the Bloomreach UI? If yes, fetch the current version before every write and use node patches.
- Who signs off the copy, the offer and the launch? Which items stay placeholders until then?
- What must be deleted or stopped at go-live, such as test scenarios or the older scenario?

## Definition of done

- What will be read back and reported as verified?
- What stays as an open item, and who owns it?
