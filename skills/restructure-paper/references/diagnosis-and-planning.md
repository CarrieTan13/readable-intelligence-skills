# Diagnosis and planning

This file supports Stages 2 and 3 of the workflow in `SKILL.md`. §R4 and §R5 apply from Stage 1 when community feedback or a style example is supplied. The preservation requirements §§P1–P4 in `SKILL.md` take precedence over everything here.

## R1. Comprehensive review and revision plan

Read the entire manuscript before settling on the revision plan. Review every section, appendix, formal statement, and proof; do not sample a few passages and generalize to the rest.

Create a section review record that answers, for each major section:

1. What role does this section play in the main argument?
2. What does the reader need to know before its definitions, construction, or calculations become meaningful?
3. Can the reader identify the intermediate goals and the transitions between proof stages?
4. Are the relevant objects, sampling laws, conditioning, and parameter choices introduced in a usable order?
5. Which explanations are missing, repeated, premature, or separated from their immediate use?
6. What revision will reduce that difficulty, and how will the revised passage be checked?
7. Does each formal statement in the section state its result in the form a specialist would expect (§S6), and which items of the editorial checklist does the section fail?
8. Which entries of the definition, coined-term, and pattern inventories (§R3) arise in this section?

Ground the answers in actual passages. Classify issues as inherited reader difficulties, revision-induced regressions in supplied material, or mathematical/source uncertainty. These categories determine the response: clarify or restructure, restore or remove an obstruction, or preserve and report uncertainty.

Apply the checklist to inherited material as rigorously as to text introduced by revision. Inheritance from the baseline determines the origin recorded in the ledger, not whether an issue is addressed: a problem present in the baseline and still present after revision is an unaddressed finding unless its retention is justified under §§P1–P4.

Review both the overall organization and the local explanations. An existing heading or introductory paragraph is not sufficient evidence that a difficult section is well organized. Identify what readers can understand from it and what they still have to reconstruct themselves.

The plan must identify the consequential improvements across the manuscript before sentence polishing begins. Consider section reorganization, grouping of related constructions, staging of long proofs, parameter explanations, and removal of repeated material. Choose the scale needed for the problem; do not use minimal edit size as the selection criterion.

For a section retained without substantive changes, record a specific reason based on its existing exposition. No change quota applies, but important unresolved reader difficulties must not be concealed by a list of minor improvements.

Maintain an inventory of all formal statements and their proofs, with original and revised locations and dispositions. Track progress by section for a long manuscript. These records support coverage and preservation; they do not belong in the paper.

## R2. Dependencies before restructuring

For every proof, identify its explicit references and the implicit dependencies necessary to follow it. Record significant cross-statement dependencies with the sentence of use and the establishing statement or passage. Distinguish a fact proved earlier within the same proof from a separate lemma that readers must locate elsewhere.

Record actual external theorem applications separately from historical attribution or general discussion of a method. Identify the invoked result and theorem number when the supplied or retrieved material gives them. Absence of a theorem number in a historical citation is not a mathematical gap. Do not invent locators for unread sources.

Use the dependency record to check proposed moves. Explain the argument in an order that makes its goals and constructions intelligible. Do not optimize total reference distance or force every singly used lemma into the same subsection as its application. A forward statement with a clearly located deferred proof is legitimate.

Do not confuse a forward reference, a proof roadmap, or reciprocal exposition with a circular argument. If a genuine proof dependency cycle is suspected, verify the extraction, preserve the affected mathematical content, and record the uncertainty. Do not fix it by inventing a proof.

## R3. Inventories

Keep three inventories in `inventories/`. They make problems that are spread across the manuscript visible as a whole, so that they are fixed everywhere rather than where they happen to be noticed. Build them in Stage 2 by listing entries and locations; decide every entry in Stage 3; apply the decisions in Stage 4; recount and check them in Stage 5; update them after every review round in Stage 6.

