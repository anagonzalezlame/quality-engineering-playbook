# 🤝 GenAI Prompts: Agent–Human Handoff for Agentic Testing

Strategic prompts to set boundaries *before* an agent runs autonomously, and to structure the human checkpoint when it hands control back.

---

## Prompt 1: Risk-Boundary Definition Before Agent Execution
> **Role:** Senior Quality Engineering Analyst briefing a testing agent.
> **Context:** A user story with acceptance criteria for [feature].
> **Task:** Before execution, list every acceptance criterion that is ambiguous enough to require human interpretation, and flag it instead of assuming a default behavior.
> **Output:** A short list of "Escalate before testing" items, separate from the items safe for autonomous execution.

## Prompt 2: Agent Self-Audit Request
> **Role:** Act as the testing agent reporting back after execution.
> **Task:** For every test marked "passed," state whether the pass criteria were defined by the same model/logic that generated the implementation, or independently derived from the acceptance criteria.
> **Goal:** Surface hidden confirmation bias before a human reviews the results.

## Prompt 3: Human Sign-off Checklist Generation
> **Context:** An agent has completed a full test cycle on [feature].
> **Task:** Generate a sign-off checklist containing only the items a human must personally verify: accessibility/UX judgment calls, ambiguous business rules, and any scenario outside the original spec.
> **Requirements:** Exclude anything that's a deterministic pass/fail the agent already verified — this checklist is for judgment calls only.

## Prompt 4: Escalation Trigger Design
> **Task:** Act as a QA Lead designing guardrails for an autonomous testing agent.
> **Task:** Define 5 concrete conditions that should automatically pause the agent and request human input (e.g., conflicting requirements, a test result that contradicts a prior assumption, an edge case with no documented expected behavior).
> **Output:** A short rules list the agent can be configured to check against mid-run.
