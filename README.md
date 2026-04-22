# Decision Skill: Better Option Detection

A decision skill that checks whether a user's chosen approach is optimal for achieving their goal.

---

## What this does

Instead of directly answering user questions, this skill forces a decision step:

👉 **Is the current approach optimal, or is there a better alternative?**

---

## Example

### Input
> "I want to improve my resume wording"

### Output
```json
{
  "better_option_exist": true,
  "better_option": "First identify and strengthen your core experiences before improving wording",
  "reason": "Optimizing wording without strong content will not significantly improve outcomes"
}
Core Logic

Traditional LLM flow:

User Input → Direct Answer ❌

This skill adds a decision layer:

User Input → Decision (mandatory) → Then Answer ✔

Why this matters

LLMs already have the ability to suggest better options, but:

It is inconsistent
It is not guaranteed to trigger
It is implicit (hidden in generation)

This skill makes it:

👉 Explicit, structured, and always executed

What this skill actually does
Converts implicit reasoning into explicit decision logic
Forces the model to evaluate alternatives before responding
Improves consistency of decision-making
When to use this skill
The user has a clear goal
The user has chosen a specific approach
There may exist a better alternative path
When NOT to use
Pure information queries (e.g. "What is the capital of France?")
The user's goal is unclear
No meaningful alternative exists
Output Structure
{
  "better_option_exist": true/false,
  "better_option": "...",
  "reason": "..."
}
Implementation (Simplified)

This skill is implemented using:

Prompt-based decision definition
Structured output constraints
A dedicated decision step before response generation
Key Insight

This project is not about making the model smarter.

👉 It is about making the decision step reliable and consistent

Positioning

This is not:

a chatbot
a customer service system
a full product

This is:

👉 a reusable decision skill that can be inserted into any LLM workflow

Example Use Cases
Resume optimization guidance
Learning path correction
Product decision support
General user intent refinement
Repository Structure
decision_skill.js → core logic
workflow.png → original workflow (optional reference)
Summary

This project extracts a hidden capability from LLMs:

👉 detecting better alternatives

and turns it into:

👉 a stable, reusable decision layer