Definition inventory. List every object, symbol, and convention that is defined, restated, or confirmed in more than one place, or whose only definition comes after its first substantive use. Find candidates by searching for each defining phrase ("let", "put", "define", "write", "denote", "we call") attached to a symbol or term that appears elsewhere, and by reading section openings and conventions paragraphs. Conventions include rules for how a function or symbol is extended outside its natural domain, uniformity conventions for implied constants, and standing normalizations. For each entry record the defining location and every later place where the same object is defined again, restated, or confirmed to still hold. Decide each later occurrence: remove it; reduce it to a short reminder marked as such ("recall that …") where a nonlocal dependency makes the reminder useful; or record it as a genuinely different object that keeps its own definition. The revised manuscript defines each object once, at or before its first substantive use, and states each convention once. A restatement inside a formal statement may be replaced by a reference to the definition when the statement remains readable on its own (§S6).

Coined-term inventory. List every noun, noun phrase, or classifying adjective that the manuscript uses as a technical term although it is not standard in the field: terms introduced by definition, labels for families of objects, metaphorical labels, and adjectives that sort objects into kinds. For each, record its first definition or the absence of one, its total occurrence count in the baseline and the sections where it occurs, the standard term or short descriptive phrase considered, the decision under §N3 with its reason, and its total occurrence count in the revision.

Pattern inventory. For each pervasive pattern identified under §N5, record the detection method (search terms, sentence openings, or structural signs, together with the sections read in full), the occurrence list with locations, the classes into which the occurrences fall, the decision for each class, and the counts by class before and after revision.

## R4. Supplied community feedback

When community feedback is supplied, track actionable items in the revision ledger. Preserve the supplied record unchanged. For each item, record the commenter and post URL or supplied locator, the paper and version concerned when known, the explicit question or observation, and any separate editorial interpretation. Mark whether evidence comes from a supplied excerpt or an inspected original post. Do not infer that a general comment concerns the assigned paper, or turn a favorable observation into an explicit complaint.

For secondhand feedback, record the original speaker, the intermediary source, the evidence for the attribution, and the manuscript and version actually discussed. Separate quoted remarks from the intermediary's interpretation. If the target is unclear, retain the item as general feedback without attributing it to the assigned paper. Record corrections to mistaken attribution in the derived ledger, preserving the supplied raw record, and revisit any editorial decisions based on that attribution.

Give each item a concrete acceptance criterion: what a reader should be able to understand or locate, and what passage or evidence would answer the question. Record the baseline passage, proposed action, revised passage and version, verification result, and remaining limitation. Distinguish improving the discoverability of an existing answer from supplying a missing explanation. Several comments may share one revision, but retain their individual source links.

Use a separate feedback disposition: `already addressed`, `addressed by revision`, `partly addressed`, `unresolved`, or `outside scope`. These describe the editorial response, alongside the implementation statuses in §W4. Mark an item addressed only when its acceptance criterion is met by a located passage and the applicable checks have passed. Explain partial, unresolved, and outside-scope decisions. A missing reference, an unverified alternative proof, or a question about formalization cannot be resolved through clearer prose alone.

Keep this mapping in the editorial record. It should support a concrete follow-up identifying the observation, what the edition changed or already explains, the exact passage, and what remains unanswered. Claim that the edition addresses an issue; do not claim the commenter agrees or considers it resolved without their response. This workflow never contacts commenters, publishes their records, or fetches linked material. Respect the supplied record's privacy restrictions and the task's access permissions.

## R5. Using a supplied style example

When a successful example is supplied as a style reference, identify the presentation features that help its reader: for example, an early deduction from existing results, a causal explanation of a construction, or a separation of the principal argument from supporting calculations. Compare the mathematical scope before drawing conclusions from length. A shorter example may omit extensions or prove a different result; it never justifies narrowing the assigned manuscript. Transfer useful presentation choices only where they address a located difficulty. Do not mechanically copy its section count, typography, repeated material, provenance text, or other features that conflict with this workflow. A reference example is optional and creates no requirement to retrieve further documents.
