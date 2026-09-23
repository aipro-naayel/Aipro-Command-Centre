---
name: static-site-workflow
description: "Use when building, reviewing, or debugging this dependency-free static site, especially before previewing or publishing HTML, CSS, or JavaScript changes."
---

# Static site workflow

Use this workflow for changes to `index.html`, `project.html`, or future static assets.

## Inspect

- Identify the page, section, and user-visible behavior being changed.
- Check both pages for shared navigation, responsive rules, metadata, and repeated design tokens.
- Preserve the current no-build architecture unless a build step is explicitly requested.

## Edit

- Prefer semantic HTML and small, local CSS or JavaScript changes.
- Keep keyboard navigation, focus states, color contrast, and mobile layout intact.
- Keep links valid and external links safe with an appropriate `rel` value.
- Avoid adding dependencies for behavior that can remain native to the browser.

## Validate

Run the cheapest checks that match the change:

```sh
npx --yes prettier --check index.html project.html
npx --yes htmlhint index.html project.html
```

For a visual check, use the recommended Live Server extension and open the changed page with **Go Live**. Check a narrow viewport around 375px and a desktop viewport around 1280px. Confirm that navigation anchors, external links, filtering or other interactions, and focus styles still work.

If `npx` is unavailable or the network is blocked, use the editor's Prettier and HTMLHint diagnostics and report that command-line validation was unavailable.

## Finish

- Re-check the diff for accidental formatting churn.
- Mention any remaining limitation, such as behavior that needs a real browser check.
