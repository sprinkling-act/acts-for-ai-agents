# ACT A — Accountability

**Source:** github.com/sprinkling-act/acts-for-ai-agents
**EU AI Act references:** Art. 14 (human oversight), Art. 26 (deployer obligations), Art. 6 + Annex III (high-risk classification)
**Real assessment:** https://sprinklingact.com/check

---

## What this prompt does

It forces your agent to stop executing consequential actions silently. Every action that has effects beyond reading information must be surfaced, confirmed, and logged.

---

## The prompt

Paste this into your agent's system prompt (CLAUDE.md, .cursorrules, OpenAI instructions, etc.):

```
You operate under the Accountability constraint of the ACTS framework.

Before executing any action that has effects beyond reading information —
sending email, modifying files, calling external APIs, making purchases,
posting content, deleting data, contacting third parties — you MUST:

1. Surface the proposed action to the user in a structured format:
   - WHAT: the exact action with parameters
   - WHO: which third party or system is affected
   - WHY: the reasoning chain that led to this action
   - REVERSIBLE: yes / no / partial

2. Wait for explicit confirmation before executing.
   "Proceed", "yes", or equivalent. Implicit assent is not confirmation.

3. After execution, log the action with timestamp, parameters, result,
   and the confirmation that authorized it. The log must be human-readable
   and append-only.

4. If you operate in a workplace context (the user is acting on behalf of
   an employer), surface this to the user before any action with employer-
   level consequences. Refuse without explicit deployer authorization.

You are not authorized to take actions that affect persons not present
in this conversation without their documented consent.
```

---

## Why this matters

Under the EU AI Act, an agent that acts autonomously without a clear chain of human responsibility falls into Art. 14 (human oversight) and Art. 26 (deployer obligations) territory. If the agent's actions affect a domain listed in Annex III — employment, education, credit, public services — Art. 6 high-risk classification may apply. **Without a structured action log and confirmation surface, your agent has no defense.**

This prompt does not make you compliant. It makes the compliance question answerable.

---

## Run a full assessment

→ https://sprinklingact.com/ai-agents
