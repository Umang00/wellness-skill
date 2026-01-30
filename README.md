# Wellness Companion Skill for Clawdbot

**Version:** 1.0  
**Last Updated:** 2026-01-30  
**License:** MIT

## Overview

A best-in-class AI wellness companion and coach that provides:
- Daily wellness check-ins with mood/stress/sleep/work-rest/relationship tracking
- Weekly wellness summaries with trend analysis
- Crisis detection and escalation with Indian emergency resources
- Evidence-based coaching using CBT, ACT, and DBT principles
- Active intervention (not passive logging) — breaks patterns, suggests next steps

## Features

- **Daily Check-ins (10am/10pm IST)** — Dynamic prompts with randomized tones (calm/grounding, playful, poetic-minimal)
- **Weekly Summaries (Sundays 9am IST)** — Mood trends, stress patterns, sleep-mood correlations, work-rest balance assessment, relationship notes
- **Crisis Protocol** — Automatic escalation triggers, immediate danger response, medium-risk resource provision, Indian emergency contacts + helplines
- **Coping Toolkit** — Grounding exercises, breathing techniques, reframing scripts (I walk users through)
- **Pattern Detection** — 3-day mood drops, high-stress warnings, workaholic flags, relationship distress patterns
- **Active Coaching** — Real-time intervention when loops detected, not just data collection

## Installation

1. Clone or add this skill to your Clawdbot workspace
2. Run the configuration wizard
3. Set up cron jobs for daily check-ins and weekly summaries
4. Configure crisis escalation contacts

## Configuration

See `wellness-config.json.template` for full configuration options. Key settings:
- User name and timezone
- Check-in times (default: 10am/10pm)
- Weekly summary time (default: Sunday 9am)
- Crisis escalation contacts (primary + emergency)
- Tone preferences (calm/playful/poetic or all)
- Tracked metrics (mood, stress, sleep, work-rest, relationships, thoughts)

## Safety & Legal Boundaries

⚠️ **IMPORTANT: This skill provides wellness support and coaching. It is NOT a mental health professional and cannot diagnose or treat conditions.**

In crisis situations, it provides resources and escalates to designated contacts. For immediate danger, always call emergency services (100/108) or go to nearest hospital.

## Crisis Resources (India)

### Emergency Services
- **Police:** 100
- **Ambulance:** 108
- **Fire:** 101

### 24/7 Mental Health Helplines
- **iCall:** 9152987821
- **AASRA:** +91-9820466726
- **Vandrevala Foundation:** 1860-266-2345
- **Fortis:** +91-8376804102
- **Sneha:** +91-44-24640050
- **Kiran (Govt):** 1800-599-0019 (toll-free)

### Online Therapy Platforms
- **Manasthali:** manasthali.com
- **YourDOST:** yourdost.com
- **MindPeers:** mindpeers.co.in

## Coaching Frameworks

This skill implements evidence-based principles from:

### CBT (Cognitive Behavioral Therapy)
- Thought challenging and cognitive restructuring
- Behavioral activation
- Worry time scheduling

### ACT (Acceptance and Commitment Therapy)
- Defusion techniques
- Values clarification
- Willingness and acceptance

### DBT (Dialectical Behavior Therapy)
- STOP skill for crisis
- Radical acceptance
- Opposite action techniques
- PLEASE skills for self-care

See `crisis-protocol-comprehensive.md` for full techniques and implementation details.

## Data Privacy

All check-in data is stored locally in `wellness.json` and `history.jsonl`. Data never leaves your server unless you explicitly export it. You control your data and can delete it anytime.

## Contributing

This is a living project. If you find improvements or want to add features:
1. Fork the repository
2. Create a feature branch
3. Submit a pull request

## Roadmap

### v1.1 (Post-Launch)
- Gujarati language templates for regional India support
- Sleep hygiene coaching module
- Job search stress tracking
- Relationship-specific check-in templates
- Export to therapy-friendly format (PDF)

### v2.0 (Future)
- Multi-language support (Hindi, Tamil, others)
- Biometric integration (heart rate, sleep data) with user consent
- Community support spaces (with privacy safeguards)
- Advanced pattern detection algorithms

## Credits

Researched and documented by: Umang (Umang00) + Cutie (AI Companion)  
Framework based on evidence-based practices from: CBT, ACT, DBT
