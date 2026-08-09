---
status: configured
topic: "Personal technology tips, tricks, and practical reference notes"
purpose: "Capture useful technical knowledge in a concise, searchable, and reusable form"
audience: "The vault owner"
created: 2026-08-09
updated: 2026-08-09
---

# Wiki Profile

This file defines the decisions that vary between wiki instances. Before the first ingest, ask your preferred AI agent to read `AGENTS.md`, interview you, and replace the placeholders below with concrete answers.

## Scope

- Topic: Useful tips, tricks, fixes, commands, workflows, tools, and explanations across personal computing, software development, devices, networking, automation, and related technology.
- Purpose: Turn scattered technical discoveries into a concise personal reference that is easy to search, verify, and reuse.
- Audience: The vault owner. Assume general technical literacy, but include enough context to make a note useful months later.
- Decisions this wiki should support: How to accomplish a technical task, choose between tools or approaches, diagnose a problem, configure a system safely, and remember why a prior solution worked.
- Explicit exclusions: General news without lasting utility; copied documentation without added value; unsupported hacks; credential or secret storage; illegal access, malware, or instructions intended to harm systems or evade authorization.

## Source Policy

- Allowed source types: Personal notes and experiments, official documentation, standards, source code and release notes, issue trackers, reputable technical articles, conference material, forum discussions, videos, and AI conversations when clearly identified.
- Trusted or preferred sources: Prefer first-party documentation, standards, source code, reproducible local results, and maintainer statements. Community sources are useful for discovery and practical context.
- Evidence that must remain immutable: All files placed in `raw/`, including captured text, exports, logs, screenshots, and attachments. Add interpretation in `wiki/`; never silently rewrite the original evidence.
- Sources that require extra verification: AI-generated material, anonymous posts, unmaintained tutorials, security advice, commands that modify or delete data, compatibility claims, benchmarks, and time-sensitive details such as prices, versions, APIs, and product availability.

## Knowledge Model

- Generated page types: `subject`, `source-summary`, `concept`, `tool`, `workflow`, `comparison`, `synthesis`, `question`, and `troubleshooting`.
- Required frontmatter beyond the global defaults: Add `platforms`, `technologies`, and `risk` when relevant. Use `risk: low`, `medium`, or `high` for operational instructions. Source summaries should retain source author, publication date, and canonical URL when available.
- Information to extract during ingestion: The problem or goal, prerequisites, tested environment, exact procedure, expected result, explanation, failure modes, safety and rollback notes, version constraints, reusable commands or snippets, provenance, and unresolved questions. Never record secrets in examples.
- Preferred subject taxonomy: Organize first by durable technical domain, such as operating systems, development, command line, networking, hardware, productivity, automation, security, and troubleshooting. Create narrower subject folders only when a cluster of related notes emerges; allow tags to span domains.

## Answering Policy

- Tone: Concise, practical, and direct. Lead with the answer or procedure, explain why it works, and call out destructive or security-sensitive steps before presenting them.
- Citation style: Cite compiled knowledge with Obsidian links and link claims to local source summaries where possible. Use normal Markdown links for external sources. Include exact versions and access dates when they affect validity.
- Certainty labels: Use `verified` for directly reproduced results or strong primary evidence, `supported` for converging reliable sources, `tentative` for plausible but incomplete evidence, and `unverified` for material not yet checked. State conflicts explicitly.
- Rules for web research: Search the web when the user asks, when local evidence is insufficient, or when facts may have changed. Prefer primary and current sources, verify risky instructions against at least one authoritative source, record retrieval dates for time-sensitive claims, and preserve useful research as source evidence before relying on it for durable pages.
