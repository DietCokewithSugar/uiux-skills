# Contributing to uiux-skills

Thanks for your interest in improving AI-generated user experiences! Here's how to contribute.

## What We Need Most

### 1. Industry-Specific Rule Sets
Create a new file in `patterns/` with UX rules for a specific industry:
- `patterns/healthcare.md` — HIPAA considerations, patient trust, accessibility for elderly
- `patterns/fintech.md` — Security perception, data visualization, error handling for money
- `patterns/education.md` — Learning flow, progress tracking, age-appropriate design
- `patterns/ecommerce.md` — Conversion optimization, trust signals, checkout flow

### 2. Anti-Patterns
Add AI-specific UX anti-patterns you've encountered in `anti-patterns/`:
- What does the AI generate wrong?
- Why does it do this?
- What's the correct pattern?

### 3. Framework Refinements
Improve the evaluation frameworks in `frameworks/` with:
- Better scoring criteria
- More specific rule mapping
- Real-world calibration data

### 4. Examples
Add before/after examples in `examples/` showing how uiux-skills improved a real project.

## How to Submit

1. Fork the repository
2. Create a branch: `git checkout -b add-healthcare-patterns`
3. Make your changes
4. Submit a Pull Request with a clear description of what you added and why

## Style Guidelines

- Write in plain language — our users include developers who aren't UX experts
- Be specific and actionable — "Add a loading spinner" not "improve feedback"
- Include the "why" — explain what user problem each rule solves
- Use examples wherever possible

## Code of Conduct

Be kind. Be constructive. We're all here to make better user experiences.
