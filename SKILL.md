---
name: fpf
description: Apply the pinned First Principles Framework (FPF) ecosystem to a real project question. Use for FPF or pattern-ID requests and for substantial engineering, learning, research, architecture, operations, strategy, decision, evidence, method, or cross-domain questions where the user wants FPF-guided help. Read the relevant Core and domain patterns from the skill snapshot, using the project's own context and evidence.
---

# FPF - First Principles Framework

FPF Library supplies connected methods for engineering, research, learning, management, and mixed human/AI work. The complete pinned publication set is under `spec/`. Its source revision is in `spec/VERSION` and `spec/SOURCE.json`. This is a deliberate snapshot: normal use neither checks upstream nor changes it.

**First read `spec/USING-FPF.md`** when applying the framework. Do not load the huge Core file wholesale; retrieve its relevant sections. `spec/Readme.md` introduces the Library. `spec/DPFs/README.md` locates four Suites and standalone frameworks. `spec/FPF-LIBRARY-REFERENCE.md` explains their architecture and document identities. Suite READMEs and Architectural References explain connected contributions. A locator does not replace a pattern's method and conditions.

## Retrieval

```
SKILL=<this skill's base directory>

$SKILL/bin/fpf cards                 # current Core entries and cards, never a hard-coded list
$SKILL/bin/fpf get SOTA-PORTFOLIO    # one Core entry or card
$SKILL/bin/fpf toc evidence          # Core heading lookup
$SKILL/bin/fpf get A.19.ECS          # one Core pattern
$SKILL/bin/fpf outline E.10          # oversized Core subsections
$SKILL/bin/fpf get E.10:6            # one Core subsection
$SKILL/bin/fpf search 'ClaimGraph'   # search Core, with owning ID
$SKILL/bin/fpf files                 # available snapshotted publications
$SKILL/bin/fpf locate 'release'      # heading lookup across Core and DPFs
$SKILL/bin/fpf search-all 'rollback' # bounded content search across publications
$SKILL/bin/fpf pattern SYSE.35       # one DPF pattern (or its location if oversized)
$SKILL/bin/fpf pattern SYSE.35 --solution # only that DPF's Solution
```

Commands may be run with `python3` if the executable bit is unavailable. Core sections over 50K auto-outline; drill into the needed subsection. For a large DPF pattern, use `--solution` or read the relevant portion at its returned location. Check the pattern's Problem frame before relying on a Solution. `locate` indexes level-2 headings in Core and framework files; use `search-all` or content search for README entries, Architectural References and deeper sections. A returned heading is only a locator.

## Method

1. **Start from the user's project question**, not from FPF topology. Do not ask them to learn pattern IDs first.
   Keep the receiving action or judgement in view, using `C.39:4.1` to establish sufficiency. Reuse an adequate known answer. Follow consequential construction gaps through `C.39:4.2–4.5`, without turning every lookup into framework development.
2. **Use the project's actual context.** Read the relevant files the user identifies or obtain the facts in conversation: subject, intended use, current difficulty, constraints, observations, and decision authority. Do not store private project material in this shared snapshot. Ask only for a missing fact that changes the next truthful result.
3. **Route by the current question.** If a pattern is named, retrieve it directly. Otherwise search the available publications together, including DPFs and Suite References when the question crosses domains. Core ordinary entries and cards are useful routes, not a required gateway or a universal sequence. Compare candidates by Situation, Question, first result, and stop conditions.
4. **Read the selected substantive pattern.** Check its Problem frame, Solution, relevant conditions and dependencies. Inspect only the branch that fits. Follow a connected Reference answer when several contributions must meet. `E.11.PUA` helps apply a selected Solution; `E.11.PUR` is for ordering candidate uses, not every task.
5. **Return the first useful result, or an honest stop.** When its connection to the original question is uncertain, apply `C.39.QR`. Recover the question independently of the proposed answer; establish what the partial result warrants and what work remains. Use `C.39.WA` when the missing contribution is an account of a whole subject and its relations. Stop when the result is sufficient for the requested use.

### Answer order

Give these three first:

- one useful result for the current situation, or an honest stop if no truthful result can yet be given;
- the current project question or action that result answers;
- any exact missing definition, test, rule, case fact, information, or authority needed before a truthful answer is possible.

If that is sufficient and no downstream identity, application, publication, or reliance is current — **stop**. Only when the result's identity, obtaining basis, application, or later reliance changes the claim, add: the selected pattern and Solution, the EntityOfConcern, the exact result kind and the basis on which it obtains, the Method/plan/dated Work/evaluation/decision it answers, and the relation or binding that makes it a result for that object.

### Discipline

