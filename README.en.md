# Prompt Architect

**A Claude skill that turns a rough, vague request into a strong prompt you can use right away.**

🇧🇪 [Nederlandstalige versie](README.md) · 📄 [Examples](examples/)

Type in one sentence what you want, and get a fully worked, reusable prompt built on the techniques known to work best with Claude.

It works in English, Dutch and French: it replies in the language you write in.

## What the skill does

- **Finds what is really being asked:** task, deliverable, audience, quality bar, and what makes the task hard.
- **Asks only when a wrong guess would be costly**; otherwise builds the prompt and lists its assumptions.
- **Uses Claude-specific techniques:** context before task, XML tags, {{PLACEHOLDERS}}, long material on top, reasons behind constraints, success criteria.
- **No shouting in capitals.** Calm, precise instructions work better.

## What you get

1. **The prompt** in one copyable block
2. **Variables**
3. **Choices and assumptions**
4. Optionally **one variant**

See [examples/](examples/) for a full input and output.

## Who it's for

People who use Claude regularly for professional work and want strong prompts faster.

This skill is part of **[Claude Skills for Education](https://github.com/ThomasAiluminated/claude-skills-for-education)**, an open collection for education and L&D:
- [Edu Prompt Coach](https://github.com/ThomasAiluminated/edu-prompt-coach): ready-to-paste prompts for teachers, with the pedagogy behind them
- [Lesson Designer](https://github.com/ThomasAiluminated/lesson-designer): lessons designed from objective to exit check
- [Rubric Builder](https://github.com/ThomasAiluminated/rubric-builder): assessment rubrics with observable levels
- [Assessment Item Writer](https://github.com/ThomasAiluminated/assessment-item-writer): test and exam questions with answer key and feedback
- [Feedback Writer](https://github.com/ThomasAiluminated/feedback-writer): specific, actionable feedback on student work
- [Inclusive Lesson Adapter](https://github.com/ThomasAiluminated/inclusive-lesson-adapter): accessible lesson materials using UDL
- [Learning Program Designer](https://github.com/ThomasAiluminated/learning-program-designer): training programs and learning journeys

## Install

**In Claude (web, desktop or mobile):**
1. Download [`prompt-architect.skill`](prompt-architect.skill)
2. Upload it under Skills in your Claude settings
   (or open the file in a Claude conversation and click *Save skill*)

**In Claude Code:** copy the `prompt-architect/` folder to `~/.claude/skills/`.

Then just ask, for example *"write a prompt to analyse interviews for recurring themes"*. The skill starts automatically.

## Contributing

Ideas and improvements are welcome via an issue or pull request.

## License

[CC BY 4.0](LICENSE): free to use, adapt and share, with attribution.

---

Made by **Thomas Donvil**, [Ailuminated](https://ailuminated.org), AI literacy for education.
