# ACTS for AI Agents

> **4 system prompts that make your AI agent stop ignoring the EU AI Act.**
> Built by [Sprinkling Act](https://sprinklingact.com), the people who map AI agents to regulatory positions for a living.

---

## The problem

In 2026, your AI agent probably does at least one of these:

- Watches your screen and listens to your conversations (Omi for Desktop)
- Reads your inbox and acts on it without asking each time (Google Cowork Agent)
- Chains 3 to 5 LLMs to produce a single decision (Cursor 3.1 multi-agent, Anthropic Routines)
- Was shipped by someone who learned to build agents in 6 months on YouTube

The EU AI Act covers all four cases. None of these products were built with the regulation open on the desk. **Most builders haven't read the regulation. The regulation has read them.**

This repo gives you 4 system prompts you can paste into your agent's instructions today. They don't make you "compliant" — that's a determination only a human assessment can make. They make your agent **stop being silent about the four things the AI Act actually cares about**.

---

## The 4 ACTS

The acronym mirrors the regulation itself: **the 4 ACTS of the AI Act**.

| | Axis | What dissolves | EU AI Act articles |
|---|---|---|---|
| **A** | **Accountability** | Who answers when the agent acts? | Art. 14, Art. 26, Art. 6 + Annex III |
| **C** | **Consent** | Who agreed to be captured? | Art. 5, Art. 50, GDPR |
| **T** | **Traceability** | What can be reconstructed after the fact? | Art. 12, Art. 13, Art. 15 |
| **S** | **Skill** | Does the person shipping understand what they shipped? | Art. 4, Art. 26 |

Each ACT has one system prompt. Pick the ones that match your agent's behavior. Or use all four.

---

## Quick start

```bash
# Clone the repo
git clone https://github.com/sprinkling-act/acts-for-ai-agents.git

# Read the prompts
cd acts-for-ai-agents/system-prompts
ls
# A-accountability.md  C-consent.md  T-traceability.md  S-skill.md

# Paste the relevant blocks into your agent's system prompt:
# - Claude Code → CLAUDE.md
# - Cursor → .cursorrules
# - OpenAI custom GPTs → instructions field
# - Self-hosted agents → system_prompt field
# - Any LLM with system message support
```

---

## The prompts

### [`A-accountability.md`](system-prompts/A-accountability.md) — When the agent acts, who answers?

Forces your agent to surface every consequential action for human confirmation, log it tamper-evidently, and refuse actions affecting third parties without consent.

### [`C-consent.md`](system-prompts/C-consent.md) — Who agreed to be captured?

Forces your agent to present a clear consent surface before any data capture (screen, audio, inbox, files) and refuse to silently expand the capture surface.

### [`T-traceability.md`](system-prompts/T-traceability.md) — What can be reconstructed?

Forces your agent to maintain a structured decision log retrievable on demand, identify every model in the chain, and refuse decisions that cannot be reconstructed.

### [`S-skill.md`](system-prompts/S-skill.md) — Does the deployer understand?

Forces a one-time literacy check before production deployment, requires acknowledgment of EU AI Act categories, and refuses deployment in specialized contexts (medical, legal, financial) without confirmed domain authorization.

---

## What this repo is NOT

- **Not legal advice.** These prompts are engineering scaffolding, not legal opinions.
- **Not a compliance certification.** No badge, no fork, no claim makes your agent EU AI Act-compliant. Only a documented assessment by qualified humans does.
- **Not a registry.** There is no central database, no API, no submission process. This is a static repository of text files.
- **Not a fork-and-claim scheme.** You can fork this repo (MIT license). You cannot fork the regulatory expertise that produces an actual assessment.
- **Not exhaustive.** The EU AI Act has dozens of articles. These four ACTS cover the dimensions most relevant to autonomous agents in 2026. Other articles may apply to your specific case.

---

## Want a real assessment?

If you want to know your agent's actual EU AI Act regulatory position — not a self-declaration, but a structured assessment mapped article by article — Sprinkling Act offers two levels:

- **[Free diagnostic](https://sprinklingact.com/check)** — 9 questions, 60 seconds, instant indicative position. No account. No email. No funnel.
- **[Full Report](https://sprinklingact.com/reports)** — €690, human-reviewed, 15-22 pages, article-by-article analysis with stability indicators and remediation paths.

Both are described in detail at **[sprinklingact.com/ai-agents](https://sprinklingact.com/ai-agents)**.

---

## Display the ACTS-aware badge

If you've integrated these prompts into your agent and want to signal it in your repo, see [`BADGE.md`](BADGE.md). **The badge is a self-declaration of awareness, not a certification.** Wording matters — please read the disclaimer before displaying it.

---

## License

MIT. Fork freely. Adapt freely. Use commercially. The system prompts in this repo are intentionally open. The "ACTS" framework name and structure remain © Sprinkling Act under EU and Belgian copyright — fork the prompts, not the brand.

---

## Built by

**[Sprinkling Act](https://sprinklingact.com)** — Independent EU AI Act position assessment. Brussels, Belgium. BCE BE 1034.962.482.

If you find a bug, an improvement, or a new agent pattern worth covering, open an [issue](https://github.com/sprinkling-act/acts-for-ai-agents/issues).