- A document label, familiar phrase, file, diagram, ticket, or identifier does not make a result truthful. Check it against the selected `Solution`.
- Do not fabricate project-local values or records to fill a pattern's slots. A missing fact is a blocker to report, not a gap to invent.
- Keep comparison conversational. Materialize a record only when a **named** receiving use relies on it.
- Cite a second pattern only when its concrete contribution changes the continuation.
- Do not turn an entry or card into a whole-project plan.
- Prefer plain engineering language. Let pattern names enter only when they make the answer easier to check.
- Cite the publication and PatternID used. Give the pinned revision when freshness or comparison matters. Do not claim the snapshot represents later repo changes.
- Preserve complete PatternIDs and SectionRefs, including suffixes and range endpoints. Resolve document identity through `Library.Reference:11.1` when unclear.
- Distinguish source citations from instructions to apply another method. Follow dependencies only as far as the receiving work requires.

## Starting points across the ecosystem

- Software architecture, build, release, reliability, platform and agent work: `spec/DPFs/Engineering DPF Suite/README.md`, then the relevant DPF. Systems Engineering covers agent execution procedures (`SYSE.47`) and representative-work testing (`SYSE.46`).
- Operations, organization, strategy, goals, workforce, finance, leadership or community work: `spec/DPFs/Management DPF Suite/README.md` and its current publication table. Goal construction and OKR/CFR questions route to GOALS, including human professional goals (`GOALS.6`) and AI work (`GOALS.7`). Hiring, reward, employee voice, protection and participation route to HRM.
- Human learning and capability change: `spec/DPFs/Human Capability Engineering DPF Suite/README.md`. Obtaining a result through help does not establish learning. Do not transfer human learning methods unchanged to AI agents.
- Algorithmic, mathematical, physical, modeling, or notation questions: `spec/DPFs/Foundational Thinking DPF Suite/README.md` and Reference, then the relevant DPF.
- Research, decision design, explanation, narrative and other standalone fields: `spec/DPFs/README.md`, then the supplying framework under `spec/DPFs/`.
- Method construction and open-ended development: Core `C.39` and `C.40.OD`, with actual domain methods. A completed task alone does not establish continuing development.
- Thinking operations connected to work, learning and further development: `spec/FPF-LIBRARY-REFERENCE.md`, `Library.Reference:9.4`. Select the missing contribution; the repertoire is not a required sequence.
- Kata process improvement: Core `E.23:4.4.1` (level-5 heading, not indexed; read it via `fpf get E.23:4.4`). Coaching that reasoning: `HCD.9:4.10`. Use `Library.Reference:6.5.3.4` when process improvement, coaching and organizational support must connect.
- Shared distinctions about claims, evidence, methods, work, decisions, and language: Core `cards`, `toc`, or `search`. A single DPF pattern may suffice; do not force a Core card first.

The current Core entries are generated from the edition with `fpf cards`; Suite members and connected questions are in the snapshotted READMEs and References. These change between editions, so do not treat older lists or IDs as authoritative.

## Boundaries

- FPF Core is upstream. A project's own ontology or framework depends on FPF; never rewrite Core to match local practice (`E.5.3` Unidirectional Dependency).
- "LPF" is not a separate artifact. The spec says *local practice framework*, authored through the same `E.4.DPF` pattern as a domain framework.
- Authoring a DPF/LPF is not a starting move. Route it through `SOTA-PORTFOLIO`: try cheaper reuse or a contribution first, open a framework decision (`E.4.PFAD`) only for a recurring unmet problem, and stop at the first adequate maintained or one-off result. A source pack or proposal is not a framework by appearance.
- FPF is too heavy when the task is small, feedback is fast and cheap, vocabulary is stable, and the decision will not be reused or audited. Say so rather than applying it.

## Refreshing the pinned snapshot

Only on an explicit request to update the skill, run `python3 $SKILL/bin/fpf-refresh --source PATH` (or set `FPF_SOURCE`). PATH is a clean local checkout of `https://github.com/ailev/FPF`; ask the user for it if neither is given. It never pulls from the network, and `--allow-dirty` deliberately snapshots uncommitted files (recorded as dirty). It copies the tracked public publications, writes source revision and file hashes to `spec/SOURCE.json`, rebuilds the Core and ecosystem heading indexes in staging, and replaces the snapshot only after indexing succeeds. Do not manually copy only Core; its DPF dependencies and `USING-FPF.md` must travel with it.

After a refresh, run `fpf cards`, `fpf locate` and `fpf pattern` on representative Core, engineering, management, human-capability, foundational and narrative questions. Verify that `DPFs/`, all four Suites, standalone frameworks and the Library Reference were copied. Compare the changed READMEs, entry/card set and named routes with this SKILL.md. Repair stale routing prose or tool assumptions; an index rebuild does not validate semantic changes. If the source checkout moves or is unavailable, ordinary work still uses the pinned snapshot. A question that explicitly requires newer upstream guidance needs an accessible newer edition or an honest freshness limit.
