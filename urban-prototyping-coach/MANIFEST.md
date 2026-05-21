# Manifest

- build_date: 2026-05-21
- package_type: plain Markdown distribution
- publishable_sot_path: `dist/urban-prototyping-coach/`
- source_documents:
  - `ai-pretotyping-gemini-cli-student-guide-ko.md`
  - `How to build with LLM.md`
- companion_skill: `SKILL.md`
- owner: lecture-works prototyping course package
- license: internal course distribution; confirm before public redistribution
- dependencies: none
- backend_required: no
- build_required: no
- runtime_targets: ChatGPT, Claude, Claude Code, generic manual fallback

## Files

- `README.md`: package entrypoint
- `pretotyping-guide.md`: plain Markdown student handout for pretotyping with prompt examples included
- `student-guide.md`: plain Markdown student handout for prototyping and design transition with prompt examples included
- `SKILL.md`: companion AI skill file aligned to `student-guide.md` and specialized for sustainable urban tech
- `domain-alignment-map.md`: compact alignment note for source, domain, and ownership boundaries
- `multi-skill-system.md`: owner/helper routing surface for the package-level multi-skill system
- `MANIFEST.md`: this manifest

## Source Mapping

- `ai-pretotyping-gemini-cli-student-guide-ko.md` -> `pretotyping-guide.md`
- `How to build with LLM.md` -> `student-guide.md`

## Distribution Notes

- Pretotyping guide is preserved as a reference document, but the integrated student-facing main guide is `student-guide.md`.
- The prompt examples are intentionally kept in the student-facing Markdown documents.
- `SKILL.md` uses `student-guide.md` as the primary working frame, adds a sustainable urban-tech domain adapter, and treats `pretotyping-guide.md` as reference only.
- `domain-alignment-map.md` records how `generate-skill`, `vector-language-cognition`, and `cogarch` shaped the current package.
- `multi-skill-system.md` defines how `urban-prototyping-coach`, `cogarch`, `vector-language-cognition`, and `generate-skill` divide owner/helper responsibility.
- runtime use follows one shared portable core: ChatGPT, Claude, and Claude Code read the same `SKILL.md`; generic chat surfaces use the documented manual fallback.
- This folder can be distributed as-is.
- Runtime compatibility closeout is recorded in `SKILL.md` as shared portable Markdown with no runtime-local delta.

## Verification

- source parity: `student-guide.md` matches `How to build with LLM.md`
- source parity: `pretotyping-guide.md` matches `ai-pretotyping-gemini-cli-student-guide-ko.md`
- skill validation: `skills-ref validate dist/urban-prototyping-coach/` passed
- plain Markdown check: no HTML wrapper tags detected in the distribution folder
- 2026-05-21 hardening verification: `skills-ref validate .` passed
- 2026-05-21 hardening verification: `quick_validate.py .` passed
- 2026-05-21 CAA generate-skill profile: ready, 120/120, runtime compatibility `shared-core only / no-delta`, no blocking findings
- 2026-05-21 three-layer audit: fixed/flexible/decisional signals present, smells 0
- 2026-05-21 multi-skill system verification: `skills-ref validate .` passed after system-surface additions
- 2026-05-21 multi-skill system verification: `quick_validate.py .` passed after system-surface additions
- 2026-05-21 multi-skill system verification: `skillanalysis analyze ./SKILL.md --profile generate-skill --run-validators` returned ready, 120/120
- 2026-05-21 multi-skill system verification: `audit_three_layer_separation.py .` reported fixed/flexible/decisional signals present, smells 0

## Validation Commands

Run from this folder:

```bash
skills-ref validate .
python3 /Volumes/Extend/.codex-relocated/skills/generate-skill/scripts/quick_validate.py .
PYTHONPATH=/Volumes/Extend/labs/SkillAnalysis/src python3 -m skillanalysis analyze ./SKILL.md --profile generate-skill --run-validators
```

## Change History

- 2026-05-21: generate-skill / CAA hardening pass added portable metadata, source-of-truth contract, runtime compatibility closeout, legacy distillation owner split, conflict resolution, Fixed/Flexible/Decisional layering, self-application gates, and runnable validation commands. Pattern repetition count: N=1 for this package-local hardening pattern.
- 2026-05-21: generate-skill + vector-language-cognition + cogarch alignment pass specialized the companion skill for sustainable urban tech, added actor-first/evidence-boundary rules, and added `domain-alignment-map.md` for source and ownership traceability.
- 2026-05-21: multi-skill system pass added `multi-skill-system.md`, fixed visible owner/helper routing, and promoted the package from a single companion skill to a package-level orchestration surface.
- 2026-05-21: runtime surface pass added explicit `ChatGPT / Claude / Claude Code` compatibility wording while keeping `shared-core only / no-delta` closeout and no runtime-local adapter files.
