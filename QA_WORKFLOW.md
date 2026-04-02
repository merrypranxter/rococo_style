# QA_WORKFLOW.md

Process for verifying AI-generated images, shader outputs, and procedural compositions against the Rococo style grammar defined in `STYLE_SPEC.md`.

---

## Phase 1: Pre-Generation Setup

Before generating, confirm the following inputs are correct:

- [ ] **Scene template selected** from `data/scene_templates.json`.
- [ ] **Required motifs** are listed in the prompt (check `data/motifs.json` for co-occurring tags).
- [ ] **Palette** is drawn from `data/palettes.json` (pastel families + gilded accents).
- [ ] **Negative anchors** are included to suppress Baroque darkness, Neoclassical lines, and photorealism.
- [ ] **Artist reference** is named (Watteau, Boucher, Fragonard, Vigée Le Brun, or Tiepolo).

---

## Phase 2: First-Pass Evaluation (Rapid Triage)

Apply these five quick checks immediately after generation:

| Check | Pass | Fail → Action |
|---|---|---|
| Palette: soft pastels + gold? | ✓ | Add palette specification; increase pastel emphasis in prompt |
| Curves dominate over straight lines? | ✓ | Add `asymmetric C- and S-scroll curves` to prompt; remove architectural rigidity |
| At least one rocaille/shell/scroll motif? | ✓ | Add `rocaille scrollwork, shell and scroll ornament` |
| Subject is aristocratic leisure, boudoir, or ornamental interior? | ✓ | Restate scene type; add fête galante or boudoir vocabulary |
| No heavy chiaroscuro or dark Baroque palette? | ✓ | Add negative anchors; increase light key in prompt |

If any check fails, patch the prompt using `QA_PATCH_LIBRARY.md` and regenerate.

---

## Phase 3: Detailed Scoring

Score the output using the 20-item checklist in `STYLE_SPEC.md` Section 5 (or `data/qa_checklist.json`).

- Score each item 0, 1, or 2.
- Calculate total out of 40.
- Acceptance threshold: **32+** with no critical failure flags.

Log scores in a generation log if tracking model consistency over time.

---

## Phase 4: Critical Failure Check

Before accepting any output, confirm none of the auto-reject conditions apply:

- [ ] Heavy chiaroscuro or dark Baroque palette dominates? → **Reject**
- [ ] No rocaille/scroll motifs AND no Rococo subject matter? → **Reject**
- [ ] Straight-leg Neoclassical furniture or classical orders visible without Rococo overlay? → **Reject**
- [ ] Photorealistic rendering pipeline that erases ornament language? → **Reject**
- [ ] Modern visual language (flat design, neon, sci-fi) without intentional stylized bridge? → **Reject**

If rejected, consult `QA_PATCH_LIBRARY.md` for targeted fixes.

---

## Phase 5: Acceptance and Logging

On acceptance:

- Note which scene template and motifs were used.
- Record palette profile applied.
- Note any prompt patches that were needed (feed back into `QA_PATCH_LIBRARY.md`).

---

## Shader-Specific QA

For shader/generative ornament outputs, use this adapted checklist:

- [ ] Curve density in ornament band zones is high; field zones have lower density.
- [ ] No long straight-line features in the ornament field.
- [ ] Shell/scroll motifs appear at key anchor points (corners, intersections).
- [ ] Palette is pastel + gold with correct value distribution (light overall, selective gold highlights).
- [ ] Texture suggests carved stucco or painted wood — not photorealistic 3D or flat digital.
- [ ] Pattern tiles or fields feel Rococo-first, not generically floral or Victorian.
