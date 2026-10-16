# Independent checklist reviewer

This file defines the independent checklist review run in Stage 6 of the workflow in `SKILL.md`. The editor follows the configuration, input, batching, disposition, and round rules below and supplies the reviewer instructions at the end to every reviewer invocation. The reviewer receives no other part of the skill except `references/editorial-checklist.md`.

## Configuration

The review is performed by a subagent running model `GPT-6.1-Sol` at reasoning effort `medium`. Use exactly this configuration for every invocation in every round, including batch and aggregation invocations. Do not substitute another model or effort level, and do not let the editing agent, or any agent that has seen the editing context, act as the reviewer.

If this configuration cannot be invoked in the environment, record the failure and its cause in `checklist-review/`, run a self-review that follows this entire protocol with the same checklist, label every resulting file as a self-review, report at delivery that independent review did not occur, and continue the workflow. A self-review never counts as independent review.

## Inputs and independence

Start every invocation in a fresh context. In the first round, supply only:

1. the authoritative baseline manuscript (PDF, and source when available);
2. the revised manuscript (built PDF and source; when no build is available, the source alone, and the reviewer then gives locations by section and statement number);
3. `references/editorial-checklist.md`, verbatim;
4. the reviewer instructions at the end of this file, with the bracketed fields completed;
5. for batch invocations, the global-pass report of the same round.

Do not supply the revision ledger, change report, statement inventory, editing history, or the editor's reasons before the reviewer's first-round verdicts. In later rounds, also supply the reviewer's previous reports, the editor's disposition table, and, for each pervasive finding marked `fixed`, the corresponding pattern-inventory entry (detection method, classes, decisions, and counts). These are records of what was changed, which the reviewer needs to verify extent; they are not the editor's arguments for retaining text.

The reviewer reads only the supplied files and writes only its own report files in `checklist-review/`. It does not edit the manuscript, access the network, or contact anyone. Invoking the reviewer grants it no other permission.

## Batching and coverage

Every round consists of a global pass, section passes, and an aggregation.

The global pass is one invocation. It covers the title, abstract, introduction, overall section structure and titles, numbering of formal statements, terminology across the whole manuscript (including its own list of coined terms with approximate counts per section), definitions and conventions repeated across sections, cross-reference style, and the bibliography, including whether every entry is cited and every citation resolves. It writes `checklist-review/round-N/global.md`.

Section passes apply every checklist item to every page of their batch. When the revised manuscript has at most 30 pages, one invocation covers all sections. Otherwise form batches of whole sections, in order, with at most 25 pages each; a section longer than 25 pages is divided at subsection boundaries, and a subsection longer than 25 pages at page boundaries. Each batch invocation receives the global-pass report and writes `checklist-review/round-N/batch-K.md`, stating the exact pages and sections examined.

The aggregation is one invocation that receives all reports of the round. It merges them into `checklist-review/round-N/summary.md`: it consolidates findings that describe the same pattern into one pervasive finding, assigns final IDs, and produces the coverage table. It checks that the pages examined by the batches together cover the whole revised manuscript; any uncovered page range is reported, and the editor reruns a batch for it in the same round before acting on the round's findings.

## Findings

Each finding records an ID of the form `R<round>-<number>`, the checklist item, the location (section, statement number, and page), an excerpt of at most two lines, the origin (inherited, introduced, or worsened, by comparison with the baseline), the severity, the problem, and a suggested type of remedy with any preservation risk the reviewer sees.

Severity is `blocking` for a formal statement that cannot be read or cited on its own, a pattern affecting a whole section or more, editorial residue or process traces in the manuscript, an uncited bibliography entry or unresolved citation, nonstandard statement numbering, or a suspected preservation regression; `major` for a local issue that materially slows an expert reader; and `minor` otherwise.

A pattern that occurs at least about ten times, or in at least three sections, is reported once as a pervasive finding. It states the detection method (search terms, sentence openings, or structural signs, and the sections read in full), at least three locations in different sections, and an estimate of the number of occurrences. The detection method must be specific enough for the editor and later rounds to recount.

As a secondary task, the reviewer flags suspected preservation regressions it notices in changed passages, such as a dropped hypothesis, a changed quantifier, a lost case, or a citation of a split statement that points to the wrong part. These flags do not replace the editor's preservation checks, and the reviewer does not claim a full preservation audit.

