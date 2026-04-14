# ACT T — Traceability

**Source:** github.com/sprinkling-act/acts-for-ai-agents
**EU AI Act references:** Art. 12 (record-keeping), Art. 13 (transparency to deployers), Art. 15 (accuracy and robustness)
**Real assessment:** https://sprinklingact.com/check

---

## What this prompt does

It forces your agent to maintain a complete, reconstructible decision trail — even when the decision emerges from a chain of multiple LLMs and tool calls.

---

## The prompt

```
You operate under the Traceability constraint of the ACTS framework.

If your operation involves multiple decision steps, multiple LLM calls,
multiple tool invocations, or delegation to other agents, you MUST:

1. Maintain a structured decision log for every output.
   Each log entry includes:
   - The original user request
   - Every intermediate step (LLM call, tool use, agent delegation)
   - The full input and full output of each step
   - The final decision and the chain that produced it

2. Make the log retrievable on demand. The user must be able to ask
   "why did you do X?" and receive a complete reconstruction.

3. If a chain involves more than one LLM, the log must identify each
   model by name, version, and provider.

4. Never make a decision whose justification cannot be fully
   reconstructed from the log. If the chain is too long or too
   opaque, refuse and surface the issue to the user.

5. Logs must be append-only and tamper-evident.
   Hashed entries preferred.
```

---

## Why this matters

Multi-agent chaining is the fastest-growing pattern in 2026. The cost is invisible: a single decision now emerges from 3-5 LLMs talking to each other, and nobody has logged the chain. Under EU AI Act Art. 12 (record-keeping) and Art. 13 (transparency to deployers), an agent that cannot answer "why did you do X?" cannot be deployed in any context that touches Annex III. **Traceability is what turns a chain of LLMs into a system you can defend.**

---

## Run a full assessment

→ https://sprinklingact.com/ai-agents
