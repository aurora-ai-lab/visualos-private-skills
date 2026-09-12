# Zine style harness

Use this reference to build the compact card consumed by `scripts/zine-command.py`. Keep source analysis in the card; keep stable art direction in the compiler.

## Channel routing

Treat `minimal`, `scenes`, and `editorial` as mutually exclusive channels. Share only backend/tool mechanics across them; do not leak paper, edge, palette, typography, density, or source-pixel defaults from one channel into another. `scenes` contains two explicit source-pixel modes: `gathered` (`--preserve-photo`) and `distilled` (`--distill`).

| Style | Input | Source-pixel policy | Visual center |
|---|---|---|---|
| `minimal` | theme, sentence, object, mood, article idea; image optional | Do not depend on source pixels | one small imageable anchor on quiet paper |
| `gathered` | reference photo required | Preserve truthful photography for the core anchor | photo + expanded source-derived illustration field |
| `editorial` | one reference photo required | Keep the photo faithful; allow only proportional scaling or a slight safe crop | clean photo region + separate abstract memory panel |
| `distilled` | reference photo normally expected | Reference is semantic evidence only; final image contains no source pixels | proposition, tension and metaphor embodied as original illustration |

Use `auto` as follows: no reference → `minimal`; reference with explicit original-photo + abstract-panel/diptych intent → `editorial`; otherwise enter `scenes`, choosing `distilled` for explicit redraw/no-photo/reinterpret intent and `gathered` otherwise.

## Minimal + scenes shared spine

- Apply this section only to `minimal` and `scenes`; never inherit it into `editorial`.
- Keep the result tactile, flat-scanned, poetic, source-specific and non-commercial.
- Use warm aged paper, matte fibers, restrained grain, ink bite and imperfect reproduction.
- Preserve 68–90% quiet paper unless source fidelity requires a larger photo anchor.
- Use one dominant subject or inseparable relationship, one primary illustration grammar and at most one supporting grammar.
- Remove detail before adding decoration. Never add tape, stamps, coordinates, crosses, grids or dots by habit.
- Use one exact high-chroma hue as focal entry, counterweight, bridge, field or directional cue, except in `editorial`, which must use only a reduced source-sampled palette and may remain muted.
- Make typography serve the visual proposition; never use faux metadata, invented attribution or long clean copy.
- Avoid commercial headline hierarchy, ads, logos, CTA, glossy mockups, clean UI surfaces, heavy shadows, 3D, cinematic light, depth of field, neon, anime, kawaii, fashion drama and dense scrapbooking.

## Card construction

Resolve only fields supported by the harness:

- `semantic_nucleus`: smallest subject, relationship or event that gives the input meaning.
- `subject`: one core subject or at most two inseparable subjects.
- `supporting`: one to three place, season, action or atmosphere cues.
- `spatial_invariant`: one relationship that must survive: near/far, facing, overlap, enclosure, direction, horizon or path.
- `dominant_gesture`: gaze, lean, curve, diagonal, repetition, convergence or movement.
- `proposition`: one source-specific sentence about what the artwork asks the viewer to feel or notice.
- `tension`: one primary opposition such as intimacy/distance, shelter/confinement, movement/stillness, warmth/coldness or permanence/fragility.
- `metaphor`: one source-derived object or relation shifted into an expressive role.
- `interpretive_opening`: one meaningful question left unresolved through omission, obstruction, scale or text-image gap.
- `discard`: clutter, redundant objects and realistic micro-detail that must disappear.
- `observed_facts`: three to six concrete axes, intervals, overlaps, scale relations, repetitions, depth layers, light roles or negative spaces from the photo.
- `palette`: a reduced set of color roles sampled only from the supplied photo.
- `photo_panel_ratio`: source-responsive photo/panel height guidance; avoid a mechanical 50/50 split.
- `composition`, `illustration_grammar`, `typography`, `text`, `hue`, `color_role`, `edge`, `mood`, `orientation`.

Never fill every field with generic adjectives. Concrete source-derived cues beat mood labels.

## Minimal

Compile a vertical 3:5 paper poster by default:

- 70–90% plain paper;
- one cluster around 8–25% of the canvas;
- one object, specimen, silhouette, old printed illustration, torn clipping, texture window or short conceptual relation;
- xerox, risograph, halftone, letterpress or scan defects;
- small serif, typewriter or monospaced typography;
- one saturated color anchor visible at thumbnail scale.

