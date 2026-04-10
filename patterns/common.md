# Common UX Patterns

Reference for AI coding agents: apply these patterns when generating UI code.

---

## Forms

### Progressive Disclosure
Don't show all form fields at once. Reveal fields as they become relevant.
- Example: Show shipping address fields only after user selects "ship to different address"
- When: Forms with > 6 fields, or with conditional logic

### Inline Validation
Validate as the user types or on field blur, not only on submit.
- Show success state (green check) for valid fields
- Show error immediately below the field, not in a toast
- Don't validate while the user is still typing (wait for blur)

### Smart Defaults
Pre-fill fields with the most likely value.
- Country → user's locale country
- Currency → locale currency
- Date format → locale date format
- Phone format → locale phone format

---

## Navigation

### Clear Wayfinding
Users should always know: where am I? Where can I go? How do I go back?
- Active state on current navigation item
- Breadcrumbs for depth > 2 levels
- Back button / escape route always visible

### Mobile Navigation
- Bottom navigation for 3–5 primary destinations
- Hamburger menu only for secondary items
- Avoid nested dropdowns on mobile — they're unusable on touch

---

## Feedback & Loading

### Skeleton Screens
Use skeleton loading (gray placeholder shapes) instead of spinners for content areas.
- Spinners only for actions (button clicks, form submissions)
- Skeleton for content that has a known layout

### Optimistic Updates
For low-risk actions, update the UI immediately and sync in background.
- Toggle switches, likes, bookmarks → update instantly
- Payments, deletions → wait for confirmation

### Empty States
Never show a blank page. Empty states should:
- Explain what will appear here
- Provide a clear action to get started
- Optionally show an illustration or helpful tip

---

## Error Handling

### Error Message Format
Every error should answer: What happened? Why? What can the user do?
- Bad: "Error 500"
- Good: "We couldn't save your changes. Please try again, or contact support if this continues."

### Destructive Action Protection
Before irreversible actions, require explicit confirmation:
- Delete → "Are you sure? This will permanently delete [item name]. This can't be undone."
- Use danger-colored (red) button for destructive action
- Make the safe option (cancel) visually prominent

---

## Onboarding

### First-Run Experience
The first 30 seconds determine if a user stays or leaves.
- Show value immediately — don't gate behind long sign-up
- Use progressive onboarding (teach features as user encounters them)
- Provide a quick-start guide for complex products

### Empty State Onboarding
When a user has no data yet:
- Show example data or templates
- Provide a single, clear "Create your first [item]" CTA
- Brief explanation of what this section is for

---

## Accessibility Baseline

### Touch Targets
- Minimum 44×44px for all interactive elements (Apple HIG)
- 48×48dp recommended (Material Design)
- Adequate spacing between targets (at least 8px)

### Color Contrast
- Normal text: 4.5:1 minimum contrast ratio (WCAG AA)
- Large text (18px+): 3:1 minimum
- Interactive elements: 3:1 against background
- Never use color alone to convey information

### Keyboard Navigation
- All interactive elements focusable via Tab
- Visible focus indicator (not just browser default — make it obvious)
- Escape closes modals and popups
- Enter activates buttons and links

### Screen Reader Support
- All images have alt text (decorative images: alt="")
- Form inputs have associated labels (not just placeholder)
- ARIA landmarks for page regions
- Dynamic content updates announced with aria-live
