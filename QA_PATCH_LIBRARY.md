# QA_PATCH_LIBRARY.md

Common Rococo generation failure patterns and their prompt/parameter patches.

Each entry includes: **Symptom → Root Cause → Patch**.

---

## 1. Palette Too Dark / Baroque

**Symptom**: Output uses deep reds, dark blues, heavy shadows, jewel tones — reads as Baroque.

**Root Cause**: Model defaulted to Baroque or "old master" palette rather than Rococo light key.

**Patch**:
```
Add: soft pastel palette — powder blue, blush rose, cream pearl, celadon mint, pale yellow
Add: ivory and off-white backgrounds with gilded accents
Add: no dark shadows, no heavy chiaroscuro, light and airy tonal key
Add: style of Boucher (not Rembrandt, not Caravaggio)
```

---

## 2. Too Symmetric / Neoclassical

**Symptom**: Ornament and composition are rigidly symmetric; furniture has straight tapered legs; feels Neoclassical or Empire.

**Root Cause**: Model applied geometric classical order rather than Rococo organic asymmetry.

**Patch**:
```
Add: asymmetric rocaille ornament, C-scroll and S-scroll, no straight lines in ornament
Add: cabriole legs, bombé case shapes, shell-carved crests
Add: asymmetrical composition with diagonal figure grouping
Remove: any classical columns, pilasters, or Greek key motifs unless stylized into Rococo
```

---

## 3. Missing Rocaille / Shell Motifs

**Symptom**: Output is ornate but uses generic floral or Victorian ornament without shell/scroll vocabulary.

**Root Cause**: Prompt did not specify rocaille vocabulary; model used nearest ornament style.

**Patch**:
```
Add: rocaille scrollwork, shell and scroll ornament, C-scrolls and S-scrolls
Add: gilded shell crest on mirror or furniture
Add: style of French Rococo boiserie, Meissonier ornament
```

---

## 4. Figures Look Generic Vintage (Not Rococo)

**Symptom**: Costumes and figures are vaguely historical but not specifically Rococo — could be Victorian, Renaissance, or generic fantasy.

**Root Cause**: Insufficient costume and gesture specificity in prompt.

**Patch**:
```
Add: robe à la française with wide panniers, lace fichu, silk ribbons
Add: powdered wig or elaborate 18th-century coiffure with feathers
Add: habit à la française — embroidered coat, breeches, tricorn hat (for male figures)
Add: flirtatious or leisurely gesture — fan, lute, reaching hand
Add: style of Fragonard or Watteau figure painting
```

---

## 5. Photorealistic Rendering Overrides Ornament

**Symptom**: Output has photorealistic skin texture, lens flare, HDR lighting, or 3D CGI material feel that overrides the painted/decorative quality.

**Root Cause**: Model defaulted to photorealistic rendering pipeline.

**Patch**:
```
Add: oil painting aesthetic, painted ornament, not photorealistic
Add: soft edges, graphic ornament language, poster-like or fresco-like surface
Add: no lens flare, no HDR, no CGI material shaders, no skin pores
Add: style of 18th-century oil painting on canvas
```

---

## 6. Mood Is Too Solemn / Religious

**Symptom**: Scene feels devotional, funerary, or morally serious — not the playful aristocratic leisure of Rococo.

**Root Cause**: Model associated historical European style with religious or heroic iconography.

**Patch**:
```
Add: playful, flirtatious, and elegant mood
Add: fête galante — aristocratic leisure in a garden, flirtation and music
Add: boudoir intimacy, decorative fantasy, mythological playfulness
Remove: crosses, altarpieces, military figures, funeral draping
```

---

## 7. Chinoiserie Drift

**Symptom**: Rococo scene has drifted into Chinoiserie — pagodas, lanterns, Chinese figures dominate.

**Root Cause**: Rococo and Chinoiserie overlap historically; model over-amplified the Chinese influence.

**Patch — keep Chinoiserie**:
```
Add: French Rococo Chinoiserie — European interpretation of Chinese motifs
Add: monkeys dressed as humans (singerie), pagoda motifs integrated into boiserie panels
Add: retain pastel Rococo palette and shell/scroll framing
```

**Patch — suppress Chinoiserie**:
```
Add: purely French Rococo without Chinoiserie influence
Add: European pastoral setting, no pagodas, no Asian architectural forms
```

---

## 8. Shader Output Is Too Uniform / Lacks Asymmetry

**Symptom**: Generative ornament pattern is too regular, tiling too mechanically, lacking Rococo organic drift.

**Root Cause**: Procedural rules enforced strict symmetry or fixed tiling without variation.

**Patch**:
```
- Add slight random angular offset (±5–15°) to each scroll unit.
- Vary scale of shell motifs by ±20% per unit.
- Anchor C-scrolls to corner attractors rather than grid points.
- Add a low-frequency noise field to perturb ornament path curvature.
- Ensure no two adjacent scrolls are exact copies.
```
