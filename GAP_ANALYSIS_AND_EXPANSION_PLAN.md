# GAP_ANALYSIS_AND_EXPANSION_PLAN.md

Tracks missing content, known weaknesses, and planned expansions for the `rococo_style` repository.
Update this file as gaps are identified during generation and QA sessions.

---

## Current Coverage Status

| Dimension | Status | Notes |
|---|---|---|
| Core motif families (rocaille, flora, fauna, figures, architecture, objects) | ✅ Initial draft | See `MOTIF_DICTIONARY.md` and `data/motifs.json` |
| Palette entries (pastels + gilded) | ✅ Initial draft | See `data/palettes.json` |
| Scene templates (fête galante, boudoir, ceiling, salon) | ✅ Initial draft | See `data/scene_templates.json` |
| Prompt scaffolds | ✅ Initial draft | See `PROMPT_PACK.md` |
| QA checklist | ✅ Initial draft | See `data/qa_checklist.json` |
| Distinction rules (vs Baroque, Neoclassicism) | ✅ In STYLE_SPEC.md | — |
| Chinoiserie sub-style | ⚠️ Partial | Mentioned in QA patches; needs dedicated motif entries |
| Rococo architecture (exteriors) | ❌ Missing | Wieskirche, Sanssouci, Charlottenburg exteriors |
| Rococo sculpture typology | ❌ Missing | Falconet, Clodion — small bronze and porcelain figurines |
| Rococo textile patterns | ❌ Missing | Brocade, damask, toile de Jouy |
| Rococo porcelain / Meissen typology | ❌ Missing | Figurines, tableware, chinoiserie ware |
| Regional variants | ❌ Missing | German/Bavarian Rococo vs French vs Italian |
| Specific artist grammars | ⚠️ Partial | Watteau, Boucher, Fragonard mentioned; no dedicated entries |
| Shader-specific procedural rules | ⚠️ Partial | Mentioned in STYLE_SPEC; no dedicated shader JSON |
| Animation / motion grammar | ❌ Missing | How drapery, garden elements, and putti should move |

---

## Priority Expansion Items

### High priority

1. **Chinoiserie sub-style motif set** (`data/motifs_chinoiserie.json`)
   - Singerie, pagoda, lantern, bamboo, Chinese garden bridge
   - Blended with standard Rococo shell/scroll framing

2. **Regional variant profiles** (`data/regional_variants.json`)
   - French Rococo (delicate, pastel, Parisian)
   - German/Bavarian Rococo (more exuberant stucco, whiter interiors, Wieskirche-type)
   - Italian Rococo (Tiepolo's ceiling frescoes; lighter color, more theatrical)

3. **Artist grammar entries** (`data/artist_grammars.json`)
   - Watteau: misty soft-focus fêtes, theatrical melancholy, figures slightly apart
   - Boucher: rosy soft flesh, explicit pastoral mythology, very pink and blue
   - Fragonard: dynamic movement, voyeuristic energy, lush greens, flying fabric
   - Vigée Le Brun: sympathetic portraiture, fashionable costume accuracy
   - Tiepolo: grand ceiling illusionism, strong sky and cloud drama

4. **Shader procedural spec** (`data/shader_spec.json`)
   - Curve density maps by zone type
   - Ornament anchor point logic
   - Material presets: gilt, stucco, satin, marble, crystal
   - Palette-to-shader-uniform mapping

### Medium priority

5. **Textile pattern library** (`data/textiles.json`)
   - Brocade, silk damask, toile de Jouy patterns
   - Parameters: repeat type, motif family, colorway

6. **Sculpture typology** (`data/sculpture.json`)
   - Small bronze/terracotta figurines (Clodion nymphs)
   - Porcelain figurines (Meissen shepherd/shepherdess)
   - Garden statuary (lead nymphs, putti, classical figures in Rococo dress)

### Low priority

7. **Architectural exterior typology**
8. **Animation/motion grammar for generative video**
9. **Negative example library** (annotated bad outputs for model training)

---

## How to Contribute Expansions

1. Add motifs to `data/motifs.json` following the existing schema.
2. Add scene templates to `data/scene_templates.json`.
3. Add prompt examples to `prompts/` as individual `.md` files.
4. Update this file to mark items as ✅ complete.
5. Open a PR with a descriptive commit message referencing the dimension being expanded.
