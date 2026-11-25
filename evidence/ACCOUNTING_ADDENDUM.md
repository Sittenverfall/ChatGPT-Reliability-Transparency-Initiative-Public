# Accounting evidence addendum — checked 2026-11-25

## OpenAI Work and Codex reporting

[OpenAI Help Center — Reviewing Work and Codex usage](https://help.openai.com/en/articles/20001478-reviewing-work-and-codex-usage-and-using-personal-analytics-in-chatgpt-desktop) was opened on 2026-11-25. It applies to eligible Enterprise/Edu workspaces and explicitly says that displayed Work/Codex chat usage is an estimate for the main conversation, not a complete record of every billable action. The article lists delegated sub-agents/separate tasks, certain separately billed tools, background activity, reporting delays and unavailable records as exclusions/limits; activity missing from a chat total can still consume credits and count against limits. The article directs complete-spend questions to workspace billing/usage records.

**Scope limit:** this official article does not prove that Plus, Pro or Business accounting has the same omission pattern. It also distinguishes chat-level estimates, monthly allowances, usage history and complete spend records. Do not describe a displayed estimate as an invoice.

## Announced shared allowance

[OpenAI Help Center — Understanding ChatGPT and Codex usage limits](https://help.openai.com/en/articles/20001625-understanding-chatgpt-and-codex-usage-limits) was opened on 2026-11-25. The article says that starting in December, Plus, Pro and Business allowances will be shared across ChatGPT and Codex and measured in tokens, with Instant excluded. It says a small group may see the changes before December.

**Status wording:** this is an announcement and early-feedback notice. It is not evidence that the transition is complete, applies to every account, or has reached a particular user. The article describes combined remaining usage/reset information in Settings → Usage; it does not promise itemized token accounting for each conversation.

## Comparator evidence

- OpenRouter's [generation metadata API](https://openrouter.ai/docs/api/api-reference/generations/get-generation) documents request-level token and cost metadata. Its [Activity dashboard announcement](https://openrouter.ai/blog/announcements/activity-dashboard/) describes spend, request, token and cache views with drill-down to individual requests. These are API-router and dashboard records, not a ChatGPT subscription ledger.
- Cursor's [current model and pricing documentation](https://cursor.com/docs/models-and-pricing) describes plan usage pools and remaining/reset information. This is allowance evidence and does not establish per-chat context occupancy. A forum post is not needed to support this distinction.
- [CRTI's 12-platform comparison](COMPETITOR_COMPARISON.md) records the other dated API, CLI, context and allowance sources and their limits.

## Required accounting distinctions

Keep these measures separate in public wording: (1) active context occupancy and limit; (2) plan/account allowance and reset; (3) request/task/session token use; (4) currency cost or estimate; (5) cache-hit counts/savings; (6) tool or background activity; and (7) storage/persistence/recovery. A count in one scope does not establish a complete ledger in another. Unknown scope or missing data must be labelled unknown, not zero or absent.

## Founder-observed Plus dashboard and Goal usage (25 November 2026)

The user supplied screenshots of one completed Codex Goal: 496,838 reported tokens and 34 minutes 35 seconds elapsed. The settings overview showed 96% of the five-hour allowance and 24% of the weekly allowance remaining. The visible UI stated that Codex, Work, Workspace Agents and ChatGPT for Excel share the displayed allowance; ordinary Chat was excluded at observation time. Analytics for a weekly period showed a prior-day update timestamp and explicitly warned that some usage data was unavailable. Several visible chat rows lacked usage values; some historical window totals exceeded 100%. The exact interpretation of those totals is unknown. The displayed Goal token count is not a complete billing ledger; no pre-run measurement exists, so neither the percentage used by this Goal nor an absolute plan token allowance can be derived. No cost-efficiency comparison with Work is established.

The same user observed a Codex model-change warning recommending a new session or returning to the prior model. Ordinary Chat separately offered reasoning-effort choices. The model and effort used throughout the Goal are not independently verified. The [Responses API guidance](https://developers.openai.com/api/docs/guides/latest-model) describes possible loss of prior reasoning items for certain model/history changes; [prompt-caching guidance](https://developers.openai.com/api/docs/guides/prompt-caching) describes supported effort changes without rewriting the cached prefix. These are API-specific documented mechanisms, not proof of consumer implementation or a causal link to conversation/tool failures. Request model/effort attribution, context integrity and reprocessing usage reporting, not disclosure of hidden reasoning content.

These are dated, scoped observations of one Plus account, not a billing audit. They are separate from the Enterprise/Edu documentation and the announced December transition.
