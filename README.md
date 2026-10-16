# Readable Intelligence Skills & Demo Papers

From AI-generated mathematics to human understanding.

This is the public contribution repository for [Readable Intelligence](https://readable-intelligence.com). It contains our current paper-rewriting skill and all five demo papers currently featured on the site.

## Current skill

**Readable Intelligence Skill (Current Version)** reorganizes proof-based mathematics and theoretical computer science papers for research readers while preserving statements and complete arguments.

- [Read the skill](skills/restructure-paper/SKILL.md) and its supporting reference files.
- [Download the current ZIP](downloads/readable-v4.zip), identical to the website download.
- The ZIP extracts to `restructure-paper/`. Follow your AI tool’s instructions for installing a skill; the skill expects a manuscript as input.

## Demo papers

These are the deployed demo PDFs, copied without modification.

| Family | Paper | Original | Readable Version |
| --- | --- | --- | --- |
| 003 | The Quasi-Riemann Hypothesis: A Zero-Free Half-Plane ℜs > 7/8 | [PDF](demos/003/original.pdf) | [PDF](demos/003/readable.pdf) |
| 102 | The Unique Games Theorem | [PDF](demos/102/original.pdf) | [PDF](demos/102/readable.pdf) |
| 074 | Every four-dimensional Kakeya set has full Hausdorff dimension | [PDF](demos/074/original.pdf) | [PDF](demos/074/readable.pdf) |
| 107 | An Upper Bound of 9/4 for the Matrix Multiplication Exponent | [PDF](demos/107/original.pdf) | [PDF](demos/107/readable.pdf) |
| 260 | The spacetime Penrose inequality and enclosing area | [PDF](demos/260/original.pdf) | [PDF](demos/260/readable.pdf) |

See [the manifest](demos/manifest.json) for source revisions and SHA-256 checksums. The complete upstream collection of 722 manuscripts remains at [openai/math](https://github.com/openai/math).

## Contribute through a pull request

Propose a new skill, improve an existing skill, or correct a demo by following [CONTRIBUTING.md](CONTRIBUTING.md). Maintainers review contributions and merge accepted changes before publishing them on the website. Opening or merging a PR does not automatically deploy the site.

## Attribution and licensing

Demo manuscripts retain [Apache-2.0](demos/LICENSE) terms and [attribution](demos/NOTICE). Readable PDFs are modified editions, identified in each demo README. The current skill was supplied without a separate license; this repository does not assign it the license of a different skill. See [LICENSES.md](LICENSES.md) for scope.
