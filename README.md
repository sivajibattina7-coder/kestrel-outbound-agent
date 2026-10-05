# Kestrel Outbound Research Agent

## What this agent does

The Kestrel Outbound Research Agent takes a public architecture/design firm's website URL and runs the outbound-research workflow for Kestrel Rooms.

It is designed to:

1. Identify the firm and its practice segment.
2. Check the firm, parent, or affiliate against the do-not-contact list.
3. Research the firm's public website.
4. Select one specific, verifiable fact from the firm's website.
5. Record the source URL for that fact.
6. Draft a personalised outbound email of 90 words or fewer.
7. Use only Kestrel's approved product claims.
8. Return a structured research result and email draft for review.

The assignment requires the agent to be usable on a new firm's website and to provide clear run instructions.

## How to run it

### Input

Provide one architecture/design firm's public website URL.

Example:

`https://briburn.com/`

### Run

Open **Kestrel Outbound Research Agent** and provide the website URL.

The simplest prompt is:

> Research this architecture firm: [PASTE WEBSITE URL]

The agent should then perform the research workflow and return the result.

## Expected output

The agent should return:

### Firm
- Firm name
- Website
- Practice segment
- Do-not-contact check

### Fact
- One specific fact found on the firm's public website
- The exact source URL where the fact was found

### Draft email
- Subject
- Email body
- Kestrel standard sign-off

### Status
- A short status note describing where the prospect stands

## Guardrails

The workflow follows the Kestrel outbound SOP:

- A prospect on the do-not-contact list, including a matching parent or affiliate, must not be researched or drafted.
- A fact must have a source URL. If a fact cannot be sourced, it must not be used.
- The outbound email must be 90 words or fewer.
- The email must open with the sourced fact.
- Product messaging must use only Kestrel's approved claims.
- The agent must not invent product numbers, customer names, comparisons, or other unsupported claims.
- The final email is a draft for approval; the SOP requires it to be moved to In Review and assigned to Nirbhay before approval.

## Approved Kestrel claims

The SOP permits the following product claims:

- Book rooms, plotters and the model shop from one calendar.
- Works with Google Calendar and Microsoft Outlook.
- Setup takes less than a day.
- Free 30-day trial, no card needed.

Approved calls to action:

- A 15-minute call
- The free trial

## Example

Input:

`https://briburn.com/`

Expected workflow:

`Website URL → DNC check → Website research → Sourced fact → Segment → Personalised email → Review`

The agent should never use an unsourced fact or proceed with a prospect that matches the do-not-contact rules.

## Deliverable context

This workflow export is Deliverable 2 of the Kestrel Outbound take-home assignment. The assignment allows the agent deliverable to be provided as a link, repository, or workflow export, provided that run instructions are clear enough for another person to run it on a new firm's website.
