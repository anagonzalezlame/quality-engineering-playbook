# 🥒 GenAI Prompts: BDD & Gherkin Scenario Design

Strategic prompts to accelerate scenario writing, edge-case discovery, and Gherkin quality review during refinement and Three Amigos sessions.

---

## Prompt 1: Feature File Scaffolding from a User Story
> **Role:** Senior QA Engineer specializing in Behavior-Driven Development.
> **Context:** [Paste the User Story and its draft Acceptance Criteria here.]
> **Task:** Convert this into a Gherkin `.feature` file using declarative, UI-agnostic steps (describe user intent, not clicks/selectors).
> **Requirements:**
> 1. Include a `Background:` only if every scenario genuinely shares the same precondition.
> 2. Cover the happy path as the first scenario.
> 3. Flag any acceptance criterion that is too vague to convert directly into a testable step, and ask a clarifying question instead of guessing.

## Prompt 2: Edge Case & Negative Scenario Generation
> **Role:** Act as an Exploratory QA Analyst reviewing a happy-path scenario for gaps.
> **Context:** [Paste an existing happy-path Gherkin scenario.]
> **Task:** Generate 5 additional scenarios covering: boundary values, invalid/malformed input, permission/role edge cases, concurrent/race-condition behavior, and a plausible "unhappy path" a real user would hit.
> **Output:** Full Gherkin, tagged appropriately (`@edge-case`, `@negative`, `@security` where relevant).

## Prompt 3: Gherkin Anti-Pattern Refactor
> **Role:** Senior BDD Reviewer doing a pull-request pass on a `.feature` file.
> **Context:** [Paste a scenario that mixes multiple behaviors, uses imperative UI steps, or duplicates acceptance criteria as comments.]
> **Task:** Identify every anti-pattern present (conjunction scenarios, UI coupling, duplicated source of truth, missing traceability tag) and rewrite the scenario to fix them.
> **Output:** A side-by-side "Before / After" with a one-line reason for each change.

## Prompt 4: Scenario Outline & Examples Table Generation
> **Context:** [Describe a business rule that depends on a combination of inputs — e.g., a discount rule based on user tier and order total.]
> **Task:** Generate a `Scenario Outline` with a complete `Examples:` table covering all meaningfully distinct input combinations, including at least one boundary case per parameter.
> **Goal:** Replace what would otherwise be 6-8 near-duplicate scenarios with one outline and a compact data table.
