# uiux-skills — UI/UX Skills for AI Coding Agents

> Make AI write code that *feels* right, not just works right.

**English** | [中文](README.zh-CN.md)

uiux-skills is a collection of AI agent skills that bring UI/UX expertise into vibe coding. Instead of checking designs after the fact, these skills teach your AI coding tool to understand your product, your users, and your experience standards — before it writes a single line of frontend code.

## The Problem

You ask an AI to "build a login page" and get code that compiles but:
- Form labels disappear when you start typing
- No loading state when submitting
- Error messages vanish after 3 seconds
- Looks like every other AI-generated page (purple gradient, card grid)

**90% of AI-generated UI has the same UX problems.** Not because the AI can't do better — because nobody tells it what "better" means for *your* product and *your* users.

## How It Works

```
/uiux profile   → Reads your project. Identifies product type and context.
/uiux insight   → Generates user personas and maps critical journeys.
/uiux generate  → Produces a tailored UX-RULES.md for your project.
/uiux review    → Audits code against your rules. Finds violations, gives fixes.
/uiux improve   → Suggests experience improvements and growth directions.
```

After Step 3, a `UX-RULES.md` file lives in your project root. Every AI tool that reads project context (Claude Code, Cursor, Windsurf, etc.) will automatically follow these rules when generating code.

## Quick Start

### Claude Code

```bash
# Add as a skill
claude skill add /path/to/uiux-skills

# Or clone and add
git clone https://github.com/DietCokewithSugar/uiux-skills.git
claude skill add ./uiux-skills
```

### Other AI Coding Tools

Copy the `SKILL.md` file and `frameworks/`, `patterns/`, `anti-patterns/` directories into your AI tool's skill/rules directory. The SKILL.md format is compatible with Cursor, Codex, OpenClaw, and any tool supporting the universal skill format.

### Manual (any project)

Just run Steps 1–3 to generate a `UX-RULES.md`, then drop it into your project root. Any AI tool that reads project files will pick up the rules.

## What's Inside

```
uiux-skills/
├── SKILL.md                  # Core skill — the full uiux workflow
├── frameworks/               # UX evaluation frameworks
│   ├── ets.md                # Experience Trust Score (enterprise/B2B)
│   ├── heart.md              # Google HEART (consumer/growth)
│   ├── sus-lite.md           # System Usability Scale (MVPs/quick check)
│   └── ueq-lite.md           # User Experience Questionnaire (content/creative)
├── patterns/                 # UX best practices
│   └── common.md             # Forms, navigation, loading, errors, onboarding
├── anti-patterns/            # Common UX mistakes AI tools make
│   └── common.md             # Purple gradients, card walls, placeholder labels...
└── examples/                 # Usage examples
    └── usage.md
```

## Evaluation Frameworks

uiux-skills auto-selects the best framework based on your product type:

| Product Type | Framework | Focus |
|---|---|---|
| SaaS / Enterprise | ETS | Trust, efficiency, error prevention |
| Consumer / E-commerce | HEART | Happiness, engagement, retention |
| MVP / Prototype | SUS-Lite | Quick usability baseline |
| Content / Creative | UEQ-Lite | Attractiveness, stimulation |

You can also specify a framework manually or use multiple frameworks together.

## Contributing

We welcome contributions! Here's what would help most:

- **Industry-specific rule sets** — UX rules for healthcare, fintech, education, etc.
- **New patterns and anti-patterns** — especially AI-specific ones you've encountered
- **Framework additions** — new evaluation frameworks or refinements to existing ones
- **Translations** — make uiux-skills accessible to non-English-speaking developers
- **Real-world examples** — before/after cases showing impact

See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## Related

- [uiux Web Tool](https://ues-agent.vercel.app) — Upload screenshots or screen recordings for deep AI-powered UX evaluation (for designers and non-technical users)
- [Agent Skills Spec](https://agentskills.io) — Universal skill format standard
- [uiux-skills on GitHub](https://github.com/DietCokewithSugar/uiux-skills)

## License

MIT
