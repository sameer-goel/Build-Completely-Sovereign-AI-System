# Level 0  -  Landing & Reverse Engineering Story

> The entry point. No code, no setup. Just the story of what we found and what we built.

## Page

| File | Owner | Status |
|------|-------|--------|
| `a0_landing_Q.html` | Q | ✅ Built |

## What This Page Teaches

One concept per slide. Brilliant-style: visual first, text is support.

| Slide | Title | Concept | Interaction |
|-------|-------|---------|-------------|
| 1 | Hero | "Build Your Own AI 100% Sovereign" | Click "Let's go →" |
| 2 | The Question | "What if you could look inside Claude Code?" | Read (sets up curiosity) |
| 3 | What We Found | 9 pieces extracted from the codebase | Tap each crate to reveal (gamified counter) |
| 4 | What We Plugged In | Ollama + qwen2.5:7b + 80 lines of Python | Cards animate in on "Plug it in" button |
| 5 | The Formula | Chassis + Engine = Local Clawd | Animated equation, pieces fade in sequentially |
| 6 | CTA | "Ready to build yours?" | Button → Act 1 |

## The 9 Crates (Slide 3  -  What We Found)

These are the pieces we extracted from the Claw Code repo:

| # | Name | One-liner | Source in repo |
|---|------|-----------|----------------|
| 1 | The Loop | Ask → tool call → result → repeat | `src/query_engine.py`, `rust/crates/runtime/` |
| 2 | Tool Registry | 184 tools the AI can call | `src/tools.py`, `rust/crates/tools/` |
| 3 | Permissions | Controls which tools are allowed | `src/permissions.py` |
| 4 | Sessions | Save & resume conversations | `src/session_store.py` |
| 5 | System Prompt | Hidden instructions for the AI | `src/setup.py`, `rust/crates/runtime/src/prompt.rs` |
| 6 | Transcripts | Full log of everything that happened | `src/transcript.py` |
| 7 | Compaction | Summarize old turns to save memory | `src/transcript.py` |
| 8 | Cost Tracking | Count every token used | `src/cost_tracker.py` |
| 9 | Streaming | Show words as they arrive | `rust/crates/api/` |

## The 3 Plugs (Slide 4  -  What We Plugged In)

| # | Name | What it replaces |
|---|------|-----------------|
| 1 | Ollama | Anthropic's cloud API → localhost:11434 |
| 2 | qwen2.5:7b | Claude 3.5/4 → local 7B model |
| 3 | 80 lines of Python | 4 real tools: read_file, write_file, bash, grep_search |

## Design Decisions

- **No sidebar, no footer nav**  -  this is a landing page, not a lesson. Full-screen slides.
- **Progress dots** at top  -  Brilliant-style, turn green as you scroll past.
- **Gamified discovery**  -  slide 3 requires tapping each crate. Counter rewards completion.
- **Auto-animations on scroll**  -  slides 4 and 5 trigger when scrolled into view.
- **One CTA**  -  "Start Act 1 →" links to `../level-1-beginner/a1_high_level_diagram.html`

## Branding

- Site name: **Sovereign Intelligence System**
- Tagline: **Build Your Own AI 100% Sovereign**
- No emoji in header/hero
- Dark theme: `#0d1117` background

## Next Steps

- [ ] Add keyboard navigation (← → arrow keys between slides)
- [ ] Add completion state (localStorage: "act0_complete")
- [ ] Mobile responsive pass
- [ ] Connect to modular shell when ready

---

*Owner: Q*
*Last updated: Session 1*
