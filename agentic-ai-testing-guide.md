# 🤖 Agentic AI in Testing: Where Automation Stops and Judgment Begins
### *A Human-in-the-Loop Framework for Autonomous Test Agents*

GenAI prompts generate a test. **Agentic AI runs one** — it plans, executes, and iterates across multiple steps without a human re-prompting it at every turn. That autonomy is powerful, and it's exactly where a new risk shows up: an agent that writes the implementation, writes the tests for it, and then reports "all green" hasn't been checked by anyone — it's graded its own homework.

This guide is my framework for using agentic AI in testing without losing the one thing it can't replace: human judgment on what actually matters.

---

## 🧩 GenAI vs. Agentic AI — Know Which One You're Using
| | GenAI (Prompt-based) | Agentic AI |
| :--- | :--- | :--- |
| **Scope** | One prompt → one output (see my [Integrated AI Toolkit](./README.md#-integrated-ai-toolkit)) | Multi-step plan: explore → test → re-test → report |
| **Human role** | Reviews every output | Reviews checkpoints, not every step |
| **Main risk** | Bad prompt, bad output | Agent validates its own assumptions across many steps before a human ever sees them |

> [!IMPORTANT]
> **The core problem:** If the same model (or a model with the same blind spots) writes the code, the tests, *and* judges the result, "tests passed" only proves internal consistency — not that the software does what the user actually needed.

---

## 🛑 The Human-in-the-Loop Checkpoint Framework
Agentic testing doesn't mean removing the human — it means placing them at the points where judgment, not pattern-matching, is required. An agent should **never cross these checkpoints unsupervised**:

1. **Ambiguous Business Rules** — if the acceptance criteria could reasonably mean two different things, the agent must escalate, not guess.
2. **Accessibility & UX Calls** — whether a flow "feels" confusing or an error state is genuinely clear is a human judgment, not a pass/fail assertion.
3. **Risk Prioritization** — the agent can surface a list of edge cases; a human decides which ones are worth the team's time before release.
4. **Out-of-Distribution Scenarios** — real users do things no spec anticipated. An agent trained on the spec can't reliably test what the spec never imagined.

---

## 🔄 Example Workflow
1. **Agent proposes** a risk-based test plan from the user story and acceptance criteria.
2. **Human reviews** the plan specifically for the four checkpoints above — not the whole plan line by line.
3. **Agent executes** the approved plan: functional, boundary, and regression checks.
4. **Human validates** exploratory findings and anything flagged as ambiguous or out-of-distribution.
5. **Sign-off** happens on the human's judgment, with the agent's execution as evidence — not the other way around.

> [!TIP]
> **Rule of thumb:** if you can't point to the specific checkpoint where a human looked at this, the agent didn't test it — it assumed it.

---

## 🎓 About the Lead
I am **Ana González Lamé**, a Quality Engineering Analyst with over six years of experience.
* **Senior QA Analyst**, manual/exploratory/API testing in agile teams.
* **Google Generative AI Leader Certified.**
* **ISTQB® Certified Tester** (Foundation Level).
* **Women Techmakers Ambassador** & International Speaker.

---
[www.anagonzalez.uy](http://www.anagonzalez.uy)
