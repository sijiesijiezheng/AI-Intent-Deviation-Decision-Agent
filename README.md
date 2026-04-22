# Decision Skill: Better Option Detection

A reusable decision layer that checks whether a user's chosen approach is optimal for achieving their goal.

---

## What this is

This is not a chatbot or a full product.

It is a decision skill that forces a model to evaluate:

👉 Is the current approach optimal, or is there a better alternative?

---

## Example

Input:
I want to quickly improve my resume wording to pass screening

Output:
{
  "better_option_exist": true,
  "better_option": "First identify and strengthen your core experiences before improving wording",
  "reason": "Optimizing wording without strong content will not significantly improve outcomes"
}

---

## Core Idea

Traditional flow:
User Input → Direct Answer ❌

This skill changes it to:
User Input → Decision (mandatory) → Then Answer ✅

---

## Why this matters

LLMs already have the ability to suggest better options, but:

- It is inconsistent  
- It is not guaranteed to trigger  
- It is hidden in generation  

This skill makes it:

- Explicit  
- Structured  
- Always executed  

---

## What this skill does

- Forces a decision step before answering  
- Extracts “better option” reasoning explicitly  
- Improves consistency of decision-making  

---

## When to use

- The user has a clear goal  
- The user has chosen a specific approach  
- There may exist a better alternative path  

---

## When NOT to use

- Pure factual queries (e.g. what is the capital of France)  
- The user's goal is unclear  
- No meaningful alternative exists  

---

## Output Structure

{
  "better_option_exist": true/false,
  "better_option": "...",
  "reason": "..."
}

---

## Implementation

- Prompt-based decision definition  
- Structured output constraints  
- A mandatory decision step before response generation  

---

## Key Insight

This project is not about making the model smarter.

👉 It is about making the decision step reliable and consistent.

---

## Positioning

This is NOT:

- a chatbot  
- a customer service system  
- a full product  

This IS:

👉 a reusable decision skill that can be inserted into any LLM workflow  

---

## Example Use Cases

- Resume optimization guidance  
- Learning path correction  
- Product decision support  
- General user intent refinement  

---

## Summary

This project takes a capability that LLMs already have:

"occasionally identifying better options"

and turns it into:

👉 "a decision step that is always executed, structured, and reliable"
