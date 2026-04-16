# 🏋️ My 3-Month Transformation — Fitness Plan App

A shareable, mobile-first single-page fitness tracker for a 14-week gym + abs transformation program. Built with vanilla JavaScript and Tailwind CSS. No backend, no login — all progress saved locally in the browser.

**🌐 Live App:** [https://anshul-cc.github.io/fitness-plan/](https://anshul-cc.github.io/fitness-plan/)

---

## 🚀 User Flow

### First-time visitor
1. Lands on a **full-screen dark landing page** — program summary, stat pills, what's included
2. Clicks **"Start My Transformation →"** — today's date is saved as their personal Day 1
3. Goes straight into **Week 1, Day 1** of the program

### Returning visitor
- App reads the saved start date from localStorage
- Automatically computes the current week (1–14) and day relative to that start date
- Opens directly on **today's workout** — no taps needed

### After Week 14
- Shows a **completion / celebration screen** with a journey summary
- **"Start a New Cycle →"** resets the start date to today; previous progress data is preserved

> The program dates are fully dynamic — anyone can open the link and start their own independent 14-week journey from any date.

---

## 📋 Program Overview

| Detail | Value |
|---|---|
| **Duration** | 14 weeks from your personal start date |
| **Training days** | 6 days/week (Mon–Sat relative to start) |
| **Rest day** | Day 7 of each week |
| **Sets per exercise** | 4 sets |
| **Rest between sets** | 60 seconds |
| **Core finisher** | Every training day (~35–38 min) |

---

## 🗓️ Weekly Split

| Day | Focus |
|---|---|
| **Monday** | 💪 Chest Day A — Flat & Mass (DB Bench, Incline DB, Flyes, Push-ups) |
| **Tuesday** | 🏋️ Back Day — Pull & Row (Lat Pulldown, Rows, Face Pulls + Pull-up Progression) |
| **Wednesday** | 🦵 Leg Day — Squats, Deadlifts, Lunges, Calves |
| **Thursday** | 💪 Chest Day B — Incline & Isolation (Incline DB Press leads every week) |
| **Friday** | 🔱 Shoulder Day — Press, Laterals, Rear Delts |
| **Saturday** | 💥 Arms Day — Biceps + Triceps + Pull-up Bonus |

---

## 🔄 4-Week Rotating Workout Plan

Exercises rotate every 4 weeks to prevent adaptation and maintain progressive overload:

- **Week 1** — Foundation compound movements
- **Week 2** — Machine variations + volume
- **Week 3** — Incline emphasis + supersets
- **Week 4** — Peak intensity + heaviest loads

The 4-week cycle repeats across all 14 weeks (`weekIndex % 4`).

---

## 🔥 Core Finisher — Abs & Fat Burn

The core program is split into two phases:

### Phase 1 — Weeks 1–3 (Mar 30 – Apr 19)
Original core finisher: 5 exercises/day focused on general core activation — Planks, Dead Bug, Russian Twists, Side Plank, Bicycle Crunches, Flutter Kicks, V-Ups, Mountain Climbers, Hollow Hold.

### Phase 2 — Weeks 4–14 (Apr 20 onwards) — New Abs Cycle
Dedicated obliques & love-handle obliteration program — 5 exercises/day (6 on Saturdays), 4 sets, 60s rest. Exercises sourced from a curated database specifically for visible abs.

| Abs Cycle Week | Focus | Main Program Weeks |
|---|---|---|
| **W1 Foundation** | Learn movement patterns, mind-muscle | W4, W8, W12 |
| **W2 Build** | Add weight, increase volume | W5, W9, W13 |
| **W3 Intensity** | Heavier, shorter rest | W6, W10, W14 |
| **W4 Peak** | Maximum load, full oblique burn | W7, W11 |

**Every day includes:** Russian Twists + Side Crunch With Leg Lift (oblique focus mandatory)

**Saturday bonus:** Incline Treadmill Walk (20 min, 10–12% incline) — best steady-state fat burn for love handles.

### Core Exercise Library (Phase 2)
Upper Abs · Lower Abs · Obliques & Love Handles · Stability

| Category | Exercises |
|---|---|
| Upper Abs | Twisting Crunch, Decline Bench Abdominal Reach, Jackknife On Bench, Seated Cable Crunch |
| Lower Abs | Abdominal Hip Thrust, Alternating Lying Leg Raise, Lying Leg Raise With Hip Thrust, Decline Bench Leg Raise, Decline Bench Alternating Knee Raise |
| Obliques | Side Crunch With Leg Lift, Russian Twists, Decline Weighted Twist, Half Kneeling Pallof Press, Twisting Cable Crunch, Decline Bench Sit Up With Twist |
| Stability | Bird Dog, Hollow Hold, Reach And Catch, Stir the Pot on Exercise Ball |
| Cardio | Incline Treadmill Walk (Saturdays) |

---

## 📱 App Features

- **Landing page** — beautiful dark onboarding screen with program stats and a single CTA to begin
- **Dynamic start date** — each user's Week 1 Day 1 begins the day they click Start; stored in localStorage
- **Auto week + day detection** — always opens on the correct week and day relative to each user's personal start
- **Completion screen** — celebrates finishing 14 weeks with a summary and option to restart a new cycle
- **Exercise GIF demos** — animated GIF for every exercise with multi-GIF carousel support
- **Progress tracking** — check off sets as you complete them; saved to localStorage by date (preserved across restarts)
- **Calorie estimates** — per-exercise kcal burn + total daily kcal shown in workout header
- **Core tab** — browse full core exercise library, filtered by difficulty (Easy / Moderate / Challenging)
- **Meal plan tab** — daily breakfast, lunch, dinner and snack suggestions with calorie counts
- **Pull-up progression** — structured Dead Hang → Scapular Pull-up → Inverted Row → Negative Pull-up program on Tuesdays
- **Optional exercises** — marked with **(O)** for exercises recommended to skip if fatigued (e.g. Bench Dips, DB Front Raises)
- **PWA-ready** — add to home screen on iPhone/Android for a native app feel
- **Shareable** — anyone can open the URL and start their own independent 14-week journey

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vanilla JavaScript (no framework) |
| Styling | Tailwind CSS (CDN) |
| Storage | Browser localStorage |
| Hosting | GitHub Pages |
| Build | None — single HTML file |

---

## 📁 File Structure

```
fitness-plan/
├── index.html               # Main app (also served as root for GitHub Pages)
└── new-my-fitness-plan.html # Source file
```

---

## 🚀 Running Locally

No build step required. Just open the file:

```bash
# Option 1 — open directly
open index.html

# Option 2 — serve locally (recommended for full PWA behaviour)
npx serve -p 3456 .
# then visit http://localhost:3456
```

---

## 📅 Program Structure

Dates are fully dynamic — they shift based on each user's personal start date. The week number and cycle always follow this pattern:

| Week | Gym Cycle | Abs Core Cycle |
|---|---|---|
| W1 | Gym W1 — Foundation | Legacy Phase (Weeks 1–3) |
| W2 | Gym W2 — Machine Variations | Legacy Phase |
| W3 | Gym W3 — Incline Emphasis | Legacy Phase |
| W4 | Gym W4 — Peak Intensity | **Abs W1 — Foundation** |
| W5 | Gym W1 | Abs W2 — Build |
| W6 | Gym W2 | Abs W3 — Intensity |
| W7 | Gym W3 | Abs W4 — Peak |
| W8 | Gym W4 | Abs W1 — Foundation |
| W9 | Gym W1 | Abs W2 — Build |
| W10 | Gym W2 | Abs W3 — Intensity |
| W11 | Gym W3 | Abs W4 — Peak |
| W12 | Gym W4 | Abs W1 — Foundation |
| W13 | Gym W1 | Abs W2 — Build |
| W14 | Gym W2 | Abs W3 — Intensity |

> For the original author (start date Mar 30, 2026), W4 begins Apr 20 and W14 ends Jul 5, 2026.
