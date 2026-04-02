# rococo_style

A structured design grammar for the **Rococo** style (~1720–1780), encoded as machine-readable data for use with AI art generation, prompt engineering, shader art, and procedural composition tools.

## What's in this repo

| File / Directory | Purpose |
|---|---|
| `STYLE_SPEC.md` | Canonical visual spec — pillars, constraints, QA checklist |
| `MOTIF_DICTIONARY.md` | Human-readable catalog of Rococo motif families |
| `PROMPT_PACK.md` | Ready-to-use prompt scaffolds and best practices |
| `QA_WORKFLOW.md` | Process for verifying AI/shader outputs against Rococo grammar |
| `QA_PATCH_LIBRARY.md` | Common failure patterns and prompt/parameter patches |
| `GAP_ANALYSIS_AND_EXPANSION_PLAN.md` | Tracks missing motifs, palettes, and scene types |
| `TASK_BOARD.md` | Active tasks and to-dos for repo expansion |
| `data/motifs.json` | Motif entities with geometry hints, placement zones, co-occurring tags |
| `data/palettes.json` | Named color entries with hex values and roles |
| `data/scene_templates.json` | Parametric scene templates for AI prompt assembly |
| `data/qa_checklist.json` | Scored QA checklist for Rococo fidelity |
| `prompts/` | Individual prompt files by scene type |
| `reference/` | Curated artwork and interior references |

## How apps should consume this data

1. Read `data/scene_templates.json` to select a scene type.
2. Pull required and optional motifs from `data/motifs.json`.
3. Apply a palette from `data/palettes.json`.
4. Assemble a prompt using `PROMPT_PACK.md` scaffolds.
5. Validate output against `data/qa_checklist.json`.

## Key Rococo characteristics

- **Asymmetric C- and S-scroll curves** (rocaille, shell, arabesque)
- **Pastel palette** (powder blue, blush rose, celadon mint, cream pearl) with **gilded accents**
- **Fête galante** scenes: aristocratic leisure, flirtation, and music in garden settings
- **Boiserie, mirrors, stucco** in interior architecture
- **Putti, floral garlands, musical instruments** as iconographic staples
- Light, airy mood — intimate scale, not monumental Baroque grandeur

## License

Creative Commons Attribution 4.0 International (CC BY 4.0)
