# Wellness Skill Plan

**Last Updated:** 2026-01-30
**Status:** Research complete, files created, GitHub repo live

---

## Architecture

```
wellness/
├── README.md                              # Full skill documentation
├── install.md                              # Installation + cron setup guide
├── .gitignore
├── wellness-config.json.template          # User config template
├── prompts/
│   ├── crisist_templates.txt            # Crisis message templates
│   ├── daily_checkin.txt                # Daily check-in prompts
│   └── weekly_summary.txt               # Weekly summary template
└── tools/
    └── coping_library.json               # CBT/ACT/DBT techniques
```

---

## Completed Components

### ✅ Crisis Protocol (Comprehensive)
- File: `CRISIS_PROTOCOL.md`
- 15 sections covering all aspects: detection, escalation, CBT/ACT/DBT, Indian resources
- Code-ready escalation logic
- Message templates for all risk levels
- Safety disclaimers and legal boundaries

### ✅ Configuration System
- Template: `wellness-config.json.template`
- Supports user customization: timezone, contacts, tones, metrics
- Pre-configured for Umang: IST, WhatsApp to +91 94261 54688

### ✅ Prompt Templates
- Daily check-in: 3 tone variations (calm/playful/poetic)
- Weekly summary: Trend analysis + insights
- Crisis templates: High/medium/low risk with escalation

### ✅ Coping Library
- Grounding techniques (5-4-3-2-1, safe place, progressive relaxation)
- Breathing exercises (box breathing)
- CBT techniques (thought challenging, behavioral activation)
- ACT techniques (defusion, values, willingness)
- DBT techniques (STOP skill, radical acceptance, opposite action, PLEASE skills)

---

## Implementation Status

### ✅ Files Created
All core skill files are now in place and committed to Git.

### ✅ GitHub Repository
- URL: https://github.com/Umang00/wellness-skill
- Status: Live and public
- Privacy: All private workspace files removed

### ✅ Memory Files Included
Two key planning documents are now part of the skill for reference:
- `CRISIS_PROTOCOL.md` — Complete crisis guide
- This was created in workspace memory, now properly included in skill

---

## Next Steps

### Immediate (1 Week of Use)
1. **Daily check-ins start** — 10am/10pm IST tomorrow (Jan 31)
2. **Data collection begins** — Mood, stress, sleep, work-rest, relationships
3. **Pattern detection starts** — After 3 days of data
4. **Weekly summary** — Sunday Feb 2, 9am IST
5. **Crisis testing** — Verify escalation triggers work correctly

### Feb 6, 2026 (Public Release)
1. **Package for public installation** — Create `SKILL.md` with proper metadata
2. **Refine based on data** — 1 week of Umang's check-ins
3. **Documentation polish** — Screenshots, examples, troubleshooting
4. **Release announcement** — Share with community

### Ongoing (Iteration)
- Add Gujarati templates (regional India)
- Sleep hygiene module
- Job search stress tracking
- Export to therapy-friendly PDF format
- Advanced pattern detection

---

## Key Learnings

1. **Privacy is critical** — Never commit private data to public repo
2. **User customization matters** — Templates, tones, contacts should all be configurable
3. **Evidence-based frameworks** — CBT/ACT/DBT are well-documented and translatable to text
4. **Cultural context is essential** — Indian emergency services, family dynamics, stigma considerations
5. **Active intervention > passive logging** — This is what makes it best-in-class

---

**This is a living plan.** Updated as we learn what works.
