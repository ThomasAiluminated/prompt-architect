# Prompt Architect

**Een Claude-skill die een ruwe, vage vraag omzet in een sterke prompt die je meteen kunt gebruiken.**

Je typt in één zin wat je wilt ("maak een prompt om van een wetenschappelijk artikel een LinkedIn-post te maken") en krijgt een uitgewerkte, herbruikbare prompt terug. Die prompt zit vol technieken waarvan bekend is dat ze bij Claude het beste resultaat geven.

*English summary: a Claude skill that turns a rough one-line request into a well-structured, reusable, ready-to-paste prompt for Claude. It works in Dutch, French and English.*

## Wat de skill doet

- **Zoekt eerst wat echt gevraagd wordt:** de taak, het eindproduct, het publiek, de kwaliteitslat en wat de taak moeilijk maakt. Op dat moeilijke deel legt de prompt de nadruk.
- **Stelt alleen vragen als een verkeerde gok veel zou kosten.** Anders bouwt hij de prompt meteen en somt hij achteraf zijn aannames op.
- **Gebruikt technieken die voor Claude werken:**
  - context vóór de taak, en uitleg waarom de taak ertoe doet
  - een rol alleen als die echt expertise toevoegt
  - XML-tags om instructies en bronmateriaal gescheiden te houden
  - `{{PLACEHOLDERS}}` zodat de prompt herbruikbaar is
  - lang bronmateriaal bovenaan, de vraag onderaan
  - de reden achter elke beperking ("onder 200 woorden, want…")
  - ruimte om eerst te redeneren bij complexe analyses
  - succescriteria waarmee Claude zichzelf kan controleren
- **Volgt je taal:** Nederlands, Frans of Engels, naargelang je vraag.
- **Geen geroep in hoofdletters.** Rustige, precieze instructies werken beter dan "CRITICAL" of "YOU MUST".

## Wat je terugkrijgt

1. **De prompt** in één codeblok, klaar om te kopiëren
2. **Variabelen**: wat je in elke placeholder zet
3. **Keuzes en aannames**: 2 à 4 korte punten
4. Eventueel **één variant**, bijvoorbeeld een kortere versie of een systeemprompt voor een Claude-project

## Voor wie

Voor wie Claude al regelmatig gebruikt voor professioneel werk (onderzoek, schrijven, keynotes, projectvoorstellen, nieuwsbrieven, lesmateriaal) en sneller een sterke prompt wil, zonder elke keer van nul te beginnen.

Werk je in het onderwijs en wil je prompts die ook in ChatGPT, Gemini of Copilot werken, met didactische uitleg erbij? Kijk dan naar [Edu Prompt Coach](https://github.com/ThomasAiluminated/edu-prompt-coach).

## Installeren

**In Claude (web, desktop of mobiel):**
1. Download [`prompt-architect.skill`](prompt-architect.skill)
2. Upload het bij de Skills in je Claude-instellingen
   (of open het bestand in een gesprek met Claude en klik op *Save skill*)

**In Claude Code:** kopieer de map `prompt-architect/` naar `~/.claude/skills/`.

Daarna volstaat een gewone vraag, zoals *"schrijf een prompt om interviews te analyseren op terugkerende thema's"*. De skill start vanzelf.

## Structuur

```
prompt-architect/
└── SKILL.md            # de volledige instructies van de skill
prompt-architect.skill  # installeerbaar pakket
```

## Bijdragen

Ideeën en verbeteringen zijn welkom via een issue of pull request.

## Licentie

[CC BY 4.0](LICENSE): vrij te gebruiken, aan te passen en te delen, met naamsvermelding.

---

Gemaakt door **Thomas Donvil**, [Ailuminated](https://ailuminated.org), AI-geletterdheid voor het onderwijs.
