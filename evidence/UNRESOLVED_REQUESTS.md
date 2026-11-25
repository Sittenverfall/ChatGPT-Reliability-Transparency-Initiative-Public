# Unresolved community requests — reviewed 2026-11-25

These entries document requests and responses visible on the linked community pages. They do not establish implementation status, product-wide failure rates, or common causes. Refer to [SOURCE_REGISTER_DRAFT.md](SOURCE_REGISTER_DRAFT.md) for source metadata and limitations.

## Context capacity and handover

- **E01 — June 18, 2026:** A user requested a context-limit progress indicator. An OpenAI Support reply dated **September 7, 2026** said the request for a progress indicator and early warning would be passed along, with no timeline. The exact forum timestamps are verified; no elapsed-time claim is needed. [Original thread](https://community.openai.com/t/add-a-context-limit-progress-indicator-in-chatgpt/1384047).
- **E02 — September 18, 2026, with follow-up September 19:** One feature-request thread asks for separate context and account-usage information, advance warnings and structured handover. It contains further reports and cross-references; those are not an independent prevalence sample. [Original thread](https://community.openai.com/t/feature-request-add-a-conversation-capacity-meter-and-automatic-handover-warning-to-every-chatgpt-chat/1398772).
- **E03 — October 7, 2026:** A user reports encountering a “conversation is too long” notice and requests advance warnings and handover. Replies on the same thread are user reports, not product telemetry. [Original thread](https://community.openai.com/t/feature-request-context-window-warning-meter-before-hitting-the-conversation-is-too-long/1404078).
- **E04 — November 12, 2026:** A user reports interrupted development work and difficulty carrying decisions into a new chat. An OpenAI Support reply dated November 17 says it will share the request for in-place compression/discarding older context and has no timeline. The response acknowledges feedback; it does not confirm a defect or planned change. [Original thread](https://community.openai.com/t/chatgpts-premature-context-limits-are-disrupting-development-work-and-causing-repeated-loss-of-productivity/1415630).

These threads concern related user needs. Do not count posts/replies as separate verified incidents, infer a shared technical cause, or treat a request/acknowledgment as implementation evidence. OpenAI's current Free-plan help guide is separate evidence and has Free-plan scope only (see E11).

## Data export reports

- **E05 — November 18, 2026:** A community member reports repeated incomplete ZIP attempts for an export expected to be about 4.25 GB and recovery through authenticated HTTP range requests. That author reports byte-range/ETag checks and successful ZIP testing, while stating the cause is unknown. This is a separate first-person community report, not the CRTI founder's separate ~2.4 GB report. Do not combine the two. [Original thread](https://community.openai.com/t/large-chatgpt-data-exports-repeatedly-cut-off-how-i-recovered-mine/1417681).
- **E12 — OpenAI export help:** The official guide explains eligibility, export delivery and link expiry, local viewing, and contacting Support if a download stops or an export appears incomplete. It does not describe a resumable range-download feature or identify the cause of a particular failure. [Official guide](https://help.openai.com/en/articles/7260999-exporting-your-chatgpt-history-and-data).

## Status

The current implementation status of the requested context and handover features is not established by these historical request threads. The official Free-plan notice and export guides document their stated scopes; neither confirms or disproves the individual reports above. Recheck current product documentation before publication. No public post or reply has been sent as part of this draft.

## Browser-based backup completeness (E14)

The original Reddit post and comments, reviewed as user-supplied screenshots on 2026-11-25, report that copying and printing long conversations can silently omit sections. Later comments also report failures in Firefox, so it is not a verified universal workaround. See [E14 in the source register](SOURCE_REGISTER_DRAFT.md) and [the original Reddit URL](https://www.reddit.com/r/ChatGPTcomplaints/comments/1tb905l/). This is separate from E05 and account-wide ZIP delivery. Exact post date and independent reproduction remain unverified.
