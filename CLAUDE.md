# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A personal exercise/fitness tracking static website (Thai language content). It has two distinct layers:

1. **Landing page** (`index.html`) — TemplateMo "Chain App Dev" Bootstrap template, currently with placeholder content.
2. **Workout viewer app** (`datasources/workout_program.html`) — A standalone Thai-language workout program viewer that renders the fitness content.

No build system, no package manager, no server. Open HTML files directly in a browser.

## Repository Structure

```
index.html                  # Main landing page (Bootstrap template)
assets/                     # CSS, JS, images, fonts for index.html
vendor/                     # Bootstrap + jQuery (local copies)
datasources/                # Source-of-truth content (all in Thai)
  workout_program.html      # Workout viewer app
  program.md                # Full 4-day Upper/Lower home program
  program-gym.md            # Gym variant of the program
  overview.md               # Weekly schedule + nutrition + tracking tables
  consultation.md           # User profile and physical constraints
  upper_body.md             # Upper body muscle reference data
  lower_body.md             # Lower body muscle reference data
  monday.md / tuesday.md / thursday.md / friday.md   # Daily workout detail (home)
  Home/                     # Home workout per-day files (alternate structure)
  Gym/                      # Gym workout per-day files (00–05 numbered)
```

## Content Architecture

The workout content is written in Thai and covers a **4-day Upper/Lower Split** for a male beginner (29 yo, home gym with dumbbells only, physical constraints on left ankle and left elbow):

- **Upper A (Monday)** — Push emphasis: Floor press, Bent-over row, Arnold press, Reverse fly, Hammer curl, Tricep kickback
- **Lower A (Tuesday)** — Quad emphasis: Goblet squat (heel elevated), RDL, Glute bridge, Sumo squat, Calf raise, Dead bug
- **Upper B (Thursday)** — Pull emphasis: Single-arm row, Floor press neutral, Lateral raise, Floor fly, Supinated curl, Wrist curls
- **Lower B (Friday)** — Hip emphasis: Sumo deadlift, Goblet squat, Hip thrust, Stiff-leg DL, Seated calf raise, Plank

Key constraints to maintain in all content edits:
- **No single-leg exercises** (left ankle: post-surgery, torn ligament)
- **No push-ups or overhead tricep extensions** (left elbow injury)
- **No bench** — use floor press, floor fly, sitting on floor
- All squat variants require **heel elevation ~2-3cm** for the left ankle

## Key Files to Know

- `datasources/program.md` — The comprehensive program with exercise selection rationale, volume summary, and 12-week progressive overload plan
- `datasources/overview.md` — Simplified version with weekly schedule and progress tracking tables
- `datasources/consultation.md` — Original user profile data
- `datasources/workout_program.html` — The viewer app (self-contained HTML/CSS/JS, renders Markdown-like content)
