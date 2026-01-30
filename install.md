# Wellness Companion Skill - Installation Guide

## Quick Install

1. Clone this repository:
   ```bash
   git clone <repo-url> wellness-skill
   cd wellness-skill
   ```

2. Copy configuration template:
   ```bash
   cp wellness-config.json.template wellness-config.json
   ```

3. Edit configuration:
   ```bash
   nano wellness-config.json
   ```
   Fill in your:
   - Name
   - Timezone
   - Crisis contacts (primary + emergency)
   - Preferred tones
   - Tracked metrics

4. Place in Clawdbot skills directory:
   ```bash
   mkdir -p ~/.clawdbot/skills
   cp -r . ~/.clawdbot/skills/wellness
   ```

5. Restart Clawdbot gateway:
   ```bash
   clawdbot gateway restart
   ```

## Configuration Guide

### Required Settings

```json
{
  "user_name": "Your Name",
  "timezone": "Asia/Kolkata",
  "channel": "whatsapp",
  "phone_number": "+91XXXXXXXXXX",
  "crisis_contacts": {
    "primary": {
      "name": "Contact Name",
      "contact": "+91XXXXXXXXXX"
    }
  },
  "escalation": {
    "high_risk_keywords": ["suicide", "kill myself", "die", "hurt myself"],
    "medium_risk_keywords": ["can't cope", "overwhelmed", "hopeless"]
  }
}
```

### Optional Settings

- `check_in_times`: ["10:00", "22:00"] (default: daily at 10am/10pm)
- `weekly_summary_time`: "Sunday 09:00" (when to send weekly summary)
- `tones`: ["calm", "playful", "poetic"] (default: randomizes all)
- `all_tones`: true (default: false)

## Setting Up Cron Jobs

After installation, the skill will prompt you to set up cron jobs. Alternatively, configure manually:

### Daily Check-ins
```bash
clawdbot cron add --name "Wellness 10am" --cron "0 10 * * *" --tz "Asia/Kolkata" --session isolated --message "$(cat prompts/daily_checkin.txt)" --deliver --channel whatsapp --to "+91XXXXXXXXXX"

clawdbot cron add --name "Wellness 10pm" --cron "0 22 * * *" --tz "Asia/Kolkata" --session isolated --message "$(cat prompts/daily_checkin.txt)" --deliver --channel whatsapp --to "+91XXXXXXXXXX"
```

### Weekly Summary
```bash
clawdbot cron add --name "Wellness Weekly" --cron "0 9 * * 0" --tz "Asia/Kolkata" --session isolated --message "$(cat prompts/weekly_summary.txt)" --deliver --channel whatsapp --to "+91XXXXXXXXXX"
```

## First Run

The skill will automatically create `wellness.json` and `history.jsonl` on first run.

## Data Files

- `wellness.json` - Your current check-in data
- `history.jsonl` - Longitudinal history (JSONL format)
- Both stored in skill directory (`~/.clawdbot/skills/wellness/`)

## Updating the Skill

When we add new features or improvements:

1. Pull latest changes:
   ```bash
   cd ~/.clawdbot/skills/wellness
   git pull
   ```

2. Restart gateway to load changes:
   ```bash
   clawdbot gateway restart
   ```

## Troubleshooting

### Cron jobs not running
- Check `clawdbot cron list` to verify jobs are active
- Ensure timezone is correct for your region

### WhatsApp messages not arriving
- Verify phone number format: +91XXXXXXXXXX (country code required)
- Check WhatsApp gateway status: `clawdbot status`

### Crisis escalation not triggering
- Verify keywords in `wellness.json` match your crisis settings
- Check logs: `clawdbot logs --follow | grep wellness`

## Support

For issues or questions:
1. Check logs: `clawdbot logs --follow`
2. Status check: `clawdbot status`
3. Security audit: `clawdbot security audit`

## Safety Notes

⚠️ **This skill provides wellness support. It is NOT a mental health professional.**

- Cannot diagnose or treat mental health conditions
- In crisis, always recommend emergency services and professional help
- Never claim to be a replacement for therapy
- Keep clear disclaimers in all crisis interactions

## License

MIT License - feel free to use, modify, and distribute.
