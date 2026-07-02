# Contributing

This repo holds behavioral rules for AI coding agents, not application code — most contributions are proposed edits to those rules, not new features.

## Before opening a PR

- Diagnose the rule, not just the wording: is it ambiguous, does it conflict with another rule, or does it miss a case? Lead with that in your issue/PR description.
- Keep the change scoped to one rule / one file.
- Match the existing style: short, imperative sentences, no filler.

## Commits

Follow [`Docs/COMMIT.md`](Docs/COMMIT.md):

- Conventional Commits format (`type(scope): subject`).
- Never include a `Co-Authored-By` trailer.

## Pull requests

- One logical change per PR.
- In the description, explain **why** the rule needs to change — the diff already shows *what* changed.

## Checklist

- [ ] Change is scoped to one rule/file
- [ ] Style matches the existing docs
- [ ] Commit message follows `Docs/COMMIT.md`, no `Co-Authored-By`
- [ ] PR description explains *why*
