# Diagnostic Framework Spec

## Purpose

Design an evidence-based questionnaire that scores failure modes in a client's current RT program. Two versions: a full pre-consultation assessment and a short weekly self-survey for Everfit.

---

## Product Architecture

| Product | Format | Use Case |
|---------|--------|----------|
| **Full Diagnostic** | Questionnaire + scored report | Pre-consultation, sent before one-time consultation |
| **Short Self-Survey** | Weekly check-in | Embedded in Everfit on-ramp and follow-up programs |
| **Consultation** | One-time, hourly rate | Discuss results, form recommendations, build implementation plan |

### Full Diagnostic Flow
1. Client purchases consultation (hourly rate)
2. Full diagnostic questionnaire sent prior to session
3. Matt scores and reviews results
4. Consultation: discuss findings, identify failure modes, build implementation plan
5. Client receives written summary + recommended next steps (which may include on-ramp, follow-up, or monthly online)

### Short Self-Survey Flow
1. Embedded in Everfit programs as weekly check-in
2. Client answers 5-7 questions each week
3. Scores track over time (trends visible to Matt and client)
4. If scores trend downward → flag for review

---

## Failure Mode Categories

Based on Phase 2 research:

### 1. Program Design Failures
- No progressive overload
- Junk volume (too many exercises, insufficient intensity)
- Insufficient volume
- Wrong program for goals
- Program hopping

### 2. Recovery Failures
- Inadequate sleep
- High life stress
- Insufficient protein intake
- Too much concurrent activity

### 3. Execution Failures
- Poor movement quality
- Not training close enough to failure
- Inconsistent attendance
- Incorrect technique

### 4. Psychological/Behavioral Failures
- Loss of motivation
- No identity shift ("I'm not a lifter")
- Perceived lack of progress
- Boredom / lack of enjoyment

---

## Full Diagnostic Questionnaire

### Section A: Training History
1. How long have you been doing resistance training? (0-6 months / 6-12 months / 1-3 years / 3+ years)
2. How many different programs have you tried in the last year?
3. When was the last time you increased the weight or reps on your main lifts?
4. How many sessions per week are you currently doing?
5. How long is a typical session?
6. Walk me through your last session — what exercises, sets, reps, and weights?

### Section B: Program Quality
7. Do you follow a structured progression plan? (Yes / Somewhat / No)
8. How many exercises do you typically do per session?
9. Do you track your weights and reps? (Always / Sometimes / Never)
10. Do you know what your current max is for your main lifts? (Yes / No / Roughly)

### Section C: Recovery Profile
11. How many hours of sleep do you get per night on average?
12. How would you rate your stress level? (1-10 scale)
13. How much protein are you eating daily? (g/kg if known, or estimate: low / moderate / high)
14. What other physical activities are you doing each week? (List + approximate hours)
15. How often do you feel fatigued or sore going into a training session? (Rarely / Sometimes / Often / Always)

### Section D: Goals and Psychology
16. What are you trying to achieve with resistance training? (Open-ended)
17. Do you feel like you're making progress? (Yes / Somewhat / No)
18. How would you describe your relationship with training? (Enjoy it / Neutral / Dread it)
19. Do you consider yourself "someone who lifts"? (Yes / No / Sometimes)
20. What's the biggest thing getting in the way of your training? (Open-ended)

### Section E: Movement Quality (if in-person or video available)
21. Can you perform a bodyweight squat to depth without pain? (Yes / No / With difficulty)
22. Can you hinge at the hips without rounding your lower back? (Yes / No / With difficulty)
23. Are there any movements that cause pain or feel wrong? (List them)

---

## Scoring Framework

Each section maps to failure mode categories. Scoring identifies the primary and secondary failure modes.

### Program Design Score (Questions 2-10)
- Low score indicators: No progression tracking, program hopping, too many or too few exercises, no structured plan
- High score: Structured program, progressive overload, appropriate volume

### Recovery Score (Questions 11-15)
- Low score indicators: <6 hours sleep, high stress, low protein, excessive concurrent activity
- High score: 7+ hours sleep, manageable stress, adequate protein, balanced activity

### Psychological Score (Questions 16-20)
- Low score indicators: No progress perception, no identity, dread, unclear goals
- High score: Clear goals, identity shift, enjoyment, perceived progress

### Movement Score (Questions 21-23)
- Low score indicators: Pain, compensation, inability to perform basic patterns
- High score: Pain-free, good form, confidence in movement

### Output
- Primary failure mode (highest priority to address)
- Secondary failure mode (next priority)
- Recommendations (ranked by impact)
- Suggested next step (on-ramp, follow-up, monthly online, PT referral)

---

## Short Self-Survey (Weekly, for Everfit)

5-7 questions, scored 1-5, tracked over time:

1. **Progress:** Did you increase weight or reps on any exercise this week? (1=No / 3=Somewhat / 5=Yes)
2. **Consistency:** How many of your planned sessions did you complete? (1=0 / 2=1 / 3=2 / 4=3 / 5=All)
3. **Recovery:** How was your sleep this week? (1=Poor / 3=OK / 5=Great)
4. **Energy:** How did you feel going into sessions? (1=Drained / 3=Normal / 5=Energized)
5. **Enjoyment:** How much did you enjoy training this week? (1=Dreaded it / 3=Neutral / 5=Loved it)
6. **Confidence:** Do you feel like you're getting stronger? (1=No / 3=Somewhat / 5=Yes)
7. **Open:** Anything getting in the way? (Free text, optional)

### Scoring
- Total score out of 30 (questions 1-6)
- Weekly trend visible in Everfit
- Below 15 for 2+ consecutive weeks → flag for review
- Free text responses flagged for Matt's attention

---

## Open Questions

- [ ] Does Everfit support custom check-in surveys, or do you need to use a third-party form?
- [ ] Should the full diagnostic be a Google Form, a PDF, or built into Everfit?
- [ ] How many response options per question? (3-point, 5-point, or open-ended?)
- [ ] Should the scoring be automated (spreadsheet/script) or manual (Matt reviews)?
