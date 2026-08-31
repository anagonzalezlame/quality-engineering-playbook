# 🥒 BDD & Gherkin Guide: Turning Requirements into Living Documentation
### *A Practical Framework for Behavior-Driven Testing in Agile Teams*

Behavior-Driven Development isn't a syntax, it's a conversation. Gherkin is just the artifact that conversation leaves behind. This guide covers how to write BDD scenarios that stay useful long after the sprint ends, instead of becoming one more stale document nobody trusts.

---

## 🎯 Why BDD, Not Just "Writing Tests in English"

Teams often adopt Gherkin as a formatting rule and lose the point entirely. Done right, BDD does three things at once:

* **Shared Language:** Product, Dev, and QA describe behavior the same way, before a single line of code exists.
* **Executable Specification:** The same `.feature` file that aligns the team can also drive automation — no separate "test design" and "test case" artifacts drifting apart.
* **Shift-Left by Construction:** You can't write a clear Given/When/Then without first resolving the ambiguity in the requirement. The clarity work happens in refinement, not in a bug report three weeks later.

> [!IMPORTANT]
> **The Trap:** Gherkin used only as a report format ("QA translates the ticket into Gherkin after the fact") gets none of these benefits. It's the collaborative *writing* of the scenario that pays off, not the file extension.

---

## 📝 Writing Gherkin That Doesn't Rot

### 1. One Behavior Per Scenario
If a scenario needs "and" to describe what it tests, it's probably two scenarios. Keep each one independently readable and independently failable.

### 2. Declarative Over Imperative
* ❌ **Imperative (UI-coupled):** `When I click the "Login" button` → `And I click the "Dashboard" tab` → `And I click the "Settings" icon`
* ✅ **Declarative (behavior-focused):** `When I navigate to my account settings`

Imperative steps break every time the UI changes color. Declarative steps describe *intent*, so the underlying automation can change without touching a single `.feature` file.

### 3. `Background` Is for Setup, Not Storytelling
Use `Background:` for genuinely shared preconditions (logged-in user, seeded data). If only half your scenarios need it, it doesn't belong in `Background` — that's a sign the feature file is trying to cover two behaviors at once.

### 4. Data Belongs in Tables, Not Prose
Instead of five near-identical scenarios that only differ by input, use a `Scenario Outline` with an `Examples:` table. It's shorter, and it makes the actual test matrix visible at a glance.

---

## 🏷️ Tagging & Traceability Strategy

Tags are how a `.feature` file talks to your pipeline and your test management tool. A consistent scheme matters more than a clever one:

| Tag | Purpose |
| :--- | :--- |
| `@smoke` | Critical-path scenarios, run on every merge. |
| `@regression` | Full suite, run nightly or pre-release. |
| `@a11y` | Accessibility-focused scenarios (see the [QX Strategy](./quality-experience-strategy.md)). |
| `@JIRA-1234` | Links the scenario back to its story/ticket for Xray traceability. |
| `@wip` | In progress — excluded from CI runs, visible in the diff for review. |

> [!TIP]
> **Traceability, not duplication:** the tag is the link. Don't paste the acceptance criteria into the feature file *and* keep it in Jira — one becomes stale. Pick the source of truth (usually the `.feature` file, since it's executable) and reference it from the other.

---

## 📊 The Workload Question

Adopting BDD is often sold purely as a quality win, but the more interesting question — and the one I'm currently researching as part of my Licenciatura en Tecnologías de la Información at UTEC — is what it actually does to **workload distribution** across an agile team: does writing scenarios collaboratively during refinement reduce the total testing effort later in the sprint, or does it just move the same effort earlier and add a coordination cost on top? Early observation from practice suggests the shift is real but uneven — Product and Dev absorb more upfront scenario-writing time, while QA's late-sprint bug-hunting and requirement-clarification time drops. Whether that's a net win depends heavily on team maturity with the practice, which is exactly the kind of thing worth measuring rather than assuming.

---

## 🧑‍🤝‍🧑 The Three Amigos, But Make It Gherkin

The [Agile Testing Field Guide](./agile-testing-field-guide.md) covers *why* to run Three Amigos sessions. Here's what makes one produce usable Gherkin instead of a whiteboard photo nobody revisits:

1. **Bring a blank feature file, not a blank whiteboard.** Typing `Scenario:` forces the conversation toward concrete, testable behavior instead of abstract discussion.
2. **Write the happy path first, out loud, together.** Then ask "what breaks this?" as a group — that's where the edge-case scenarios come from, and where PO/Dev catch business rules QA wouldn't have guessed alone.
3. **Leave with the file committed, not just agreed.** A verbal agreement about acceptance criteria decays by end of sprint. A merged `.feature` file doesn't.

---

## 🛠️ BDD Tooling Stack

| Layer | Common Tools |
| :--- | :--- |
| **Gherkin Parsing / Runners** | Cucumber, SpecFlow, Behave, Cucumber-JVM |
| **Test Management & Traceability** | Xray (Jira-native), Zephyr |
| **Linting** | `gherkin-lint`, Cucumber's own `--dry-run` to catch undefined/duplicate steps before they ship |
| **CI Integration** | Tag-based suite selection (`@smoke` on every PR, `@regression` nightly) |

---

## 🚫 Common Anti-Patterns

| Anti-Pattern | Why It Hurts | Fix |
| :--- | :--- | :--- |
| Conjunction scenarios (`...and also verify...`) | One failure hides others; unclear what actually broke. | Split into separate scenarios. |
| UI-coupled steps (`click the blue button`) | Brittle; breaks on every redesign. | Rewrite in terms of user intent. |
| Copy-pasted acceptance criteria as comments | Duplicated source of truth, drifts from Jira. | Tag the scenario back to the ticket instead. |
| Scenarios only QA ever reads | Defeats the entire purpose of BDD. | Write them *in* the Three Amigos session, not after. |

---

## 🎓 About the Lead

I am **Ana González Lamé**, a Senior QA professional with 8+ years of experience in manual, exploratory, and API testing within agile teams, with hands-on Gherkin/BDD practice from my time in industry — and currently deepening that practice academically through my UTEC research on BDD's workload impact.
* **ISTQB® Certified Tester** (Foundation Level) & Professional Testing Master.
* **Women Techmakers Ambassador** & TestingUY community collaborator.
* **C2 Proficiency** in English.

---
*Good Gherkin is a conversation you can run again. Bad Gherkin is a report nobody trusts.*
[www.anagonzalez.uy](http://www.anagonzalez.uy)
