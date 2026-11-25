# Codex Goals evidence for CRTI-017

**Evidence checked:** 2026-11-25. **Status:** documented behavior plus limited live state observation. This note does not claim that all proposed completion controls are implemented.

## Primary documentation

OpenAI's [Using Goals in Codex](https://developers.openai.com/cookbook/examples/codex/using_goals_in_codex) guide was opened on 2026-11-25. It describes Goals as persisted, thread-scoped objectives with lifecycle and budget state. It says a Goal should be marked complete only after checking relevant concrete evidence and explains that user/system controls govern pause, resume, clear and budget-limited transitions. The guide is a product source for the documented design, not independent proof that every host enforces every step.

## Live Codex Goal observations

Two Goal states were observed through the platform Goal API in this thread:

1. A simple branch/path verification Goal ran `git branch --show-current` and `Test-Path handoff/CODEX_TASK.md`; the command results were `crti-draft` and `True`. After those checks, `update_goal` returned `status=complete` and a subsequent Goal result recorded the objective as complete.
2. The current CRTI publication-candidate Goal was retrieved with `get_goal` after a continuation. The result contained its active objective and `status=active` while the work remained incomplete.

These observations verify that a Goal's persisted objective/status and concrete command output were observable across turns in this execution. They support using platform Goal state as evidence in an acceptance test. No diagnostic receipts, personal correspondence, screenshots or conversation transcript are included.

## What this evidence does not prove

The two observations did not attempt to mark a Goal complete with missing, stale, contradicted or model-only evidence. They therefore do not prove that the platform independently blocks a false completion, identifies each unmet criterion, or enforces the same behavior on every Codex host. Public proposal wording must present platform-controlled validation as a requested capability. CRTI-017 and CRTI-019 remain proposed requirements until those negative and positive cases are tested against an identified platform version.

## Required acceptance cases

- **Positive:** provide fresh authoritative evidence for every criterion; verify persisted objective, evidence references, completion state and completion output.
- **Negative:** remove one criterion's evidence, substitute a contradictory result, substitute stale evidence, or provide only a model assertion. Each case must keep the Goal non-complete and expose the exact unmet criterion.
- **Lifecycle:** confirm pause, resume and budget-limited transitions use the documented user/system controls and do not falsely mark the objective complete.

Record host/version, criterion IDs, evidence sources, timestamps, requested and actual transitions, and error/status identifiers. Do not treat this draft's own prose or a green check as proof that the platform implements the proposed gate.

## Subsequent completion and continuity observation (25 November 2026)

User-supplied Codex screenshots show a longer Goal running through multiple steps, then a stalled/blocked state after a private Git push required approval and direct access to the required ChatGPT Library records was unavailable. The user authorized the private push; a separate QA chat reconciled and verified the Library checkpoints. The remote private-branch contents were checked independently. The Codex closure reported `READY_FOR_PUBLICATION_REVIEW`, Goal `complete`, 496,838 tokens and 34 minutes 35 seconds elapsed, and explicitly stated that it did not access the Library directly. This is evidence of one workflow with autonomous progress and cross-surface recovery, not proof that all host-side completion checks are enforced. No publication occurred. A transient disappearing approval prompt was reported by the user; its exact identity/cause was not confirmed.

A separate earlier tool-availability incident showed missing verified timestamps and reported unavailable tools interspersed with reported successful time calls; the underlying dispatch/exposure/invocation cause remains unknown. No server outage or model-transition cause is established. Request persistent visible pending approvals, authorized resume without duplicate work, actual call telemetry and clear cross-surface storage capability boundaries under requirements 17–22.
