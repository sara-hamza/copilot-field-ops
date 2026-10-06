# copilot-field-ops

## What it does

Field Assistant: interprets optical and test results, suggests the next test and writes site close-out notes.

Part of the **department-copilots** suite: local-only copilots where the employee provides the input, Claude analyses it on the machine, and the employee decides what to do. No CRM, NMS, email or system integrations.

## Install

```bash
claude plugin marketplace add sara-hamza/department-copilots
```

```bash
claude plugin install field-ops@department-copilots
```

Type what the test set or the ONT shows, drop in a photo, or paste your rough notes. Get back the likely cause, the single next test to run, a compliance read of the photo, or a clean site visit summary.

| Command | Use when |
|---|---|
| `/field-ops:interpret <readings>` | You have ONT status, RX levels, OTDR events or power meter readings and want to know what they mean |
| `/field-ops:next-test <what you have done so far>` | You want only the next cheapest test, not the whole analysis |
| `/field-ops:site-summary <rough notes>` | Turn your notes into a SITE VISIT SUMMARY for the ticket |
| `/field-ops:photo-check <photo(s)>` | Check a pit, closure, FDH, lead-in or ONT photo for visible compliance concerns |

Requires `copilot-common` (screenshot-reader for photos). Works with `sticky-notes` for carrying site context across the day.

Reference knowledge lives in `skills/field-assistant/references/`. The optical ranges, OTDR thresholds and test order there are sensible defaults marked `CUSTOMISE`; replace them with the company's field standard.
