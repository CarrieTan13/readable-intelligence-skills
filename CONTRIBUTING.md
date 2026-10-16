# Contributing

We welcome new paper-reading skills, improvements to the current skill, and corrections to the demo papers. Submit a GitHub pull request instead of uploading a skill to the website.

## Submit a proposal

1. Fork this repository and create a branch.
2. Edit the relevant Markdown files under `skills/restructure-paper/`, or add a new folder under `skills/<your-skill-name>/` containing `SKILL.md` and any supporting references.
3. In `SKILL.md`, include YAML front matter with `name` and `description`, then explain the intended readers, required inputs, workflow, expected outputs, and limitations. Keep references relative and include only files needed by the skill.
4. Describe the change and provide a short before/after example showing how it improves understanding while preserving the mathematics. You may use one of the demos.
5. Open a pull request against `main`. Disclose any scripts, external services, or tools required, and document their purpose. Do not include credentials, personal reader data, executables, or papers you cannot redistribute.

For a new skill, state its license and authorship. For changes to an existing skill, explain any licensing changes rather than replacing attribution. Contributions involving papers must include provenance, redistribution terms, and a clear description of changes. Do not edit original PDFs to make a correction; add a separately identified revision.

## Review and publication

A maintainer checks relevance, clarity, file structure, provenance, and mathematical preservation, and tries the proposed workflow on a representative example before accepting it. Format checks alone cannot establish that a skill is useful or that a proof is correct. Submitted instructions and scripts are reviewed before execution.

After review, a maintainer merges accepted changes. Publication on readable-intelligence.com is a separate curated release:

1. Review the final skill files and regenerate the downloadable ZIP from those exact files, preserving the `restructure-paper/` top-level folder for the current skill.
2. Verify that the ZIP matches the published sources; for changed PDFs, update SHA-256 values and provenance in `demos/manifest.json`.
3. In the website repository, update `public/skills/readable-v4.zip` (or add a versioned artifact), add approved new skills to the Skills page, and deploy the website.
4. Verify the live download and record the published repository commit in the release notes.

Only maintainer-approved releases are listed on the website. Existing uploads are not automatically promoted to the public Skills page.
