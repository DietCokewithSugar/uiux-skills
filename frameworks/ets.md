# ETS — Experience Trust Score

## Overview
ETS measures how much users **trust** a product to help them accomplish their goals reliably. 
Best suited for enterprise tools, internal platforms, and products where trust and efficiency 
matter more than delight.

## Dimensions

### 1. Task Efficiency (Weight: 0.25)
Can users complete their core tasks quickly and without unnecessary steps?
- Measure: Steps to complete key tasks, time on task
- Rules should focus on: streamlined flows, smart defaults, keyboard shortcuts, batch operations

### 2. Error Prevention & Recovery (Weight: 0.25)
Does the system prevent mistakes and help users recover gracefully?
- Measure: Error frequency, recovery success rate, data loss incidents
- Rules should focus on: validation, confirmation dialogs for destructive actions, undo, auto-save

### 3. System Transparency (Weight: 0.20)
Does the user always know what's happening and why?
- Measure: User confusion incidents, support tickets about "what happened?"
- Rules should focus on: loading states, progress indicators, status messages, audit trails

### 4. Consistency & Predictability (Weight: 0.15)
Does the system behave the same way in similar situations?
- Measure: Pattern deviations, learning curve for new features
- Rules should focus on: design system adherence, consistent interaction patterns, predictable navigation

### 5. Perceived Reliability (Weight: 0.15)
Does the system feel solid and professional?
- Measure: Perceived performance, visual polish, uptime perception
- Rules should focus on: fast response times, no layout shifts, professional typography, no broken states

## When to Use
- B2B SaaS products
- Internal enterprise tools
- Admin dashboards and back-office systems
- Products where a mistake has real business cost (finance, operations, logistics)
- Products where users are repeat, daily users (not casual visitors)

## Scoring
Each dimension is scored 0–100. Weighted sum produces the overall ETS score.
- 90–100: Excellent — users trust the product implicitly
- 70–89: Good — trust is established with some friction points
- 50–69: Fair — users work around issues, trust is conditional
- Below 50: Poor — users don't trust the product, seek alternatives
