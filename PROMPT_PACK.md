# PROMPT_PACK.md

Ready-to-use Rococo prompt scaffolds for AI image generation, prompt engineering tools, and generative composition systems.

Each scaffold is composable: swap bracketed `[slots]` to change subject, palette, motifs, or camera.

---

## Core Prompt Vocabulary (Rococo keywords)

### Style anchors
```
rococo painting, 18th century French rococo, Louis XV style,
fête galante, fête champêtre, pastel palette, gilded ornament,
rocaille scrollwork, shell and scroll ornament, boiserie interior,
soft diffuse light, powdered wig, panniers, cabriole legs
```

### Negative anchors (what to suppress)
```
no baroque chiaroscuro, no dark shadows, no neoclassical austerity,
no photorealistic rendering, no modern elements, no heavy symmetry,
no straight furniture legs, no hard outlines on ornament
```

---

## Scaffold 1: Fête Galante — Park Scene

```
an 18th-century French rococo fête galante in a lush ornamental park,
[N] aristocratic figures in [COLOR] silk gowns and embroidered coats,
flirting, playing lute and violin, dancing beneath feathery-foliaged trees,
marble statues and a stone fountain in the background,
rocaille scrollwork on the fountain base, floral garlands hanging from trees,
soft pastel palette — powder blue, blush rose, cream — with gilded accents,
diffuse warm afternoon light, gentle atmospheric depth,
style of Watteau and Fragonard, oil painting aesthetic
```

**Slots:**
- `[N]`: 3 / 5 / 7 / 10 figures
- `[COLOR]`: powder blue / blush rose / pale yellow / celadon mint

**Add-ons:**
- `a small spaniel dog at the feet of the central figure`
- `a garden swing hung from a large oak, a figure mid-swing`
- `distant garden pavilion half-hidden in mist`

---

## Scaffold 2: Boudoir Portrait

```
a rococo portrait of an aristocratic [GENDER] in a [COLOR] silk [GARMENT],
seated on a gilded chaise longue in an intimate boudoir,
white and gold boiserie wall panels behind, an ornate gilded mirror above the fireplace,
soft silk draperies in pastel tones framing the scene,
rocaille shell ornament on the mirror frame and chair crest,
small porcelain vase and fresh roses on the console table,
soft interior diffuse light with selective highlights on satin folds and gold leaf,
style of Boucher and Vigée Le Brun, oil on canvas aesthetic
```

**Slots:**
- `[GENDER]`: woman / man / couple
- `[COLOR]`: blush rose / powder blue / pale yellow
- `[GARMENT]`: robe à la française / embroidered court coat

**Add-ons:**
- `a small lap dog curled on the chaise`
- `a stack of leather-bound books and writing implements`
- `a Venetian mask on the vanity table`

---

## Scaffold 3: Ceiling Fresco

```
a rococo ceiling fresco, viewer looking upward,
an oval trompe-l'œil opening revealing a bright pastel sky,
clusters of plump putti playing with garlands and clouds,
allegorical female figures in flowing silk draperies floating on clouds,
swirling gilded stucco rocaille cartouches framing the oval,
asymmetric shell and scroll ornament in the corners,
pastel colors — pale gold, sky blue, cloud white, blush — with warm gilding,
bright diffuse sky light radiating from the center,
style of Tiepolo and Boucher ceiling work, fresco aesthetic
```

**Add-ons:**
- `a central allegorical figure (Aurora, Venus, or Juno) on a cloud chariot`
- `peacock feathers and roses scattered among the clouds`
- `architectural illusionism: painted columns appear to extend upward into the sky`

---

## Scaffold 4: Rococo Salon Interior

```
a grand rococo salon interior, 18th-century French,
high boiserie-paneled walls in cream and gold, elaborate stucco ornament,
tall windows with silk drapes, a crystal chandelier overhead,
paired gilded mirrors above gilded console tables,
rocaille ornament on the fireplace surround and overmantel mirror,
porcelain vases, ornate bracket clock, floral arrangements,
chairs and settees with cabriole legs and pastel silk upholstery,
parquet floor, soft natural light from tall windows,
style of the Palace of Versailles and Hôtel de Soubise, architectural interior rendering
```

**Add-ons:**
- `a small group of aristocrats in conversation near the fireplace`
- `a harpsichord in the corner with sheet music open`
- `a tapestry on one wall depicting a pastoral scene`

---

## Scaffold 5: Rococo Still Life / Vanitas

```
a rococo still life on a marble console table,
porcelain figurines, a Meissen vase filled with roses and peonies,
a Venetian mask, a pearl necklace, a folded fan,
gilded clock with scrollwork, scattered petals on the silk cloth,
warm soft light from an unseen window,
pastel palette — rose, cream, gold — against a dark boiserie background,
style of 18th-century French decorative painting
```

---

## Scaffold 6: Mythological Boudoir

```
a rococo mythological painting, Venus and Cupid in a boudoir setting,
Venus semi-draped in pale pink silk on a gilded daybed,
Cupid (putti) hovering nearby with bow and arrows,
doves perched on a curtain rod, rose garlands framing the scene,
warm soft light, pastel and ivory palette, gilded accents,
shallow garden or interior setting, statues of Amor visible in background,
style of Boucher, oil on canvas, mythological pastoral
```

---

## Scaffold 7: Shader / Generative Ornament Field

```
an infinite rococo ornament pattern,
asymmetric shell and C-scroll interlace repeating with variation,
floral rosettes, acanthus leaves, and pearl bead chains filling the field,
pastel gold on cream background, selectively gilded ornament highlights,
no straight lines, all curves — S-curves, C-scrolls, spirals, fans,
high ornament density with breathing space in the center of each unit,
suitable as a wallpaper or shader texture tile
```

---

## Assembling Custom Prompts: Rules of Thumb

1. Always anchor with at least one Rococo style keyword (see Core Vocabulary above).
2. Specify palette explicitly — models default to oversaturated or Baroque darks without guidance.
3. Include at least one motif family: rocaille, garland, putti, or gilded mirror.
4. Name a relevant artist reference: Watteau, Boucher, Fragonard, Vigée Le Brun, Tiepolo.
5. Use negative anchors to suppress Baroque, Neoclassical, or modern contamination.
6. For shaders: replace figure/scene terms with pattern/field/tile language from Scaffold 7.
