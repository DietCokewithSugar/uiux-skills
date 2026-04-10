# Common UX Anti-Patterns

These are patterns that AI coding tools frequently produce. Flag them in reviews.

---

## Layout & Visual

### The Wall of Cards
**Problem:** Everything is a card in a grid. No visual hierarchy. Nothing stands out.
**Why AI does this:** Cards are the "safest" layout pattern in training data.
**Fix:** Establish clear hierarchy — hero section, primary content, secondary content. 
Not everything needs to be a card. Use lists, tables, or featured items to create variety.

### Purple Gradient Syndrome
**Problem:** Generic gradient backgrounds (#667eea → #764ba2) that every AI-generated site uses.
**Fix:** Use solid colors, subtle textures, or brand-specific palettes. If a gradient is used, 
it should be intentional and tied to the brand.

### Tiny Text, Huge Headings
**Problem:** H1 at 64px, body text at 12px. Looks "designed" but is unreadable.
**Fix:** Body text minimum 16px on web, 14px on mobile. Heading scale should be proportional 
(1.25–1.5× ratio between levels).

### Missing Visual Hierarchy
**Problem:** All text is the same size/weight. User can't scan the page.
**Fix:** Use size, weight, color, and spacing to create 3–4 distinct levels of hierarchy. 
The user should be able to understand the page structure in 3 seconds.

---

## Interaction

### Placeholder-Only Inputs
**Problem:** Form inputs use only placeholder text as labels. Labels disappear when user types.
**Fix:** Always use a visible `<label>` element above or beside the input. Placeholder text is 
supplementary (example format), not the label.

### Toast-Only Errors
**Problem:** Errors shown only as toast notifications that disappear after 3 seconds.
**Fix:** Inline errors next to the relevant field. Toasts only for global messages. 
Error messages should persist until the issue is resolved.

### Infinite Scroll Everywhere
**Problem:** Long lists with no pagination, no "back to top", no way to find a specific item.
**Fix:** Use pagination for structured data (tables, search results). Infinite scroll only for 
feeds/timelines. Always provide search/filter as an alternative to scrolling.

### Modal Overload
**Problem:** Every action opens a modal. Modals inside modals. Full-page modals that aren't modal.
**Fix:** Use modals only for: confirmation of destructive actions, focused tasks that require 
isolation, content preview. Everything else can be inline, in a drawer, or on a new page.

### Missing Loading States
**Problem:** Button clicked, nothing happens for 2 seconds, then the page changes.
**Fix:** ANY action that takes >300ms needs visual feedback. Button → loading spinner/disabled. 
Page → skeleton screen. API call → progress indicator.

---

## Content & Microcopy

### Robot Speak
**Problem:** "Operation completed successfully." "Invalid input detected." "Resource not found."
**Fix:** Write like a helpful human. "Saved!" / "Please enter a valid email address." / 
"We couldn't find that page — try searching for what you need."

### Mystery Icons
**Problem:** Icon-only buttons with no label or tooltip. User has to guess what they do.
**Fix:** Pair icons with text labels. Icon-only is acceptable only for universally recognized 
symbols (close ×, search 🔍, menu ☰) and must have aria-label.

### Empty Empty States
**Problem:** A blank page when there's no data. No explanation, no CTA, no guidance.
**Fix:** Every empty state should answer: "What is this page for?" and "How do I get started?"

---

## Mobile-Specific

### Desktop UI on Mobile
**Problem:** Horizontal tables, tiny buttons, hover-dependent interactions on touch devices.
**Fix:** Responsive design is not "shrink the desktop layout." Rethink information architecture 
for mobile: stack content vertically, use cards instead of tables, enlarge touch targets.

### Hidden Primary Actions
**Problem:** Key actions buried in hamburger menus on mobile.
**Fix:** Primary action should be the most visible element on screen. Use sticky bottom bar 
or floating action button for the #1 thing users do.

---

## Performance

### Layout Shift
**Problem:** Content jumps around as images/fonts/ads load. Frustrating and disorienting.
**Fix:** Reserve space for images (explicit width/height), use font-display:swap with 
size-adjust, avoid injecting content above the fold after initial render.

### No Offline Handling
**Problem:** App shows white screen or cryptic error when network drops.
**Fix:** Show last cached state with "offline" indicator. Queue actions for retry. 
Graceful degradation is better than total failure.
