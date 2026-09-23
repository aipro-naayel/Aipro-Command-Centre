---
name: Static site editing
applyTo: "**/*.html,**/*.css,**/*.js"
description: "Use when editing this static site: preserve the no-build architecture, responsive behavior, accessibility, and validation workflow."
---

# Static site rules

- Preserve the no-build, dependency-free architecture unless the task explicitly asks for a new toolchain.
- Keep both pages usable at narrow and wide viewports. Check layout changes at approximately 375px and 1280px wide.
- Preserve semantic HTML, visible keyboard focus, descriptive link text, document language, and meaningful page titles and descriptions.
- Keep JavaScript progressive: the page should remain readable and navigable when scripting is unavailable.
- Reuse the existing design tokens and visual language before introducing new colors or type styles.
- Keep edits focused. Do not duplicate a shared behavior when a small, local change is enough.
- After editing, format the changed HTML/CSS/JavaScript and run the static checks described in `.github/skills/static-site-workflow/SKILL.md`.
