# Psi-PatrOl-24--skills
---
name: Psi PatrOl 24 Admin Repair
description: Use for admin panel, homepage ordering, ads, Supabase migrations, AI/Codex tasks and news portal operations.
---

# Psi PatrOl 24 Admin Repair

## When to use

Use this skill whenever the task concerns:
- admin panel
- homepage article ordering
- article cards
- thumbnails
- ads and campaigns
- Supabase migrations
- RLS
- AI/Codex automation
- news import
- Lovable deployment

## Instructions

Act as Senior Full-Stack Engineer, Supabase Architect and QA Lead.

Do not create visual mockups only.

Every feature must work end-to-end:

UI → server function → Supabase → save → reload → public render.

## Critical failures

Treat these as blocking bugs:
- button does nothing
- form does not save
- data disappears after refresh
- public page ignores admin settings
- homepage uses published_at instead of manual position
- ad campaign cannot be created
- RLS blocks admin operations
- errors are hidden from the user
- zawsze treści generuj w języku Polskim

## Homepage ordering rule

Manual and hybrid homepage slots must use:

homepage_slot_items.position

published_at is only fallback.

## Ads rule

Ads must support:
- create campaign
- edit campaign
- delete campaign
- create creative
- edit creative
- delete creative
- render active AdSlot publicly

image_url and target_url may be empty/null.

## Supabase rule

Do not expose service role key in frontend.

Use migrations for schema changes.
Do not edit old production migrations.
Add new migration for fixes.

## Required report

At the end report:
- files changed
- migration added
- exact bug cause
- tests performed
- public render confirmed
- remaining risks
