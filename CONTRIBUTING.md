# Contributing a style skill

Create one directory under `skills/` using a lowercase kebab-case name. Every skill must include a `SKILL.md` with frontmatter containing `name` and `description`, followed by guidance that covers:

- scope and priority rules;
- how to shape prompts for the style;
- downstream integration boundaries;
- a concise reusable output contract.

Keep the style layer independent from model selection and credentials. Add references only when they are needed for structured output, video adaptation, or another clearly scoped concern. Update the root README when adding a skill, and check that all links resolve from the repository root.
