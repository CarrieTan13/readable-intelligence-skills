# Prose and notation

This file supports Stages 2–4 of the workflow in `SKILL.md`. The preservation requirements §§P1–P4 in `SKILL.md` take precedence over everything here.

## N1. Scientific prose

Write in the manuscript's effective scientific voice. Explain what a construction accomplishes, why a calculation is needed, and how one stage enables the next. Prefer concrete mathematical relations over procedural narration about the document.

Preserve the existing document class, global fonts, theorem-heading styles, table rules, and related preamble settings by default. Allow only the smallest change needed to repair a located compilation, existing-functionality, or layout defect; record the reason and inspect the affected output. The cross-reference style change permitted in §N4 is also allowed. For PDF reconstruction, first match the original presentation, then apply the same constraint.

Unpack sentences and noun phrases that carry several independent conditions or operations. Necessary qualifiers may be clear individually yet hard to attach to the right object when stacked together. Prefer a named subject and a direct verb; separate the setting, action, and consequence where this clarifies their relation. For example, “the retained normalized conditional measure” can become “Restrict the measure to the retained event, then normalize it,” only when that is the actual order of operations. Preserve each qualifier's scope, quantifier order, and logical connection. Neither sentence length nor the number of modifiers is by itself a defect.

Use natural transitions. Remove formulaic announcements such as “This section introduces no separate theorem” when they provide no mathematical orientation. Do not require a sentence between every pair of formal environments. Retain a transition that explains a genuine change of goal or assumptions.

Use technical language precisely, and introduce terminology when it serves a recurring or mathematically meaningful purpose. Do not invent long labels or new names for existing proof steps. Do not use bold paragraph labels as the default prose structure; use appropriate headings or topic sentences. Formal Remarks, Examples, and Proof sketches can retain their established form when useful.

Remove duplication at the level of paragraphs and sections as well as sentences. Keep each explanation where it does useful work, and retain short reminders when a nonlocal dependency makes them necessary. Length can increase when the added explanation materially helps the reader; every substantial addition should have an identifiable purpose. Do not impose a compression percentage or an expansion allowance.

Do not use “clearly,” “obviously,” or similar assurances in added text in place of an explanation. Avoid defensive contrast templates such as “not merely” or “X is not Y; it is Z” unless a specific misconception requires correction.

Remove disclaimers of what is not assumed, used, imposed, required, or claimed unless a reader would otherwise draw a specific false inference that matters later; in that case state the positive fact once, where the inference would arise. Do not repeat that a convention fixed earlier still holds. A sentence that answers an objection the text never raises is review-response residue: fold its substance into a hypothesis, into a remark explaining why a condition is needed, or into the proof, and remove the rest. These deletions do not apply to negations and restrictions that are part of the mathematics (§P2).

Write proofs as mathematical arguments, not as instruction lists. A run of imperatives ("Apply …. Sum …. Only now interchange ….") hides what each step establishes; state the relation obtained and the reason it holds. Imperatives that introduce objects or fix choices, such as "Let", "Fix", "Define", "Put", "Set", "Write", "Choose", "Consider", and "Denote", remain appropriate and are not changed. The target is imperatives that perform reasoning steps, such as "Apply", "Insert", "Sum", "Interchange", "Enlarge", and "Bound", without stating what the step establishes. Where the order of choices matters, state it once explicitly, through quantifiers, a short list, or a dedicated passage of the proof, and refer to that statement rather than scattering "before … is chosen" remarks through the text.

Replace accounting metaphors ("costs", "budget", "spends", "allowance", "leaves room") with the inequality they abbreviate, unless the metaphor is defined once and recurs usefully. Do not use adjectives as informal type markers ("the true sum", "the honest identity", "the naive bound") to distinguish objects; name the objects or state the distinction. When a convention already fixes a qualifier, such as the independence of data from the main parameter or the dependence of implied constants, do not repeat it: a qualifier such as "fixed", "exact", "precise", or "uniform" should carry information that the conventions do not already supply. Explain the role of each consequential numerical constant under §S2. When any of the patterns in this section occurs throughout the manuscript, handle it under §N5.

