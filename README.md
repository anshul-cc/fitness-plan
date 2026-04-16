# 🏋️ My 3-Month Transformation — Fitness Plan App

A personal mobile-first single-page fitness tracker for a 14-week gym + abs transformation program. Built with vanilla JavaScript and Tailwind CSS. No backend, no login — all progress saved locally in the browser.

**🌐 Live App:** [https://anshul-cc.github.io/fitness-plan/](https://anshul-cc.github.io/fitness-plan/)

---

## 📋 Program Overview

| Detail | Value |
|---|---|
| **Duration** | 14 weeks (March 30 – July 6, 2026) |
| **Training days** | 6 days/week (Mon–Sat) |
| **Rest day** | Sunday |
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

- **Auto week detection** — app knows which week of the program you're in based on today's date
- **Exercise GIF demos** — animated GIF for every exercise with multi-GIF carousel support
- **Progress tracking** — check off sets as you complete them; saved to localStorage by date
- **Calorie estimates** — per-exercise kcal burn + total daily kcal shown in workout header
- **Core tab** — browse full core exercise library, filtered by difficulty (Easy / Moderate / Challenging)
- **Meal plan tab** — daily breakfast, lunch, dinner and snack suggestions with calorie counts
- **Pull-up progression** — structured Dead Hang → Scapular Pull-up → Inverted Row → Negative Pull-up program on Tuesdays
- **Optional exercises** — marked with **(O)** for exercises recommended to skip if fatigued (e.g. Bench Dips, DB Front Raises)
- **PWA-ready** — add to home screen on iPhone/Android for a native app feel

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

## 📅 Program Timeline

| Week | Dates | Gym Cycle | Abs Cycle |
|---|---|---|---|
| W1 | Mar 30 – Apr 5 | Gym W1 | Legacy Phase |
| W2 | Apr 6 – Apr 12 | Gym W2 | Legacy Phase |
| W3 | Apr 13 – Apr 19 | Gym W3 | Legacy Phase |
| W4 | Apr 20 – Apr 26 | Gym W4 | Abs W1 Foundation |
| W5 | Apr 27 – May 3 | Gym W1 | Abs W2 Build |
| W6 | May 4 – May 10 | Gym W2 | Abs W3 Intensity |
| W7 | May 11 – May 17 | Gym W3 | Abs W4 Peak |
| W8 | May 18 – May 24 | Gym W4 | Abs W1 Foundation |
| W9 | May 25 – May 31 | Gym W1 | Abs W2 Build |
| W10 | Jun 1 – Jun 7 | Gym W2 | Abs W3 Intensity |
| W11 | Jun 8 – Jun 14 | Gym W3 | Abs W4 Peak |
| W12 | Jun 15 – Jun 21 | Gym W4 | Abs W1 Foundation |
| W13 | Jun 22 – Jun 28 | Gym W1 | Abs W2 Build |
| W14 | Jun 29 – Jul 5 | Gym W2 | Abs W3 Intensity |
