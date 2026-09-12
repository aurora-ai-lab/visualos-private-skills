# Zine Poster Skill — Editorial Image Generation for AI Agents

**English** · [简体中文](README.zh-CN.md)

**Project status:** active

Turn an idea or photograph into restrained, tactile editorial artwork without relying on a loose collection of prompts.

- **Deterministic compiler** — every request is normalized into one inspectable prompt and a predictable image-tool call.
- **Isolated style contracts** — `minimal`, `scenes`, and `editorial` cannot silently leak rules into one another.
- **Explicit source fidelity** — preserve real photo pixels, distill semantics into an original illustration, or pair a faithful photo with a source-derived abstract panel.

[![Tests](https://github.com/jas0nh/zine-poster-skill/actions/workflows/test.yml/badge.svg)](https://github.com/jas0nh/zine-poster-skill/actions/workflows/test.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-111111.svg)](LICENSE)

<p align="center">
  <img src="assets/samples/zine-channel-guide.png" width="400" alt="Guide comparing minimal, photo-preserving scenes, source-distilled scenes, and editorial zine channels">
</p>

## Choose a channel

| Channel | Input | Source-pixel policy | Result |
| --- | --- | --- | --- |
| `minimal` | Idea or text | No photo required | Quiet aged-paper poster with radical whitespace and one compact visual anchor |
| `scenes --preserve-photo` | Photograph | Preserves truthful photo material | Torn-paper photographic expansion with a visible fibrous handoff |
| `scenes --distill` | Photograph | Forbids source pixels in the result | Original illustration derived only from the source's meaning and structure |
| `editorial` | Photograph | Preserves a faithful photo region | Clean photo-and-abstract-panel composition derived from observed relationships and colors |

## 10-second quick demo

From the repository root, compile a complete prompt without credentials, provider setup, or third-party Python packages:

```bash
python3 scripts/zine-command.py \
  --command '/zine minimal --prompt-only A rain-soaked bookshop at midnight' \
  | python3 -m json.tool
```

The JSON output exposes the selected channel, style recipe, aspect ratio, exact final prompt, and the tool-call contract. Prompt-only mode deliberately leaves the generation call empty.

## Requirements

- Git and Python 3.10 or newer; the compiler and tests use only the Python standard library.
- For generated artwork, a host agent with a prompt-based image-generation tool.
- For photo workflows, a host tool that accepts reference images.
- Provider credentials remain owned and configured by the host; this skill does not read or store them.

## Install

### One-liner for Codex

```bash
git clone --depth 1 https://github.com/jas0nh/zine-poster-skill.git "${CODEX_HOME:-$HOME/.codex}/skills/zine"
```

Start a new Codex conversation after installation so the skill catalog refreshes.

### Tell an agent to install it

Paste this one-line instruction into an agent that can access GitHub and its local skills directory:

```text
Install the skill from https://github.com/jas0nh/zine-poster-skill as `zine` in your local skills directory, validate its SKILL.md, and report the installed path; do not modify provider credentials.
```

The agent should clone or copy the repository so that `SKILL.md` is directly inside the final `zine/` directory. Typical destinations include:

- Codex: `${CODEX_HOME:-$HOME/.codex}/skills/zine`
- Hermes: `${HERMES_HOME:-$HOME/.hermes}/skills/zine`
- Other harnesses: the harness's documented local skill directory

For Hermes, the equivalent one-liner is:

```bash
git clone --depth 1 https://github.com/jas0nh/zine-poster-skill.git "${HERMES_HOME:-$HOME/.hermes}/skills/zine"
```

If the destination already exists, update it with `git -C <path> pull --ff-only` or install into a new directory after reviewing local changes.

## Usage

```text
/zine --help
/zine minimal A rain-soaked bookshop at midnight
/zine scenes --preserve-photo Turn this street photo into a tactile zine composition
/zine scenes --distill Reinterpret this seaside photo as a study of distance
/zine editorial Pair the original photo with its abstract memory panel
```

`scenes --preserve-photo` retains truthful photographic material and introduces a torn fibrous handoff. `scenes --distill` uses the source only as semantic evidence and forbids photographic pixels in the final artwork. `editorial` keeps the photo faithful and derives a separate clean ivory panel from observed relationships and source colors.

Run the deterministic compiler directly for prompt-only use:

```bash
python3 scripts/zine-command.py \
  --command '/zine minimal --prompt-only A rain-soaked bookshop at midnight'
```

For photo workflows, provide a compact JSON card containing `reference_image` plus source observations described in [`references/style-harness.md`](references/style-harness.md).

## Compatibility

| Host | Installation or integration | Support level |
| --- | --- | --- |
| Codex | Clone into `${CODEX_HOME:-$HOME/.codex}/skills/zine` | Designed and tested with Codex and GPT-Image-2 |
| Hermes | Clone into `${HERMES_HOME:-$HOME/.hermes}/skills/zine` | Local-skill installation; generation depends on the configured host image tool |
| Other agent harnesses | Run the compiler and map its generic JSON arguments to the host image tool | Compatible when the host supports prompts and, for photo modes, reference images |

## Compiler integration

The compiler emits a generic JSON structure containing:

- the selected channel and style;
- the final prompt;
- the requested aspect ratio;
- reference-image fields when supplied;
- an `image_generate`-shaped call for compatible harnesses.

Agents using a differently named image tool should preserve the compiled prompt exactly and map only the aspect-ratio and reference-image arguments. Credentials and provider selection remain the responsibility of the host harness.

## References and attribution

This project synthesizes and extends ideas from the following skills. Please visit the original repositories for their authors' full documentation and current license terms:

- [Zeejay0/gathered-scenes-zine-skill](https://github.com/Zeejay0/gathered-scenes-zine-skill) — photo-preserving Gathered Scenes and semantic distillation concepts; MIT at the reviewed revision.
- [LiamGvchi/gc-minimal-zine-poster](https://github.com/LiamGvchi/gc-minimal-zine-poster) — minimal zine-poster composition and material language; MIT at the reviewed revision.
- [ZzzLc0405/photo-abstract-editorial](https://github.com/ZzzLc0405/photo-abstract-editorial) — faithful-photo plus source-derived abstract-panel workflow. No explicit license file was present at the reviewed revision, so this repository links and credits the project but does not redistribute its prompt files or example assets.

Detailed revision and license notes are preserved in [`references/upstream-licenses.md`](references/upstream-licenses.md) and [`NOTICE`](NOTICE).

## License

The original code, prompts, documentation, and generated help artwork in this repository are released under the [MIT License](LICENSE). Third-party projects remain subject to their respective licenses.