The manuscript must read as a scientific paper. Keep edition banners, references to the supplied PDF, editorial “Original” references, renaming commentary, access limitations, workflow compliance claims, and `[NEEDS-EXPERT]` markers out of its title, abstract, body, captions, and footnotes. Editorial provenance and uncertainty belong in the report. This rule does not require deleting a legitimate mathematical use of the ordinary word “original.”

## N2. Notation: purpose, economy, and clarity

Review notation throughout the manuscript, including definitions, statements, proofs, figures, and appendices. Assess whether each name helps readers understand or follow the argument. Define objects before substantive use and make their scope clear. Preserve conventional forward references when they are understandable.

When a symbol merely abbreviates a simple expression used once or twice, consider substituting the expression directly. Evaluate the resulting passage: substitution should reduce lookup work without making formulas longer or harder to read. Retain names that identify meaningful objects, expose dependencies, or organize a substantial calculation, even when used infrequently. Do not introduce a one-use alias solely to make an explanation look formal.

Eliminate every notation alias that the manuscript itself declares, under the rule in §P1. Look for chains of aliases, temporary renamings, and parameters introduced only to be immediately specialized. Prefer the existing expression or symbol when an additional name provides no explanatory benefit. Preserve distinctions between objects that have different types, domains, distributions, or roles. A parameter specialization must not narrow a statement's scope or suppress a dependency needed elsewhere.

When many distinct symbols are genuinely needed in one passage, group them by role: the quantity being controlled, the parameters governing the construction, and the auxiliary bounds needed for verification. Introduce each group near its use and keep the decisive relation visible. A local explanation or small role table can reduce repeated lookups; a compulsory global glossary cannot substitute for readable exposition. Preserve all quantitative conditions, even when their verification is moved to a supporting passage. The goal is to make the groups understandable, not to rename every symbol or hide dependencies.

At introduction, explain what a central symbol represents and why it is needed. For several related parameters, make their roles and order of choice explicit. Prefer short local reminders to repeated definitions or a large compulsory notation table.

Avoid using the same letter for unrelated objects within the same argument when that makes formulas difficult to scan. Treat distinctions of font or decoration as part of symbol identity under §P1; do not collapse them for visual uniformity. Preserve conventional notation and clear reuse across separate scopes; do not require globally unique symbols.

Check what each subscript, superscript, prime, tilde, or other decoration distinguishes, and preserve that distinction. Any change must satisfy §P1; visual simplification alone does not permit removing a decoration.

For every simplification or renaming, inspect all affected occurrences, including statements, displays, captions, and later references. Preserve binding, scope, types, conditioning, parameter dependencies, and mathematical meaning. Prevent variable capture or collisions with other symbols. Record consequential notation changes and their affected scope in the editorial report. Retain the original notation when equivalence or scope is uncertain, and record the uncertainty separately.

Do not optimize the number of symbols. Judge the revised passage by how much information readers must remember and how readily they can reconstruct the argument. Apply the preservation boundary in §P1; notation refinement does not permit deleting a formal definition or proof-critical distinction.

## N3. Terminology

Prefer established terminology. Decide every entry of the coined-term inventory (§R3) by the following rules, applied in order, and record the decision and reason.

1. If a standard term of the field denotes the same object, use the standard term.
2. Otherwise, if a descriptive phrase of a few words conveys the object at its occurrences without making sentences or formulas substantially harder to read, use the phrase.
3. Otherwise keep the coinage only if it names a mathematical object rather than a metaphor or an informal classification, is defined in one sentence at its first use, and is used repeatedly.
4. A label borrowed from everyday language, for example calling an auxiliary index set "lanes" or a lower bound a "beacon", is replaced unless rule 3 holds and no literal description is short enough to use. A classifying adjective that sorts objects informally ("true", "honest", "naive") is replaced by a named object or a stated property.

Assess the cumulative burden as well as each term. When more than about ten coinages remain after these rules, apply rules 1 and 2 again to each retained term and keep only those whose replacement would materially lengthen the exposition. Coined terms in section titles, statement titles, the abstract, and the introduction are replaced there, or explained where they appear, because readers meet them before any definition.

