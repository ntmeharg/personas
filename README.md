# Personas

Standing context on specific colleagues (working style, role, communication preferences, history), used through Claude Code.

One repository, not one-per-person. Claude should load the right person's `SKILL.md` when that person comes up in conversation. Root `CLAUDE.md` is the router: it tells Claude to check `skills/<person>/SKILL.md` whenever a tracked name is mentioned.

Treat this repo as private. Notes are professional / working-relationship context only — no sensitive personal information.

## How to add a person

1. Create `skills/<person-slug>/SKILL.md`. The slug is lowercase and hyphenated (`first-last`).
2. Copy the frontmatter and body template from an existing person file, then replace the name, slug, and description.
3. Fill in Role, Working Style, Standing Context, and History / Notes as you have real context. Placeholder sections are fine until then.
4. Add the person to the roster table in `CLAUDE.md`.
5. Commit with a message that names the person, e.g. `ben-matthews: add initial skill`.

Frontmatter:

```yaml
---
name: <person-slug>
description: Use when discussing, preparing for, or drafting communication
  to or about <Full Name>. Covers role, working style, and relevant history.
---
```

Write the `description` so Claude can match on first name, nicknames, or role references when those uniquely identify the person.

## How to update a person

1. Edit `skills/<person-slug>/SKILL.md`.
2. Commit with a message that says what changed and why.

Commit history is the point. Prefer:

```
ben-matthews: note new reporting change
```

over:

```
update
```

`git log -- skills/<person-slug>/SKILL.md` and `git diff` both work per person because each person has an isolated directory.

## Initial roster

- Ben Matthews — `skills/ben-matthews/`
- Nick Painton — `skills/nick-painton/`
- Kyle Kutter — `skills/kyle-kutter/`
- Greg Hall — `skills/greg-hall/`
- Bobby Gruenwald — `skills/bobby-gruenwald/`
