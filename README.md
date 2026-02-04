# Diet To-Do Tracker

A lightweight, offline-first diet checklist and habit tracker inspired by Todoist.

## Core User Experience
- Daily checklist with meals (breakfast, lunch, snacks, dinner), each item supporting a checkbox, time suggestion, and optional notes.
- Automatic daily reset at 12:00 AM, with yesterday stored in history.
- Streak system that tracks current streak and best streak, breaking on any fully missed day.
- Calendar history view with color-coded adherence (green/partial/missed) and drill-down per date.
- Smart reminders for upcoming meals and missed check-ins.

## Advanced Features
- Weekly/monthly reports with adherence percentage and missed-meal analysis.
- Custom diet plans (weight loss, muscle gain, maintenance), switchable anytime.
- Water intake tracker with daily goal progress.
- Mood/energy tracking to correlate with adherence.
- Offline-first storage with optional future cloud sync.

## Optional Enhancements
- Perfect day badge.
- Meal photo upload.
- AI suggestion prompts based on missed meals.
- Lock screen widget for quick check-ins.

## Data Model (Draft)
- `dietPlans`: multiple plans, each with default daily items and time suggestions.
- `dailyEntries`: daily checklist items, timestamps, notes, and completion state.
- `streaks`: current streak, best streak, and last completed date.
- `waterIntake`: daily count and goal.
- `mood`: energy, sleep, stress per day.

## Daily Reset Logic (Draft)
1. At local midnight, persist the day to history.
2. Evaluate adherence for streak updates.
3. Generate a fresh checklist from the active plan.
4. Clear daily water intake and mood inputs.

## Notifications (Draft)
- Scheduled reminders for meals.
- Late reminders if a meal is not checked by a configured grace period.
- Optional motivational copy variants.