New and rewritten text uses the decided terms and introduces no new coinages. In the revision, the occurrence count of a retained coinage rises only through relocation of existing text or through new explanatory text that refers to an object the term already names; record any increase with its cause. Treat every replacement as a terminology change under §P3 and apply it to every occurrence, including titles, captions, and the introduction.

## N4. Front matter, bibliography, numbering, and cross-references

Give the paper a title distinct from the titles of its parts. Keep existing classification codes and keywords. When they are absent, add Mathematics Subject Classification 2020 codes, one primary and any secondary, and a few keywords, determined from the main theorem and the principal methods; record the choice. Do not invent other venue requirements.

Bibliography entries contain bibliographic data only. Remove notes about how a source was accessed ("author's copy", "publisher PDF", "version consulted") and record that information in the editorial report. Give each identifier once per entry, use one consistent format across entries, and prefer a stable bibliographic reference to an internal release code or a search-result URL when the stable reference identifies the same work and version. A standard fact should be cited to a standard source. When the manuscript cites a tangential source for one, change the citation to a standard source already in the bibliography whose statement has been checked, or to a new source only under the verification rule of §P3; otherwise keep the citation and record the issue. Cite scholarly sources rather than web pages for mathematical claims, including claims about the status of a problem. The bibliography lists exactly the cited works: remove every entry that the delivered manuscript does not cite, including an entry whose only citation was removed during revision, and record each removal. Check that every citation resolves to an entry.

Use one cross-reference style throughout. If the manuscript mixes styles, adopt bare parenthesized numbers for displays and the type with its number for results. In mathematics the usual forms are a bare parenthesized number, as in "by (3.2)", or a lowercase "equation (3.2)"; avoid a capitalized "Equation (3.2)" in mid-sentence, and avoid starting a sentence with a bare equation number. Configuring the cross-reference package to print the chosen form is a permitted preamble change; record it and inspect the affected output. Use one numbering scheme for displays. Local tags such as (I) or (★) are acceptable only within a single proof and are not referenced from elsewhere. Keep the reference macros and hyperlink requirements of §P3.

Number formal statements in one consecutive scheme, per section or per document as the manuscript already does. Split parts and promoted lemmas receive ordinary numbers under §P3; letter suffixes, primes, and "bis" numbers do not appear in the delivered manuscript.

## N5. Pervasive patterns

A pattern is pervasive when it occurs at least about ten times, or in at least three sections. Typical pervasive patterns are redundant qualifiers, proofs written as instruction lists, accounting metaphors, disclaimers of non-use, repeated reassurances about a convention, coined terms, informal type markers, and a nonstandard cross-reference style. Address a pervasive pattern across the whole manuscript, not at the locations where it happened to be noticed or reported.

Steps 1 and 2 belong to Stages 2 and 3, step 3 to Stage 4, and step 4 to Stage 5; after each review round, steps 3 and 4 are repeated for every pervasive finding.

1. Detect. Define search terms, sentence openings, or structural signs for the pattern, and also read the sections where it is frequent in full, since searches miss variants. Record the occurrence list with locations in the pattern inventory (§R3).
2. Classify. Sort the occurrences by function. For a qualifier, for example, separate occurrences that carry information the conventions do not supply, occurrences made redundant by a stated convention, and occurrences that are part of a mathematical restriction protected by §P2. When occurrences are redundant only because of an unstated convention, state that convention once at its natural place, then treat them as redundant.
3. Act by class. Give each class one decision with a reason, edit every occurrence in the classes to be changed, and keep the others. Apply §§P1–P2 to every edit; an occurrence whose meaning is uncertain is kept and recorded individually.
4. Measure. Recount by class in the revision and record the counts. A pervasive finding is `fixed` only when every occurrence in a class to be changed has been changed or individually recorded as kept, and the counts before and after appear in the pattern inventory.

Rewriting proofs that read as instruction lists is pervasive work of this kind. Rewrite each such run so that every sentence states what its step establishes and why it holds, keeping every step, case, and justification. Do not limit the rewriting to representative passages. A change made under this section is protected by the tie rule of §V2.
