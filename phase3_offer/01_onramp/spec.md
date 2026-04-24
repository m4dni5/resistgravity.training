# On-Ramp Program Spec

## Purpose

Define the standalone Everfit on-ramp program that takes a non-lifter from zero to a sustainable RT habit.

---

## Product Architecture

| Product | Format | Delivery |
|---------|--------|----------|
| **On-Ramp Program** | Standalone Everfit program | Self-directed, app-based |
| **Follow-Up Programs** (1-3) | Standalone Everfit programs | Self-directed, app-based |
| **Monthly Online** | Custom programming + monthly call | For those needing customization |
| **Consultation** | One-time, hourly rate | In-person or remote |

### On-Ramp → Follow-Up Path

1. Client purchases on-ramp program on Everfit
2. Completes 8-week on-ramp independently (or with optional consultation)
3. Graduates to one of 1-3 follow-up programs based on goals/progress
4. If customization needed → joins monthly online offering

---

## Program Design Parameters

Based on Phase 1 and Phase 2 evidence:

### Frequency
- **Target:** 2-3 sessions per week
- **Evidence:** 1-2 sessions/week produces meaningful health gains; 2-3 is optimal (Radaelli 2025, Shailendra 2022)
- **Recommendation:** Start at 2x/week for weeks 1-4, progress to 3x/week in weeks 5-8

### Session Duration
- **Target:** 30-45 minutes
- **Evidence:** Time is the #1 barrier; shorter sessions improve adherence (Phase 2, 03_time_efficiency.md)

### Exercise Selection
- **Target:** 4-5 compound movements per session
- **Evidence:** Multi-joint exercises are more time-efficient; free weights and machines are equivalent for health (Phase 1, 04_exercise_selection.md)
- **Movement patterns:** Squat, hinge, push, pull, carry

### Intensity
- **Target:** 60-80% 1RM (RPE 6-8)
- **Evidence:** Effective for health outcomes; lower intensities also work for untrained individuals (Borde 2015, Rhea 2003)

### Progression
- **Model:** Add reps within a range (e.g., 8-12), then increase load when top of range is achieved
- **Evidence:** Progressive overload via reps OR load is effective (Plotkin 2022)
- **Simplicity:** No periodization, no wave loading, no complex programming in weeks 1-8

### Volume
- **Target:** 2-3 sets per movement pattern per session
- **Evidence:** 1-2 sets/week per muscle group produces meaningful gains; 2-3 sets/session is better (Krieger 2010)

---

## Program Structure (8 Weeks)

### Weeks 1-2: Learn
- Focus: Movement quality, exercise familiarity
- 2 sessions/week
- 4 exercises per session (squat pattern, hinge pattern, push, pull)
- Light loads, higher reps (10-15) to build motor patterns
- Goal: Client can perform each movement safely and consistently

### Weeks 3-4: Build
- Focus: Introduce progressive loading
- 2 sessions/week
- Add 5th exercise (loaded carry or single-leg variation)
- Moderate loads, moderate reps (8-12)
- Begin tracking loads and reps
- Goal: Client is progressing week to week

### Weeks 5-6: Strengthen
- Focus: Progressive overload
- 2-3 sessions/week
- Same 5 exercises, increasing load
- Reps in 6-10 range for main lifts
- Goal: Measurably stronger than week 1

### Weeks 7-8: Consolidate
- Focus: Habit formation and independence
- 2-3 sessions/week
- Client should be able to run the session with minimal coaching
- Introduce concepts: when to increase load, how to know if a set was effective
- Goal: Client can train independently

---

## Session Format Template

1. **Warm-up** (3-5 min): Light movement, dynamic stretching
2. **Main work** (25-35 min): 4-5 exercises, 2-3 sets each
3. **Finish** (2-3 min): Brief cool-down, log loads/reps

---

## Everfit Implementation Notes

- Each week is a distinct program block in Everfit
- Video demonstrations for each exercise (Matt's own or curated)
- Built-in progression cues ("if you hit 12 reps, increase weight by X next session")
- Weekly self-survey (short diagnostic version) embedded as check-in
- Optional consultation available at hourly rate for form review or troubleshooting

---

## Follow-Up Programs (1-3 Options)

After completing the on-ramp, clients graduate to a follow-up. Options to design:

1. **Continued Health Focus:** Same template, progressive overload, 3x/week
2. **Strength Focus:** Heavier loads, lower reps, compound lifts
3. **Sport/Activity Integration:** RT programmed around skiing/hiking/paddling schedule

Each is a standalone Everfit program. Clients who need customization join the monthly online offering.

---

## Open Questions

- [ ] What exercises are available in Everfit's exercise library? Do you need to create custom demos?
- [ ] How many follow-up programs to design initially (1, 2, or 3)?
- [ ] Pricing for on-ramp vs. follow-up vs. monthly?
- [ ] Should the weekly self-survey be part of this spec, or developed separately with the diagnostic?
