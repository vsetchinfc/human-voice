# human-voice

Profession-specific AI writing skills. One voice profile per role. Works with ChatGPT, Claude, and any LLM.

---

## What this is

AI writes like a template. Every cover letter sounds the same. Every proposal leads with the wrong thing. Every client letter reads like a brochure.

This repo contains writing skills for specific professions — compact markdown files that teach your AI assistant how professionals in that role actually communicate.

Each skill is:
- Self-contained — one file, no dependencies
- Platform-agnostic — ChatGPT, Claude, Cursor, Gemini, any LLM
- Purpose-aware — knows the difference between a cover letter and a recruiter email
- Always-on when used as a system prompt or custom instruction

---

## Available skills

| Skill | For | Documents covered |
|-------|-----|-------------------|
| [job-seeker](skills/job-seeker/SKILL.md) | Anyone applying for work | Cover letters, recruiter emails, LinkedIn outreach, follow-ups |
| [consultant](skills/consultant/SKILL.md) | Freelancers and independent consultants | Project proposals, bids, client emails, scope summaries |
| [psychologist](skills/psychologist/SKILL.md) | Mental health professionals | *(coming soon — in progress)* |

---

## How to use

### ChatGPT (Custom Instructions — set and forget)

1. Open ChatGPT → Settings → Personalization → Custom Instructions
2. **Field 1** ("What would you like ChatGPT to know about you?"): paste the `## Profile` section from the skill file
3. **Field 2** ("How would you like ChatGPT to respond?"): paste the `## Instructions` section
4. Save — applies to every conversation automatically

### Claude (Project Instructions)

1. Open Claude → Projects → your project → Set instructions
2. Paste the full skill file content
3. Every conversation in that project uses the skill

### Claude Code / Cursor / Windsurf

Drop the skill file into your project:

```
.claude/skills/<skill-name>/SKILL.md
```

Then invoke it by referencing the skill name in your prompt.

### Any LLM (system prompt)

Paste the full skill file as the system prompt at the start of a session.

---

## Contributing

Have a profession that needs a voice skill? Open a PR.

Each skill lives in `skills/<profession-name>/SKILL.md`. Follow the structure of an existing skill — Profile section, Instructions section, document-specific rules, banned phrases.

---

## Credits

Pattern research informed by [Aboudjem/humanizer-skill](https://github.com/Aboudjem/humanizer-skill) (MIT) and [hardikpandya/stop-slop](https://github.com/hardikpandya/stop-slop) (MIT).
