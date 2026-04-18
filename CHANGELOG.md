# Changelog

All notable changes to the Fitness Plan App are documented here.

---

## [v2.0] — April 18, 2026

### 🚀 Landing Page & Onboarding
- Added a full-screen dark landing page shown to first-time visitors
- Displays program summary: 14 weeks · 84 sessions · 6 days/week · 5 muscle groups
- "What's included" checklist: muscle groups, core finisher, progressive cycles, meal plan, progress tracking
- Single **"Start My Transformation →"** CTA button with orange glow effect and press animation
- Subtitle confirms today becomes Day 1 the moment user clicks Start

### 👤 Dynamic Per-User Start Date
- `PROGRAM_START` is no longer hardcoded — it is read from `localStorage` (`programStartDate` key)
- When a user clicks Start, today's date is saved as their personal program start
- All week numbers, workout dates, week date ranges, and day-of-week labels now calculate dynamically relative to each user's start date
- App is fully shareable — anyone can open the URL and begin their own independent 14-week journey

### 🔄 Smart Returning User Flow
- On every subsequent visit, app reads saved start date and auto-navigates to the correct week and day
- No extra taps — opens directly on today's workout
- `getTodayProgramDay()` computes which day of the 7-day week the user is on (Day 1 = start date, Day 7 = rest day), independent of calendar day names

### 🏆 Program Completion Screen
- After all 14 weeks are complete, shows a celebration screen instead of the app
- Displays trophy icon, "You Did It. 14 Weeks Done." headline, and completion stats
- Lists what was built: chest/back/legs/shoulders/arms, obliques & core, progressive overload
- **"Start a New Cycle →"** resets the start date to today; all previous progress data is preserved in localStorage

### 💾 Progress Data Preservation
- Existing progress (sets checked off, keyed by calendar date) is preserved across program restarts and new cycles
- No data is wiped when starting a new cycle

---

## [v1.2] — April 17, 2026

### 🖼️ GIF Updates
- Updated 5 exercise GIFs in `CORE_LIB` with corrected URLs provided:
  - **Side Crunch With Leg Lift** → pinimg (2891c5…)
  - **Alternating Lying Leg Raise** → fitnessprogramer Alternate-Leg-Raises
  - **Jackknife On Bench** → jefit 343
  - **Seated Cable Crunch** → pinimg (c67133…)
  - **Twisting Cable Crunch** → jefit 789
- Fixed **Hollow Hold** GIF reverted from broken `.png` back to original pinimg URL

### 🧹 CORE_LIB Rebuild
- Removed 13 old exercises no longer in the program (Plank, Dead Bug, Bicycle Crunches, Flutter Kicks, etc.)
- Added 16 new exercises with curated GIF URLs from fitnessprogramer, jefit, and pinimg
- Kept 5 existing entries: Bird Dog, Heel Touches, Russian Twists, Hollow Hold, Incline Treadmill Walk
- Total: 21 entries across Upper Abs · Lower Abs · Obliques · Stability · Cardio categories

---

## [v1.1] — April 15–16, 2026

### 🔥 New Abs & Obliques Core Program (Phase 2)
- Replaced generic core finisher with a dedicated obliques + love-handle program starting W4 (Apr 20)
- **Phase 1 (W1–W3):** Original core finisher preserved exactly — Planks, Dead Bug, Side Plank, Russian Twists, etc.
- **Phase 2 (W4–W14):** New 4-week abs cycle with 5 exercises/day (6 on Saturdays), 4 sets, 60s rest
- Roman Chair replaced with Decline Bench Sit Up With Twist (Roman Chair not available at gym)
- Incline Treadmill Walk kept as 6th item every Saturday (20 min, 10–12% incline)

| Abs Cycle | Focus | Applies To |
|---|---|---|
| W1 Foundation | Movement patterns, mind-muscle | W4, W8, W12 |
| W2 Build | Add weight, increase volume | W5, W9, W13 |
| W3 Intensity | Heavier loads, shorter rest | W6, W10, W14 |
| W4 Peak | Maximum load, full oblique burn | W7, W11 |

### 🔁 Routing Fix — getCoreFinisher()
- Replaced single `CORE_FINISHER[weekIdx % 4]` lookup with two separate arrays + a routing function
- `CORE_FINISHER_LEGACY[weekIdx]` used for weeks 1–3 (original exercises intact)
- `CORE_FINISHER_ABS[(weekIdx-3) % 4]` used for weeks 4–14 (new abs program)
- Fixes regression where new exercises were incorrectly shown in weeks 1–3

### 🔢 Sets Updated to 4
- All exercises across EX_LIB, CORE_LIB, PULLUP_PROG, and BONUS_PULLUP updated from `3 ×` to `4 ×`
- Reflects current Week 4 training volume

### 🌐 GitHub & GitHub Pages
- Repository created: [github.com/anshul-cc/fitness-plan](https://github.com/anshul-cc/fitness-plan)
- Live app deployed via GitHub Pages: [anshul-cc.github.io/fitness-plan](https://anshul-cc.github.io/fitness-plan/)
- `index.html` added as GitHub Pages root entry point

### 📄 README Created
- Full documentation added covering program overview, weekly split, core phases, exercise library, app features, tech stack, and program timeline

---

## [v1.0] — April 13–14, 2026

### 💪 Thursday Chest Day B Added
- Added a second chest day (Thursday) to all 4 workout week templates
- Monday renamed to **Chest Day A** (flat/mass focus: DB Bench, Push-ups, Flyes)
- Thursday becomes **Chest Day B** (incline/isolation focus: Incline DB Press always leads)
- Incline DB Press is the first exercise every Thursday across all 4 week variants

| Week | Thursday Chest Day B Exercises |
|---|---|
| W1 | Incline DB Press, Cable Chest Flyes, Pec Deck / Butterfly, DB Chest Flyes |
| W2 | Incline DB Press, Machine Chest Press, DB Chest Flyes, Push-ups |
| W3 | Incline DB Press, Bench Dips (Chest focus), Cable Chest Flyes, Pec Deck / Butterfly |
| W4 | Incline DB Press, Machine Chest Press, DB Chest Flyes, Bench Dips (Chest focus) |

### 🏷️ Optional Exercise Markers
- Exercises suggested for skipping when fatigued marked with **(O)** suffix
- **DB Front Raises (O)** — Friday Weeks 2 & 3 (front delts already taxed by two chest days)
- **Bench Dips (O)** — Saturday all weeks (skip if triceps/shoulders fatigued)

### 🔥 Calorie Burn Added
- `kcal` field added to every exercise entry in EX_LIB, CORE_LIB, WARMUP_HANG, BONUS_PULLUP, PULLUP_PROG
- Per-card display: `· ~X kcal` shown in yellow next to sets/duration
- Daily total kcal computed across all exercise sections (warmup + main + pullup + bonus + core finisher) and shown in workout day header

### 🖼️ Incline Treadmill Walk
- Added to EX_LIB and CORE_LIB with correct GIF URL
- Duration set to 20 min single walk (not 3 × 30 sec)
- Appears as 6th item every Saturday in the core finisher