The summary ends with a table giving, for every checklist item, `findings`, `clear` with the scope examined, or `not applicable` with a reason. Frequency counts may locate candidates but are not findings by themselves.

## Dispositions

For each finding, the editor records `fixed` with the revised location, `rejected` with a specific reason, or `unresolved` with the limitation and the next action. The only acceptable reasons for rejection are a conflict with the preservation requirements of `SKILL.md` that no permitted remedy avoids, or evidence that the finding is mistaken. Inheritance from the baseline, the effort required, the number of occurrences, and the length of the affected passage are not reasons. A pervasive finding may be marked `fixed` only when its pattern-inventory entry shows every occurrence of the classes to be changed as changed or individually recorded as kept, with counts by class before and after revision. Every fix passes through Stage 5 and a local reader comparison under §V2 before the next round.

## Later rounds

In each later round, the reviewer:

1. verifies every non-pervasive fix in context and re-examines the surrounding passages for new problems;
2. for every pervasive finding marked `fixed`, recounts the occurrences in the whole revised manuscript with the recorded detection method and compares the result with the editor's counts; then inspects a sample of the remaining occurrences: ten, or five percent of them if that is larger, but at most fifty (all of them if fewer than ten), drawn from at least three sections and excluding the locations reported earlier; the fix fails if the recount disagrees materially with the editor's counts or if the sample contains an occurrence of a class the editor decided to change;
3. assesses whether each rejection gives an acceptable reason;
4. applies the checklist to all new or substantially rewritten text and reports new findings.

Every later round again uses the global pass, batches, and aggregation described above, restricted to the changed pages plus the pages needed for the recounts and samples; the global pass is repeated in full.

Run rounds until no blocking finding remains open and no fix is reported as failed, up to three rounds. Every finding still open after the last round is reported in the change report with its disposition.

## Reviewer instructions

Supply the following text to every reviewer invocation together with the inputs above, completing the bracketed fields:

```text
You are an independent reviewer of a revised mathematics manuscript. You did not
write the revision and you have not seen the editor's reasons. Using the attached
editorial checklist, find writing and presentation problems in the revised
manuscript.

Inputs: baseline manuscript [paths]; revised manuscript [paths]; editorial
checklist [path]; round [N]; invocation [global pass | batch K: pages ... and
sections ... | aggregation]; [batches: the global-pass report]; [aggregation:
all reports of this round]; [later rounds: your previous reports, the editor's
disposition table, and the pattern-inventory entries of pervasive fixes].

Rules:
1. Examine every page assigned to this invocation: front matter, sections,
   appendices, formal statements, proofs, and bibliography as applicable.
   State exactly which pages and sections you examined.
2. Apply every checklist item. Its "Addressed when" sentence is the complete
   criterion. Inherited problems count; label each finding inherited,
   introduced, or worsened by comparing with the baseline.
3. Ground every finding in a located passage and quote at most two lines.
   Do not rewrite the manuscript; you may suggest the type of remedy.
4. Report a pattern that occurs at least about ten times, or in at least
   three sections, once as a pervasive finding, with a recountable detection
   method, at least three locations in different sections, and an estimate
   of its extent.
5. Flag any suspected change of mathematical content you notice in revised
   passages (hypotheses, quantifiers, cases, constants, citation targets).
   Do not claim to have verified the mathematics.
6. In later rounds: check each fix in context; for each pervasive fix,
   recount with its detection method over the whole manuscript and inspect a
   sample of ten remaining occurrences, or five percent if larger, at most
   fifty, from at least three sections and away from earlier locations;
   check each rejection's reason; then look for new problems in changed text.
7. Do not access the network, edit files, or use material other than the
   inputs. Write only [checklist-review/round-N/<file>.md].

Output: a findings list (ID R[N]-k, checklist item, location, excerpt, origin,
severity blocking/major/minor, problem, suggested remedy type, preservation
risk); for later rounds, a verdict for each earlier finding (fix confirmed,
fix failed with evidence, rejection accepted, rejection disputed); for the
aggregation, a table with one row per checklist item marked findings, clear
(with the scope examined), or not applicable (with a reason), and a coverage
statement listing any page range not examined.
```
