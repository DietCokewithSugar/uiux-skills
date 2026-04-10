# SUS-Lite — Lightweight System Usability Scale

## Overview
A simplified version of the classic SUS (System Usability Scale) designed for quick evaluation 
during development. Instead of a post-use survey, this version translates SUS principles into 
concrete development-time checkpoints. Best for MVPs, prototypes, and rapid iteration.

## Dimensions

### 1. Learnability (Weight: 0.30)
Can a new user figure out how to use the product without instructions?
- Checkpoint: Can someone complete the primary task on first visit without help text?
- Rules should focus on: self-explanatory UI, conventional patterns, visible affordances, 
  progressive disclosure, sensible defaults

### 2. Efficiency (Weight: 0.25)
Once learned, can users complete tasks quickly?
- Checkpoint: Does the primary task take fewer than 5 clicks / 30 seconds?
- Rules should focus on: minimal steps, smart defaults, auto-complete, 
  remember user preferences, keyboard shortcuts for power users

### 3. Memorability (Weight: 0.15)
Can returning users re-establish proficiency quickly?
- Checkpoint: Would a user who returns after 2 weeks know what to do?
- Rules should focus on: consistent layout, visible navigation, clear labels,
  persistent state, recent activity indicators

### 4. Error Tolerance (Weight: 0.20)
How well does the system handle user mistakes?
- Checkpoint: What happens if the user does something "wrong"?
- Rules should focus on: forgiving inputs, undo support, clear error messages,
  non-destructive defaults, confirmation for irreversible actions

### 5. Satisfaction (Weight: 0.10)
Is the experience pleasant enough that users don't dread using it?
- Checkpoint: Would a user complain about this to a coworker?
- Rules should focus on: reasonable loading times, no visual jank, 
  professional appearance, respectful tone in messages

## When to Use
- Early-stage products and MVPs
- Hackathon projects
- Internal tools with limited UX budget
- Quick usability gut-check during development
- When you need a "good enough" UX baseline fast

## Scoring
Each checkpoint: Pass (1) / Partial (0.5) / Fail (0). Weighted sum × 100.
- 80–100: Ship it — usability is solid
- 60–79: Ship with caveats — known friction points
- 40–59: Needs work — users will struggle
- Below 40: Don't ship — fundamental usability problems
