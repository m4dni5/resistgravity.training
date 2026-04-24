# Diagnostic Framework Design

## AGENTS.md — Context for Subagents

### What This Is

Designing the diagnostic service for Audience B: adults 40+ who are already doing RT but not getting results.

### Research Inputs

From Phase 2 (barriers_adherence/):
- `05_progression_failures.md` — Progressive overload failure, junk volume, program hopping
- `02_adherence_dropout.md` — Perceived lack of progress drives dropout
- `03_time_efficiency.md` — Recovery deficits, concurrent training interference
- `06_identity_psychology.md` — Motivation collapse when results stall

From Phase 1 (effective_rt/):
- `02_programming_variables.md` — Volume, frequency, intensity, progression
- `03_concurrent_training.md` — Interference effect from other activities
- `05_recovery_adaptation.md` — Sleep, protein, stress as limiting factors

From Benefits (benefits/):
- `00_summary.md` — The persuasive case for RT (for the guide/copy)

### Key Design Constraints

- Target: 40+ adults who lift but aren't progressing; may also be active in outdoor sports
- Matt's edge: diverse movement background (martial arts, dance, Olympic lifting, powerlifting, strongman, CrossFit, mountain guiding) — he can diagnose movement quality issues
- The diagnostic should be the manual prototype for a future app that integrates RT with lifestyle analysis
- Could be delivered in-person (ideal) or remotely (video + questionnaire)

### Open Questions (Pending Matt's Input)

1. What's the deliverable? (Written assessment? Rebuilt program? Single session with notes?)
2. Is this a standalone service, or a gateway to ongoing coaching?
3. Should this be the manual version of the app methodology you want to build?
4. Can this be delivered remotely, or does it require in-person assessment?

### Deliverable

A spec document defining:
- Assessment protocol (what to evaluate)
- Diagnostic questions and criteria
- Common failure modes and their solutions
- Deliverable format (what the client receives)
- How it connects to the on-ramp or ongoing services