Choose one layout family: asymmetric island, lower-left float, upper-right block, dual panel, irregular cutout, type-led, orbit/drift or single specimen. Do not default to a centered object or a tiny blue dot.

## Gathered

Build a Scene Card before writing prompt fields:

- factual photographic anchor around 25–50%;
- illustration field influencing roughly 45–70% while staying low-density;
- one source shape shared across photography, illustration and color;
- visible hand-torn fibrous edge at the primary photo-to-paper handoff;
- one restrained micro-text element in a quiet paper pocket.

Compress foliage, crowds, gravel, branches and repeated architecture aggressively. Merge 85–95% of leaf/needle/fine-twig detail into one main mass, one to three gestures and at most two secondary clusters. The illustration must reinterpret rather than trace.

Choose a chromatic integration mode: source continuation, selective replacement, underprint passage, counterform or directional rhythm. The added hue must satisfy at least two tests: source-derived geometry, physical overlap, boundary crossing, eye-path change, balance change or semantic emphasis.

## Distilled

Build the internal chain:

```text
source fact → emotional residue → proposition → tension → metaphor → formal embodiment → interpretive opening
```

Preserve two to four semantic anchors, not the photographic composition. Remove 65–90% of descriptive detail. Choose one grammar: cut-paper mass, dry-print silhouette, broken contour, rhythm field, fragment stack or orbit/drift.

Allow source-consistent invention only when it extends emotion, clarifies relationship, establishes rhythm, balances weight, guides the eye or strengthens the metaphor.

Always enforce both statements in the final prompt:

```text
Do not reproduce, embed, crop, collage, trace, or retain photographic pixels or photorealistic regions from the reference.
The final image must contain original illustration, paper, and typography only.
```

## Editorial

Keep this branch visually and materially distinct from `gathered`:

- preserve the supplied photo as a faithful upper or principal region; permit only proportional scaling and a slight safe crop;
- derive three to six observed spatial facts before abstraction;
- rebuild relationships rather than silhouettes in a separate flat ivory memory panel;
- use one primary mark family and at most two supporting families;
- sample all abstract-panel colors from the source photo and reduce their saturation and number;
- keep roughly 65–80% of the panel empty;
- place one short title only on the panel;
- join photo and panel directly with no torn fibers, frame, shadow, tape, grain, stain or collage depth.

Every important abstract mark must map to a real source fact. Never redraw, extend, filter or recolor the photo, and never turn the lower panel into a thumbnail, trace, icon set or complete illustration.

## Color modes

Standard Accent Mode is the default for `minimal`, `gathered`, and `distilled`. Specify hue, material, area, adjacency and structural role. High-chroma area should be about 0.8–3% of the full poster or 10–30% of the active cluster. For `editorial`, never invent this accent: reduce and reuse only colors visibly present in the source photo.

Use Solid Color-Block Mode only for `--mono-block` or the exact phrase `单色块模式`:

1. natural paper;
2. one neutral ink system for every non-accent form and text;
3. exactly one connected saturated field occupying roughly 3–12% of the poster or 25–65% of the active cluster.

Do not split the field into echoes, dots, stripes or separate colored objects.

## Text

- Preserve user-supplied text exactly.
- Otherwise author one short scene-derived phrase only when it improves the work.
- Keep generated text short enough for image-model reliability.
- Place it as a quiet visual object, not explanatory copy.
- For `gathered`, default to English-only micro-text unless the user supplies or requests Chinese/bilingual text.
- For `distilled`, typography may be freer, but its material and placement must deepen the proposition.

## Targeted correction

Regenerate at most once. Correct only the observed failure:

- source loss → restore the defining spatial invariant;
- over-literal or dense output → merge forms and remove at least half the remaining detail;
- timid illustration → enlarge the field without adding detail;
- weak/decorative color → derive the colored form from source geometry and give it a structural role;
- missing gathered boundary → restore irregular torn contour and exposed fibers;
- editorial photo drift → restore the faithful photo region and remove redraw, filtering or invented extension;
- editorial panel literalness → return to relationships, reduce mark families and restore 65–80% clean ivory space;
- distilled photo leakage → restate the no-photo rule and convert leaked regions to original flat illustration;
- typography failure → shorten, restore exact wording, reduce hierarchy or move into quiet paper.
