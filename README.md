# PROVEN Skincare Plugin

Two agents, five skills, one brand system. Install once, everyone gets it.

## Architecture

```
Plugin (proven)
├── Agents
│   ├── Campaign Producer — marketing assets, no-stop pipeline
│   └── Product Designer — UI/UX work, gated checkpoints
├── Skills (shared knowledge both agents draw from)
│   ├── proven-voice — brand tone of voice
│   ├── proven-email — Klaviyo strategy & structure
│   ├── proven-creative — photography prompt system
│   ├── proven-ui — design system & frontend
│   └── proven-brand-qa — brand scoring critic
├── Agent References
│   ├── skill-loading-map.md — what to load per channel
│   ├── channel-specs.md — platform formats & limits
│   └── error-recovery.md — failure handling
└── Connectors
    ├── Klaviyo — email campaigns & flows
    └── Gemini (nanobanana) — image generation
```

## Two Agents

### Campaign Producer
Takes a marketing brief and delivers finished assets without stopping for approval.

**Handles:** email, social media, paid ads (Google/Meta), campaign landing pages, product launch assets, seasonal promos.

**Process:** story & copy → image direction → image generation → assembly → brand QA. Runs straight through. Human reviews once at the end.

**Skills used:** proven-voice, proven-email, proven-creative, proven-ui, proven-brand-qa.

### Product Designer
Takes a UI/UX request and builds it with approval checkpoints.

**Handles:** product UI, feature design, components, page layouts, wireframes, design system work.

**Process:** section architecture (approve) → copy (approve) → build → brand QA. Gates exist because UI changes are harder to undo.

**Skills used:** proven-ui, proven-brand-qa. Adds proven-voice and proven-creative only when needed.

### Routing
Your team doesn't pick an agent. They describe what they need:
- "Mother's Day email campaign" → Campaign Producer
- "Redesign the quiz results card" → Product Designer
- "Landing page for the SPF sale" → Campaign Producer (it has a narrative)
- "Redesign the landing page template" → Product Designer (it's a design system asset)

## Setup (Enterprise)

1. Push to a **private** GitHub repo.
2. Organization Settings → Plugins → add repo as marketplace source.
3. Set to **Auto-install** for the whole org.
4. Ensure **Cowork** and **Skills** are enabled.
5. Each person sets `GOOGLE_AI_API_KEY` for Gemini image generation.

## Testing

See `eval/test-briefs.md` for 5 test briefs with scoring rubrics, ordered by difficulty. Run Test 1 first. If it works end-to-end, proceed.

## Updating

Push to GitHub, click "Update" in org settings. Plugin name `proven` is the unique ID — new versions overwrite automatically.
