# 🎬 Cinematic Prompt Master

**Turn a plain scene description into a cinematic-grade AI image / video prompt — with purposeful camera movement and randomized facial micro-expressions.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**🌍 [English](README.md) · [简体中文](README_zh-CN.md) · [繁體中文](README_zh-TW.md) · [日本語](README_ja.md) · [한국어](README_ko.md) · [Español](README_es.md) · [العربية](README_ar.md)**

*English below. 语言版本见 [Language versions](#language-versions).*

---

## Why this exists

Most AI video prompts describe **what** is in the frame, but never **how the camera moves** or **what the face is actually doing**.

The result is predictable:

- 📷 Camera floats with no intent — no subject, no reason to move
- 😐 Every close-up has the same generic "sad / happy" face
- 🔁 Run it ten times, get ten identical expressions

**Cinematic Prompt Master** fixes both. It forces every prompt through a two-step pipeline:

1. **Camera Movement Review** — purposeful, occlusion-aware, gimbal-stable, rehearsed
2. **Double-Random Facial Injection** — 20 emotions × 3 variants = 60 distinct facial states, sampled randomly

---

## The two core mechanics

### 1. Camera Movement Rules

| Principle | What it means |
|---|---|
| **Purposeful Movement** | The camera locks onto a clear subject. If the subject changes, the shot must hand off smoothly. |
| **Occlusion Transitions** | Use a whip pan, or let a pillar / passer-by / body block the lens for a frame, to hide the cut. |
| **Dolly + Boom Mixing** | Combine dolly in / dolly out with boom / crane, and shift shot scale across space changes (wide → close-up). |
| **Visual Stability** | Default to a 3-axis gimbal or slider look. No nausea-inducing shake. |
| **Choreographed Blocking** | Camera, actor blocking and lighting must feel rehearsed — a zero-error continuous shot. |

> **Exception:** Montage and static-collage styles get **no** camera description at all.

### 2. Double-Random Facial Injection

- **Layer 1** — pick 1 emotional category matching the scene mood
- **Layer 2** — randomly pick **one** of that emotion's **A / B / C** variants

Repeating the same variant every time is strictly forbidden, which is what keeps output from going stale.

### The 20 emotion categories

`Anger` · `Sadness` · `Fear` · `Disgust` · `Contempt` · `Anxiety` · `Shame` · `Guilt` · `Jealousy` · `True Joy` · `Social Smile` · `Contentment` · `Moved` · `Surprise` · `Confusion` · `Skepticism` · `Focus` · `Suppression` · `Hubris` · `Embarrassment`

Each comes with 3 anatomically specific variants (brow, eyelid, pupil, philtrum, nasolabial fold, ment… ) — 60 states total.

---

## Install

### Claude Code / Claude.ai Skills

```bash
mkdir -p ~/.claude/skills/cinematic-prompt-master
cp SKILL.md ~/.claude/skills/cinematic-prompt-master/SKILL.md
```

### Cursor / Windsurf / other agents

Paste the contents of `SKILL.md` into your project rules file (e.g. `.cursorrules`) or system prompt.

### Any other model (Seedance, Kling, Sora, Runway, Midjourney…)

Just paste `SKILL.md` as the system instruction, then describe your scene in natural language.

---

## Language versions

| File | Language | Note |
|---|---|---|
| File | Language | Note |
|---|---|---|
| `SKILL.md` | English | Main version — recommended, best parsed by most video models |
| `SKILL_zh-CN.md` | 简体中文 (Simplified) | Use this if you want Chinese prompt output |
| `SKILL_zh-TW.md` | 繁體中文 (Traditional) | Use this if you want Traditional Chinese prompt output |
| `SKILL_ja.md` | 日本語 | Use this if you want Japanese prompt output |
| `SKILL_ko.md` | 한국어 | Use this if you want Korean prompt output |
| `SKILL_es.md` | Español | Use this if you want Spanish prompt output |
| `SKILL_ar.md` | العربية | Use this if you want Arabic prompt output (RTL) |

> Cinematography terms (dolly in, whip pan, 3-axis gimbal…) stay in English across
> all versions — models recognise these tokens more reliably.

---

## Usage

```
You: A woman in ancient costume waits on the city wall at dusk.
     It gets dark and he never comes. She turns and leaves.
```

The skill returns a full prompt with:

- A chained camera move (wide → whip pan → close-up)
- One randomly sampled micro-expression, written into the prompt
- Stability and lighting instructions baked in

See [`examples/`](examples/) for three full before / after walkthroughs.

---

## Tips for best results

- 🎲 **Ask for 3 takes.** Each run samples a different A/B/C variant — pick the best face.
- 🗣️ **Say the emotion out loud** if you have one in mind; otherwise let the skill choose from the mood.
- 📐 **Name your shot scale** ("I want it to end on a close-up") and the skill will design the move to land there.
- 🎭 **Montage?** Say so explicitly — the skill will correctly drop all camera language.
- 🌏 Prompt output is English by default (best parsed by most video models). Ask for Chinese / Cantonese output if you need it.

---

## Repo structure

```
cinematic-prompt-master/
├── SKILL.md              # the skill itself (EN) — this is all you need
├── SKILL_zh-CN.md        # 简体中文版
├── SKILL_zh-TW.md        # 繁體中文版
├── SKILL_ja.md           # 日本語版
├── SKILL_ko.md           # 한국어版
├── SKILL_es.md           # Versión en español
├── SKILL_ar.md           # النسخة العربية
├── README.md             # you are here (EN)
├── README_zh-CN.md       # 简体中文說明
├── README_zh-TW.md       # 繁體中文說明
├── README_ja.md          # 日本語の説明
├── README_ko.md          # 한국어 설명
├── README_es.md          # Documentación en español
├── README_ar.md          # التوثيق بالعربية
├── LICENSE               # MIT
└── examples/
    └── before-after.md   # 3 full walkthroughs
```

---

## Contributing

Pull requests welcome. The highest-value contributions:

- 🎭 New emotion categories (with 3 anatomically distinct variants each)
- 🎥 New camera-movement patterns
- 🌐 Translations of `SKILL.md`

---

## License

[MIT](LICENSE) — do whatever you want, attribution appreciated.
