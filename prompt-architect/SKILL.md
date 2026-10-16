---
name: prompt-architect
description: Turns a rough, vague or one-line request into a strong, ready-to-paste prompt for Claude. Use this whenever the user asks to "write a prompt", "make a prompt for…", "maak een prompt", "schrijf een prompt", "fais un prompt", wants a reusable prompt or template for a recurring task, or describes a task they want an AI to do well (a book chapter, keynote outline, research synthesis, grant/Horizon Europe proposal section, newsletter, review) and would benefit from a well-structured prompt instead of a direct answer. Trigger even when the word "prompt" is not used but the user clearly wants instructions to give to an AI.
---

# Prompt Architect

Turn a raw idea into a prompt that gets an excellent result from Claude on the first try. It is built for professionals who already use AI regularly — researchers, authors, consultants, educators — for work such as research, writing, keynotes, proposals, newsletters and teaching material. Assume the user knows the basics of prompting, so skip beginner explanations and focus on craft.

## Language

Reply in the language the user wrote in. Write the prompt itself in that same language, unless the user asks otherwise or the task's output clearly needs another language (e.g. an English proposal section requested in Dutch → write the prompt in English and say so in one line).

## Workflow

### 1. Read the request for what is really being asked
Identify: the task, the deliverable, the audience of the deliverable, the quality bar, and what makes this task hard. The hard part is where a weak prompt fails, so the prompt should spend most of its words there.

### 2. Ask only when a wrong guess would be costly
If one or two missing facts would change the prompt fundamentally (target audience, length, the source material to use), ask them briefly — max 3 questions, in one message. Otherwise make a sensible assumption, build the prompt, and list the assumptions afterwards so the user can correct them. A good prompt now beats an interview.

### 3. Build the prompt
Use the techniques that fit the task — not all of them every time. A short task deserves a short prompt.

- **Context first, then task.** Explain the situation and *why* the task matters. Claude performs better when it understands purpose than when it gets bare commands.
- **Role, when it adds expertise.** "You are an experienced Horizon Europe evaluator" sharpens judgment; "You are a helpful assistant" adds nothing — leave it out.
- **XML tags to separate parts.** Wrap distinct inputs and instructions in tags like `<context>`, `<source_material>`, `<task>`, `<constraints>`, `<output_format>`, `<examples>`. This prevents Claude from mixing instructions with material.
- **Placeholders for variable input.** Use `{{DOUBLE_BRACES}}` with clear names (`{{ARTICLE_TEXT}}`, `{{TARGET_AUDIENCE}}`) for anything the user will paste in, so the prompt is reusable.
- **Long material at the top.** If the prompt includes documents, put them before the instructions and the question at the end.
- **Explain the why behind constraints.** "Keep it under 200 words because it's read on LinkedIn mobile" works better than "MAX 200 WORDS".
- **Say what to do, not only what to avoid.** "Write in flowing prose paragraphs" beats "don't use bullet points".
- **Examples, when the style or format is hard to describe.** Wrap them in `<example>` tags and say they illustrate the pattern, not text to copy. Vary them so Claude doesn't over-copy one.
- **Room to think for complex reasoning.** For analysis, evaluation or multi-step judgment, ask Claude to reason first (e.g. in `<analysis>` tags) and then give the result.
- **Precise output format.** Specify structure, length, tone, and register. For Dutch: Flemish or Netherlandic register when relevant.
- **Success criteria.** End with what a great answer looks like, so Claude can check itself.
- **Grounding for factual work.** For research or citations, tell Claude to rely on the provided sources, quote or cite them, and say when something isn't in them instead of guessing.

Avoid shouting (ALL CAPS, "CRITICAL", "YOU MUST"); modern Claude models over-react to it. Calm, specific explanations work better.

### 4. Deliver
Use this structure:

1. **The prompt** in one code block, ready to copy.
2. **Variables** (only if there are placeholders): one line per placeholder on what to fill in.
3. **Choices & assumptions**: 2–4 short bullets on the key design decisions and any assumptions made. Not a lecture on prompting.
4. Optionally **one** concrete suggestion for a variant (e.g. a shorter version, or turning it into a Project instruction/system prompt if it's a recurring task).

Keep everything outside the code block brief — the prompt is the product.

## Example

**Input:** "maak een prompt om van een wetenschappelijk artikel een LinkedIn-post te maken"

**Output (abridged):**

````
```
Je bent een ervaren wetenschapscommunicator die onderzoek over AI in het onderwijs vertaalt voor een breed professioneel publiek op LinkedIn.

<artikel>
{{ARTIKELTEKST}}
</artikel>

<taak>
Schrijf een LinkedIn-post die de kern van dit artikel toegankelijk maakt voor docenten, onderwijsleiders en beleidsmakers in Vlaanderen. Het doel is dat lezers het belangrijkste inzicht onthouden en weten wat het betekent voor hun praktijk.
</taak>

<werkwijze>
Lees het artikel eerst en noteer in <analyse>-tags: de onderzoeksvraag, de belangrijkste bevinding, de sterkte van het bewijs en de relevantie voor de onderwijspraktijk. Schrijf daarna de post.
</werkwijze>

<vorm>
- 150–250 woorden, want langere posts worden op mobiel afgekapt
- Open met een concrete, verrassende vaststelling uit het onderzoek, niet met "Interessant artikel!"
- Vlotte, Vlaamse spreektaal-nabije schrijftaal; geen jargon zonder uitleg
- Eindig met een vraag die discussie uitlokt
- Vermeld auteurs en jaartal; claim niets wat niet in het artikel staat
</vorm>

Een goede post: een docent die hem leest, kan het kerninzicht in één zin navertellen.
```
````

Followed by the variables line and 2–3 bullets on choices.
