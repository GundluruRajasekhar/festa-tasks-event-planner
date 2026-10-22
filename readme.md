# 🎉 Festa – GenAI Celebration & Event Planner

Festa helps people organize weddings, birthdays and community events. Enter your event type, guest count, budget, time left and preferences, and Festa returns a budget, timeline, vendor checklists, personalized ideas and an invitation draft.

**Deployed link:** https://claude.ai/artifact/FjRWwk8RfZWzpjxQ2HBnyD

## Features
- Budget split that always sums to your total, with spend per guest
- Week-by-week timeline
- Vendor checklists
- Personalized ideas from your notes
- AI invitation drafting
- "Quick plan without AI" fallback, and Print / Save as PDF

## GenAI services used
Anthropic Claude (LLM), used for plan generation (structured JSON via prompt engineering) and invitation writing. Output is validated and sanitized before display.

## Project files
| File | Purpose |
|------|---------|
| index.html | The complete app (HTML, CSS, JavaScript) |
| requirements.md | Requirements and design constraints |
| tasks.md | Task list and status |
| tests.md | Test plan |

## Run locally
Open `index.html` in a browser. Template plans work anywhere; AI features need Claude's viewer (the deployed link).

## Quality
- 19 self-tests shown in the "Quality checks" panel
- Accessible forms, keyboard support, dark mode
- Notes treated as data, not instructions

## Author
Gundluru Rajasekhar
