# Skill Catalog

Use the invocation name below after the skill is installed and available in your current Codex environment. Folder labels may differ from the `name` in `SKILL.md`. Skill instructions do not by themselves supply an image model or API service.

23 callable skill entrypoints and 1 incomplete source folder are documented.

## VisualOS

| Skill | Folder | Invocation | Purpose |
|---|---|---|---|
| [Reference Image Analysis](visual-reference-decoder/USAGE.md) | `visual-reference-decoder` | `$nuyoah-image-reverse-prompt` | Analyze composition, color, lighting and materials; produce a reusable image prompt. |
| [Portrait Photography Direction](portrait-scene-director/USAGE.md) | `portrait-scene-director` | `$nuyoah-xiezhen-prompt` | Plan portrait shoots, write photography prompts and adapt a reference series. |
| [Minimal Paper Posters](paper-editorial-maker/USAGE.md) | `paper-editorial-maker` | `$gc-minimal-zine-poster-v0-3` | Create minimal paper-texture posters with negative space, collage and editorial typography. |
| [Photo Zine Composition](photo-zine-composer/USAGE.md) | `photo-zine-composer` | `$zine` | Compose tactile zines, photo-preserving collages and editorial diptychs. |
| [Everyday Candid Photography](candid-life-photo/USAGE.md) | `candid-life-photo` | `$candid-life-photo` | Write natural everyday scene prompts with ambient light and informal composition. |
| [Staged Candid Characters](discreet-candid-character/USAGE.md) | `discreet-candid-character` | `$discreet-candid-character` | Write staged public-scene prompts for fictional adult characters with occlusion and telephoto framing. |
| [Portrait Emotion Direction](editorial-emotion-control/USAGE.md) | `editorial-emotion-control` | `$editorial-emotion-control` | Control subtle expressions, posture and lighting in portrait prompts. |
| [Photo Style Transformation](style-revival-editor/USAGE.md) | `style-revival-editor` | `$style-revival-editor` | Translate photos into illustration, paper, hand-drawn or retro styles while preserving key features. |
| [Fashion Sketch Portrait](fashion-sketch-portrait/USAGE.md) | `fashion-sketch-portrait` | `$fashion-sketch-portrait` | Redraw a person photo as a high-fashion semi-realistic hand-drawn portrait, preserving identity, hair, clothing colors and props on a near-white paper ground. |
| [Photo-to-Poster Direction](photo-revival-poster/USAGE.md) | `photo-revival-poster` | `$photo-revival-poster` | Define consistent composition, color, material and typography rules for photo-based editorial posters. |
| [Batch Visual Prompts](prompt-batch-conductor/USAGE.md) | `prompt-batch-conductor` | `$prompt-batch-conductor` | Plan distinct visual directions and produce consistent, independent prompts for a series. |
| [AI Character Worldbuilder](ai-character-worldbuilder/USAGE.md) | i-character-worldbuilder | $ai-character-worldbuilder | Build a consistent original adult AI character, ongoing content series and conversion path. |
| [Color Card Outfit Lab](color-card-outfit-lab/USAGE.md) | color-card-outfit-lab | $color-card-outfit-lab | Turn licensed reference-video structure into original color-card outfit stills and video prompts. |

## UI GPT SKIL

| Skill | Folder | Invocation | Purpose |
|---|---|---|---|
| [UI GPT SKIL — Motion Direction](ui-gpt-skil/USAGE.md) | `ui-gpt-skil` | `$ui-gpt-skil` | Translate motion requests into triggers, effects, timing and accessible interaction behavior. |
| [GSAP Core Animation](gsap-skills/gsap-core/USAGE.md) | `gsap-skills/gsap-core` | `$gsap-core` | Implement tweens, easing, stagger and responsive motion. |
| [GSAP Timeline](gsap-skills/gsap-timeline/USAGE.md) | `gsap-skills/gsap-timeline` | `$gsap-timeline` | Sequence and coordinate multiple animation stages. |
| [GSAP Scroll Animation](gsap-skills/gsap-scrolltrigger/USAGE.md) | `gsap-skills/gsap-scrolltrigger` | `$gsap-scrolltrigger` | Implement viewport triggers, pinning and scroll-linked progress. |
| [GSAP for React](gsap-skills/gsap-react/USAGE.md) | `gsap-skills/gsap-react` | `$gsap-react` | Integrate GSAP into React with scoped animations and lifecycle cleanup. |
| [GSAP for Vue and Svelte](gsap-skills/gsap-frameworks/USAGE.md) | `gsap-skills/gsap-frameworks` | `$gsap-frameworks` | Integrate GSAP into non-React component lifecycles. |
| [GSAP Plugins](gsap-skills/gsap-plugins/USAGE.md) | `gsap-skills/gsap-plugins` | `$gsap-plugins` | Use advanced plugins for dragging, text, SVG and layout transitions. |
| [GSAP Performance](gsap-skills/gsap-performance/USAGE.md) | `gsap-skills/gsap-performance` | `$gsap-performance` | Reduce animation jank and unnecessary layout or rendering work. |
| [GSAP Utilities](gsap-skills/gsap-utils/USAGE.md) | `gsap-skills/gsap-utils` | `$gsap-utils` | Use interpolation, mapping, clamping, snapping and related helpers. |

## Apple Design

| Skill | Folder | Invocation | Purpose |
|---|---|---|---|
| [Apple Design](apple-design/SKILL.md) | apple-design | $apple-design | Design interface hierarchy, navigation, components and accessibility using Apple's official Human Interface Guidelines. Marked Internal-use in the skill license field. |

## Incomplete source folder

| Folder | Status | Source description |
|---|---|---|
| [character-continuity-lab](character-continuity-lab/USAGE.md) | Not callable: no `SKILL.md` is included | The source README describes `create-white-block-comic`, a recurring-character two-panel comic workflow; its implementation is absent. |

## Sources and attribution

Original README files, license files and skill instructions are retained. VisualOS directory labels are organizational labels, not replacements for original authorship. The six adapted VisualOS prompt skills describe their origins in their own `Provenance` sections.

GSAP skills were imported from [greensock/gsap-skills](https://github.com/greensock/gsap-skills) and are grouped under **UI GPT SKIL**. The separate `ui-gpt-skil` entry contains motion-direction guidance and the user-supplied Vibe Coding motion dictionary.

