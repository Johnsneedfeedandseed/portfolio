# Using AI and GitHub Copilot in this project

This document summarizes how artificial intelligence (AI) and GitHub Copilot were used to speed up and support development of the scrollytelling portfolio.

## Purpose
A short guide to remember which tasks were delegated to AI/Copilot, how outputs were requested, and what manual checks were applied before accepting changes.

## What we asked AI / Copilot to do
- Generate reusable HTML/CSS fragments (for example `assets/partials/footer.html`).
- Provide examples of responsive `srcset` and optimized image attributes for ImageKit.
- Suggest accessibility improvements: ARIA roles, `aria-label`, tab order, and `prefers-reduced-motion`.
- Draft and polish copy: hero taglines, short bio, project descriptions and concise alt text.
- Create technical checklists: steps for performance (Lighthouse), image optimization, and cross-browser testing.
- Provide prompts and example commands to support the development workflow in VS Code.

## Example prompts used (copy and adapt)
- "Create an HTML `footer` with three centered rows: © 2026 Joaquin Arriola; email `johnsneedbiz@gmail.com`; link to the GitHub repo that opens in a new tab and has an `aria-label` 'Ver proyecto en Github'."
- "Generate an `img` example with `srcset` using ImageKit transforms for 400w, 800w and 1200w and a `sizes` attribute suitable for a gallery grid."
- "Suggest accessibility improvements for a gallery lightbox: focus management, keyboard controls, roles and ARIA attributes."

## Workflow (how to integrate suggestions)
1. Keep `project-brief.md` up to date and reference it in prompts: "See prepared content in project-brief.md." 
2. Request a specific fragment or component from Copilot/AI.
3. Manually review generated code for readability, semantics, accessibility and licensing.
4. Test in the browser (DevTools), run Lighthouse and check CLS/LCP after integrating changes.
5. Iterate and refine based on test results and feedback.

## Best practices and verification
- Data handling: do not send sensitive information to external services.
- Licensing: verify any suggested code snippets to avoid reusing restricted-license material.
- Validation: use linters and validators (`eslint`, HTML validators) and perform manual accessibility testing (keyboard navigation, screen reader).
- Performance: follow the image checklist in `project-brief.md` (srcset, LQIP, width/height or `aspect-ratio`).

## Where generated results live
- Components/partials created with AI are placed in `assets/partials/` (e.g., `footer.html`).
- Content drafts and prompt references are kept in `docs/` and `project-brief.md`.

## Final notes
AI and Copilot are used as assistants to produce drafts of code and copy. Always validate and adapt outputs before publishing to production.
