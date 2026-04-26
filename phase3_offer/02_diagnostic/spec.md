# Weekly Self-Survey Specification

## Purpose

Define the design principles, evidence base, and constraints for building an effective weekly check-in for resistance training clients 40+. This is the spec that generates the deliverable (see `weekly_checkin.md`).

---

## Product Context

| Product | Format | Use Case |
|---------|--------|----------|
| **Full Diagnostic** | Questionnaire + scored report | Pre-consultation, sent before one-time consultation |
| **Short Self-Survey** | Weekly check-in (this spec) | Embedded in Everfit on-ramp and follow-up programs |
| **Consultation** | One-time, hourly rate | Discuss results, form recommendations, build implementation plan |

The weekly self-survey is embedded in all Everfit programs. It tracks signals that the workout data alone cannot capture, and flags problems before they become dropout.

---

## Design Principles

1. **Don't duplicate Everfit data.** Workout tracking already captures objective progress (weight, reps, sets) and consistency (session completion). The survey should capture what the data can't.

2. **One concept per question.** Each question measures one thing. "How did you sleep and feel this week?" is two things.

3. **Recovery-weighted.** For 40+ adults, recovery is typically the binding constraint — not effort or knowledge. Recovery gets more questions than any other domain.

4. **Include psychology.** Dropout is driven by perception (progress, enjoyment), not just physiology. At least two questions should capture psychological state.

5. **One open question for context.** Some signals (concurrent activity, life events) don't fit a scale. A free-text field captures what scales can't.

6. **Directionally aligned.** All scored questions point the same direction: higher = better. This keeps scoring simple and interpretation intuitive.

7. **Completable in under 2 minutes.** Friction kills compliance. 5-6 questions max for scored items.

---

## Domains

### Recovery (primary — 3 questions)

**Research basis:**
- Sleep quality is "the most important recovery variable" for 40+ adults. Sleep deprivation impairs force production, reduces testosterone and GH, increases cortisol. (Knowles et al., 2018)
- Older adults experience prolonged soreness and force decrements from exercise-induced muscle damage. Recovery time course is a key signal for program adjustment. (Clifford, 2019; Morán-Navarro et al., 2017)
- "Sleep quality, nutrition, and total life stress are stronger determinants of recovery than age alone." (05_recovery_adaptation.md)

**Required signals:**
- Sleep quality
- Post-session recovery rate (day-after soreness/fatigue)
- Life stress

**Why three separate questions instead of one composite:** Sleep, soreness, and stress are independent inputs to recovery. A client can sleep well but be highly stressed. A client can be low-stress but wrecked from a hard session. The individual signals are more diagnostic than a single "how recovered do you feel."

### Psychology (secondary — 2 questions)

**Research basis:**
- Perceived lack of progress is the top dropout predictor, independent of actual progress. (02_adherence_dropout.md)
- Boredom and dread are top dropout predictors. (02_adherence_dropout.md)
- Self-Determination Theory: autonomy, competence, and relatedness predict long-term adherence. Intrinsic motivation (enjoyment) outperforms extrinsic goals (aesthetics). (06_identity_psychology.md)

**Required signals:**
- Enjoyment vs. dread
- Perceived progress (subjective, not objective)

### Context (informational — 1 open question)

**Research basis:**
- Concurrent training interference: running and high-volume endurance work attenuate strength gains. (Wilson et al., 2012; Huiberts et al., 2024)
- Sprint/high-intensity work causes less interference than long slow distance. (Ferraro-Farro et al., 2026)

**Required signal:**
- Free-text: other physical activities + open notes

---

## What to Exclude and Why

| Excluded | Reason |
|----------|--------|
| Objective progress (weight/reps) | Captured by Everfit workout tracking — redundant |
| Session completion / consistency | Captured by Everfit attendance data — redundant |
| Identity questions ("do you consider yourself a lifter") | Don't change week to week — better for full diagnostic |
| Program satisfaction | Overlaps with enjoyment — one question covers both |
| Energy/readiness going into sessions | Composite of sleep + soreness + stress — the three individual signals are more diagnostic |
| Protein intake | Hard to self-assess weekly — better for full diagnostic or nutrition check-in |

---

## Scoring Framework

- **Scale:** Linear Scale 0-5 (Everfit native type)
- **Total:** Sum of all scored questions
- **Direction:** Higher = better on all scored questions
- **Flag threshold:** <= 60% of max score for any single week
- **Flag threshold:** Any single question scores 0 or 1
- **Flag threshold:** Enjoyment or Progress drops 2+ points from prior week

### Why 60% and not 50%:

With only one week of history visible (no graphing), catching problems early matters more than avoiding false positives. A 60% threshold flags earlier, giving Matt a chance to intervene before the client disengages.

### Why week-over-week drops on Q4/Q5 specifically:

A sudden drop in enjoyment or perceived progress is a leading indicator of dropout. Recovery scores can fluctuate with life events without threatening adherence. But when a client stops enjoying training or stops feeling progress, they're close to quitting.

---

## Platform Constraints

- Everfit Linear Scale type: 0-5 range
- Everfit shows current + prior week only (no trend graphing)
- Short Answer type available for open questions
- Survey embedded as weekly check-in within Everfit programs
- Scoring and flagging are manual (Matt reviews)

---

## Deliverable

See `weekly_checkin.md` for the final survey ready to build in Everfit.
