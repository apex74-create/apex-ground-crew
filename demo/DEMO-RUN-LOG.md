# Apex Ground Crew v0 — Demonstration Run Log

**Scope:** AGC-DEMO-001 — Sample Bakery, Johannesburg, MI
**Need as filed:** "one-page site that says what we bake and how to order"

## The run

- **Time in:** Thu Nov 5, 2026, 09:54:57 EST (14:54:57 UTC) — sample scope filed with the live intake form's exact six fields.
- **Time out:** Thu Nov 5, 2026, 11:10:18 EST (16:10:18 UTC) — deliverable complete and filed.
- **Elapsed:** 1 hour 15 minutes wall clock. Most of that was two external stalls, named below — the hands-on assembly was minutes. No rounding: the stalls are part of this run's true record.

## What the factory did

1. Assembled the scope from the form input alone: `demo/sample-bakery-scope.json` (the scope as filed).
2. Produced one deliverable end-to-end from that input: the Sample Bakery one-page site copy — headline, what-we-bake list, how-to-order block.
   - File: `demo/sample-bakery-one-pager.html`
   - Live: https://apex74-create.github.io/apex-ground-crew/demo/sample-bakery-one-pager.html
3. Filed the scope into Mav's intake: `~/workspace/your_files/ground-crew-intake/AGC-DEMO-001-sample-bakery-scope.json` (local copy of the same record as `demo/sample-bakery-scope.json`).

## Filing-rule state (square corners)

- The filing rule names two addressees: the business mailbox + Mav's intake. Mav's intake leg is verified (files above).
- The business-mailbox leg: the live form posts to FormSubmit for delivery to masteradminapex@apex-airsolutions.com. From the factory network, formsubmit.co is unreachable — DNS resolves, every connection times out (HTTP 000, three attempts, 09:55–10:20 EST); no activation or delivery mail arrived. Real visitors reach FormSubmit from their own networks; the form also carries a mailto fallback that hands the scope to the visitor's own mail app addressed to the business mailbox.
- The factory's direct Gmail delivery of this demo scope was attempted and is BLOCKED on a Gmail egress approval that expired unapproved on the worker session (approval id connector-attempt-4a70c86e08b2d5039133db40aad13b6ca206d8aeb71dd606ec3fbf7f29d86374). One approval in the main session clears it; the scope email is composed and ready (`~/workspace/processing/agc/scope_mail.eml`).
- Verdict on the mailbox leg: wired and addressed, delivery from the factory side pending that one approval — stated plainly, not rounded up to "verified."

## Stalls on this run (for the record)

1. FormSubmit unreachable from the factory network (see above).
2. Gmail send approval expired (~30 min wait) + two failed preparations after it.
3. The VM's /tmp was wiped mid-run; build scratch was rebuilt under `~/workspace/processing/agc/`. No repo or deliverable loss — everything in the repo was already committed.

## v0 proof statement

The door is connected to the machine: a scope went in through the form's fields, the factory assembled it, and a finished one-page deliverable came back out against the same scope id — page live, scope filed, log written. The one open thread is the mailbox delivery approval named above.
