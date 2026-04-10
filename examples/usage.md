# uiux-skills — Usage Examples

## Example 1: New Project Setup

**You:** I'm starting a new React project — it's an online appointment booking system for a dental clinic.

**What uiux does:**
1. `/uiux profile` → Identifies: Healthcare SaaS, appointment booking, web-responsive
2. `/uiux insight` → Generates personas (anxious patient, busy receptionist, clinic admin), maps booking journey
3. `/uiux generate` → Selects ETS framework (trust matters in healthcare) + custom safety rules, writes `UX-RULES.md`

**Result:** Before a single component is built, the project has a `UX-RULES.md` that ensures:
- Appointment confirmation shows clear date/time/provider
- Cancellation requires explicit confirmation but is easy to find
- Patient data forms are forgiving (multiple phone formats accepted)
- Loading states during booking prevent double-submissions
- Accessibility is WCAG AA compliant (healthcare requirement)

---

## Example 2: Review Existing Component

**You:** `/uiux review` [pastes a login form component]

**uiux finds:**
```
🔴 CRITICAL — Placeholder-only labels
   Inputs use placeholder as label. Disappears when typing.
   Fix: Add <label> element above each input.

🔴 CRITICAL — No error messages
   Failed login shows only a red border. No text explanation.  
   Fix: Add inline error: "Email or password is incorrect. Please try again."

🟡 WARNING — No loading state on submit
   Button stays static during API call.
   Fix: Add disabled state + spinner during submission.

🔵 INFO — Password field lacks visibility toggle
   Users can't check what they typed.
   Fix: Add show/hide password toggle icon.

UX Review Score: 4/10
Top priority: Add visible labels to all form inputs
```

---

## Example 3: Improve Existing Product

**You:** I have an e-commerce site. `/uiux improve` — I want to reduce cart abandonment.

**uiux produces:**
```
## Quick Wins 🎯
- Add progress indicator to checkout (Step 1/3, 2/3, 3/3)
- Show order summary sticky on the right during checkout
- Auto-save cart contents for returning visitors

## Experience Differentiators ✨
- Guest checkout with optional account creation AFTER purchase
- "Save for later" on cart items instead of just delete
- Trust signals near payment (security badges, return policy)

## Growth-Oriented UX 📈
- Exit-intent: Show saved cart reminder
- Smart address auto-complete to reduce form friction
- One-click reorder for returning customers

## Strategic Direction 🧭
1. Simplify checkout to 2 steps max (address → payment+confirm)
2. Add real-time shipping estimates on product pages
3. Implement wishlist for long-term engagement
```

---

## Example 4: Existing Project Without UX-RULES.md

**You:** Can you check the UX of my project? [project already has code but no UX-RULES.md]

**What uiux does:**
1. Reads existing code (README, package.json, components) → auto-runs Step 1 (Profile)
2. Infers users from the product type → auto-runs Step 2 (Insight)  
3. Generates `UX-RULES.md` → Step 3
4. Reviews the existing code against the new rules → Step 4
5. Suggests improvements → Step 5

All in one flow, automatically.
