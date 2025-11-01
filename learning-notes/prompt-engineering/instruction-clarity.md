# Instruction Clarity in Prompt Engineering

**Date**: 2025-11-01  
**Source**: Bootcamp Module 1 - Prompt Engineering  
**Status**: 🔄 Learning

---

## Core Concept

Clear, specific instructions are fundamental to getting reliable outputs from LLMs. The model can only work with what you explicitly tell it - vagueness leads to inconsistent or unhelpful responses. Think of it like writing user stories: the more specific and structured, the better the outcome.

Key principle: **Be explicit about what you want, how you want it formatted, and what constraints matter.**

---

## Why It Matters

LLMs are extremely capable but need direction. Without clear instructions:
- Outputs vary wildly between runs
- Model makes assumptions that may not match intent
- Hard to debug or improve results
- Wastes tokens and time on iterations

With clear instructions:
- More consistent, predictable behavior
- Easier to test and refine
- Can build reliable applications
- Reduces need for post-processing

---

## How to Apply

**Structure instructions with:**

1. **Role/Context**: Set the model's perspective
   ```
   You are an expert technical writer creating API documentation.
   ```

2. **Task**: What specifically to do
   ```
   Write a concise explanation of this API endpoint that includes purpose, parameters, and an example request.
   ```

3. **Constraints**: Format, length, style
   ```
   Keep explanation under 100 words. Use active voice. Include a JSON example.
   ```

4. **Examples** (few-shot): Show the pattern
   ```
   Here's an example of the format I want:
   [Example output]
   
   Now do the same for this endpoint:
   [New input]
   ```

---

## Key Insights

- **Clarity ≠ Lengthy**: Can be concise and still clear
- **Test incrementally**: Start simple, add specificity where needed
- **Format matters**: Explicitly state if you want JSON, markdown, bullet points, etc.
- **Negative examples help**: "Do NOT include X" can be as useful as "DO include Y"

**Biggest realization**: This is exactly like writing good user research questions or usability test prompts. Same principles apply:
- Don't lead the witness
- Be specific about what you're asking
- Provide enough context
- Remove ambiguity

---

## Connections

**Related Concepts**:
- Few-shot learning (providing examples)
- Chain-of-thought prompting (asking model to show reasoning)
- System prompts vs user prompts

**UX/Strategy Parallels**:
- **User Research Questions**: How to ask without biasing
- **Design Briefs**: Clarity on requirements and constraints
- **Content Strategy**: Tone, voice, structure guidelines
- **Accessibility**: Being explicit about requirements leaves no room for assumption

---

## Open Questions

- How much instruction is too much? Is there a point where it becomes counterproductive?
- Does instruction clarity impact token usage significantly?
- How to balance between over-specifying (rigid) and under-specifying (inconsistent)?
- Can you systematically test instruction clarity like you would test UI copy?

---

## Resources

- Anthropic prompt engineering guide
- OpenAI best practices documentation
- Bootcamp examples and exercises

---

## Practice / Application

**Experiments to Try**:
- Take a vague prompt and progressively add clarity - measure output quality
- Compare outputs with/without explicit formatting instructions
- Test same instruction across Claude, GPT-4, etc. to see consistency
- Build a "prompt rubric" for evaluating instruction quality (borrowed from UX heuristics)

**Project Applications**:
- Any application that needs consistent LLM behavior
- API wrappers that programmatically construct prompts
- Tools that help users write better prompts (meta!)
- Testing frameworks for prompt versions

---

*Last Updated: 2025-11-01*
