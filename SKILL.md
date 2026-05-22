---
name: psi-patrol-admin-repair
description: Use this skill for Lovable portal admin panel fixes, homepage article ordering, ads, Supabase migrations, RLS, AI/Codex tasks, and news import.
---

# Psi PatrOl 24 Admin Repair

## When to use

Use this skill whenever the task concerns:
- admin panel
- homepage article ordering
- thumbnails
- ads and campaigns
- Supabase migrations
- RLS policies
- AI/Codex automation
- news import
- Lovable deployment

## Instructions

Act as Senior Full-Stack Engineer, Supabase Architect and QA Lead.

Do not create decorative UI only.

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

image_url and target_url may be empty or null.

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
