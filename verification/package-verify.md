# Cognitive Architecture Analysis: urban-prototyping-coach

- Path: `/Volumes/Extend/lecture-works/프로토타이핑/lectureguide/urban-prototyping-coach/SKILL.md`
- Profile: `generate-skill`
- Topology class: `unknown`
- Runtime compatibility: `shared-core only / no-delta`
- Status: `ready`
- Score: 120/120 (100.0%)

## Dimensions

| Dimension | Status | Score |
| --- | --- | ---: |
| Identity and purpose | `pass` | 15/15 |
| Scope and routing boundaries | `pass` | 15/15 |
| Progressive disclosure and package structure | `pass` | 15/15 |
| Evidence, rubric, and measurable outputs | `pass` | 20/20 |
| Execution model and agent workflow | `pass` | 20/20 |
| Validation, portability, and delivery readiness | `pass` | 15/15 |
| generate-skill contract | `pass` | 20/20 |

## Criteria

### Identity and purpose
- `PASS` Has a stable name or H1 title (5/5) - name='urban-prototyping-coach'
- `PASS` States the skill purpose (5/5) - Guide students using the integrated How to build with LLM handout to turn broad sustainable urban-tech ideas into sma...
- `PASS` Provides machine-readable metadata (5/5) - frontmatter_keys=['compatibility', 'description', 'license', 'metadata', 'name']

### Scope and routing boundaries
- `PASS` Defines activation or use conditions (5/5) - matched=['when to use']
- `PASS` Defines boundaries or exclusions (5/5) - matched=['only', 'boundary', 'blocked']
- `PASS` Identifies owner, route, or canonical source (5/5) - matched=['owner', 'route', 'source of truth', 'sot']

### Progressive disclosure and package structure
- `PASS` Links to supporting references (5/5) - references=15
- `PASS` Keeps referenced local assets resolvable (5/5) - local_refs=15, existing=15
- `PASS` Uses staged loading or reusable package surfaces (5/5) - matched=['progressive disclosure', 'scripts/']

### Evidence, rubric, and measurable outputs
- `PASS` Contains a rubric or pass/fail criteria (5/5) - matched=['rubric', 'must', 'should', 'score']
- `PASS` Requires evidence, sources, or citations (5/5) - matched=['evidence', 'source', 'provenance']
- `PASS` Has local or external evidence anchors (5/5) - local_refs=True, external_refs=False
- `PASS` Defines measurable outputs or artifacts (5/5) - matched=['json', 'report', 'artifact', 'output', 'path']

### Execution model and agent workflow
- `PASS` Defines a loop or staged process (5/5) - matched=['score', 'observe', 'act']
- `PASS` Explains tools, scripts, or calls (5/5) - matched=['script', 'command', 'selection', 'runtime']
- `PASS` Accounts for context, memory, or state (5/5) - matched=['context', 'memory', 'state', 'history', 'session']
- `PASS` Defines failure, fallback, or safety handling (5/5) - matched=['blocked', 'fallback', 'credential', 'permission']

### Validation, portability, and delivery readiness
- `PASS` Names validation tests or checks (4/4) - matched=['quick_validate', 'preflight', 'quality gate']
- `PASS` Includes runnable command evidence (4/4) - command_like=True
- `PASS` Avoids relying only on absolute local paths (3/3) - absolute_refs=3, relative_refs=12
- `PASS` Mentions delivery, maintenance, or change tracking (4/4) - matched=['history', 'release', 'package']

### generate-skill contract
- `PASS` Contains canonical generate-skill sections (5/5) - missing_sections=[]
- `PASS` Locks section names in rubric or quality gate text (5/5) - missing_locks=[]
- `PASS` Declares one runtime compatibility closeout state (5/5) - runtime_compatibility_status=shared-core only / no-delta
- `PASS` Includes portable metadata vocabulary (5/5) - missing_metadata_terms=[]

## Findings

No blocking findings.

## Validator Evidence

- `passed` skills-ref validate: `skills-ref validate /Volumes/Extend/lecture-works/프로토타이핑/lectureguide/urban-prototyping-coach` - Valid skill: /Volumes/Extend/lecture-works/프로토타이핑/lectureguide/urban-prototyping-coach
- `passed` quick_validate.py: `python3 /Volumes/Extend/.codex-relocated/skills/generate-skill/scripts/quick_validate.py /Volumes/Extend/lecture-works/프로토타이핑/lectureguide/urban-prototyping-coach` - Skill is valid!
- `passed` audit_three_layer_separation.py: `python3 /Volumes/Extend/.codex-relocated/skills/generate-skill/scripts/audit_three_layer_separation.py /Volumes/Extend/lecture-works/프로토타이핑/lectureguide/urban-prototyping-coach` - [audit] /Volumes/Extend/lecture-works/프로토타이핑/lectureguide/urban-prototyping-coach/SKILL.md
