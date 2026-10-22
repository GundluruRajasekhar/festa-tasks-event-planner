# Festa – Requirements

## Problem statement
Create a GenAI-powered planning assistant that helps users organize weddings, birthdays and community events with budgets, timelines, vendor checklists and personalized ideas.

## Users
Individuals and families planning a celebration, and community organizers with limited planning experience.

## Functional requirements
| ID | Requirement |
|----|-------------|
| FR1 | User selects an event type: wedding, birthday, community event, baby shower, anniversary or corporate party. |
| FR2 | User enters guests (2–5000), budget in ₹ (1,000–1,00,00,000), weeks remaining (1–104) and optional notes (max 300 characters). |
| FR3 | The app generates a budget breakdown whose amounts sum exactly to the total budget, plus average spend per guest. |
| FR4 | The app generates a countdown timeline matched to the weeks remaining. |
| FR5 | The app generates vendor checklists (venue, caterer, decorator and others). |
| FR6 | The app generates personalized ideas based on the user's notes. |
| FR7 | The app drafts an invitation text on request. |
| FR8 | A template plan is produced when AI is unavailable or fails. |
| FR9 | The user can print or save the plan as PDF. |

## GenAI usage
- Model: Anthropic Claude, called via the Claude Artifacts sample capability.
- Plan generation: prompt engineering with strict JSON output (summary, budget, timeline, vendors, ideas).
- Invitation drafting: a second prompt returning plain text.
- User notes are fenced as data in prompts; AI output is validated, cleaned and budget-rescaled before display.

## Non-functional requirements
- **Security:** no raw HTML insertion; input validation and limits; 3-second cooldown between AI calls.
- **Accessibility:** labels, field-level errors, live status messages, keyboard focus, 44px targets, light and dark contrast, reduced-motion support.
- **Efficiency:** single file, no external libraries, self-tests run when idle.
- **Reliability:** every AI failure path falls back to a template plan.
- **Testing:** 19 automated self-tests plus manual cases in the test plan.

## Out of scope
Real vendor booking, payments, user accounts and saved plans.
