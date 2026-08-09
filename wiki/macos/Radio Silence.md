---
type: tool
created: 2026-08-09
updated: 2026-08-09
status: draft
platforms:
  - macOS
technologies:
  - local AI
risk: medium
certainty: unverified
tags:
  - macos
  - firewall
  - privacy
  - ai-tools
---

# Radio Silence

## Summary

Radio Silence is recorded as a Mac firewall utility that can block network access for selected local AI tools. This can provide an observable check that those tools continue to work without sending screen or voice context to cloud services.

## Evidence

- A user-provided note attributes this workflow to [[Nick Chapsas]] and cites [[Speed Up Your AI Development Workflow by 2x]].
- Certainty: **unverified**. The original cited material, product documentation, and direct test results have not been ingested.

## Privacy Interpretation

Blocking a tool's network access can show whether it functions offline and prevent direct outbound connections while the rule is active. By itself, that does not establish the tool's behavior when network access is allowed or rule out data transmission through another process.

## Safety

Firewall rules may interrupt updates, authentication, synchronization, and other expected features. Record the blocked process and be prepared to reverse the rule.

## Connections

- [[Mac Productivity Utilities]] — The lightweight macOS toolkit containing this option.
- [[Nick Chapsas]] — Person credited with the workflow in the supplied note.

## Open Questions

- What is the canonical Radio Silence product page and current pricing or license?
- Which exact local AI tools and processes were blocked in the cited workflow?
- What test demonstrated that screen or voice context stayed local?

## Sources

- [[Speed Up Your AI Development Workflow by 2x]]
