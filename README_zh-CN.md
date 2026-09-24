# 🎬 Cinematic Prompt Master（简体中文说明）

**将一段普通的场景描述，变成电影级的 AI 绘图／影片 Prompt —— 附带目的性的运镜，与随机化的面部微表情。**

> 其他语言：[English](README.md) · [简体中文](README_zh-CN.md) · [繁體中文](README_zh-TW.md) · [日本語](README_ja.md) · [한국어](README_ko.md) · [Español](README_es.md) · [العربية](README_ar.md)

---

## 为什么需要这个 skill

大部分 AI 影片 Prompt 只描述**画面里有什么**，但从来不讲**镜头怎么动**、**那张脸到底在做什么**。

结果非常 predictable：

- 📷 镜头没有目的地飘 —— 没有主体，没有动的理由
- 😐 每次特写都是同一个罐头式的「哭／笑」
- 🔁 跑十次，出来十次一模一样的脸

**Cinematic Prompt Master** 同时解决这两个问题。每个 Prompt 都要过两关：

1. **运镜审查与优化** —— 有目的、会用遮挡转场、三轴稳定、有排练感
2. **双重随机面部注入** —— 20 种情绪 × 3 种变体 = 60 种面部状态，随机抽样

---

## 两条核心规则

### 1. 运镜规则（Camera Movement Rules）

| 原则 | 含义 |
|---|---|
| **建立目的性** | 镜头必须锁定明确主体。主体转换时要描述「流畅交接」。 |
| **遮挡转场** | 用甩镜（whip pan），或用柱子、路人、身体遮住镜头一瞬间来藏剪辑。 |
| **推拉＋升降混搭** | Dolly in / out 配 boom / crane，空间转换时改景别（全景 → 特写）。 |
| **稳定视觉** | 默认 3-axis gimbal 或 slider，避免晃到晕。 |
| **走位排练感** | 镜头、演员走位、灯光要有高度排练感，做到零失误的长镜头。 |

> **例外：** 蒙太奇（Montage）与静态拼贴风格 —— **完全不需要运镜描述**。

### 2. 双重随机面部核心注入

- **第一层** —— 按场景氛围挑 1 种情绪大类
- **第二层** —— 从该情绪的 **A / B / C** 中**随机**挑一种（严禁每次都用同一种）

### 20 种情绪大类

`愤怒` · `悲伤` · `恐惧` · `厌恶` · `轻蔑` · `焦虑` · `羞愧` · `内疚` · `嫉妒` · `真心高兴` · `假笑` · `满足` · `感动` · `惊讶` · `困惑` · `怀疑` · `专注` · `隐忍` · `傲慢` · `尴尬`

每种有 3 个解剖学上具体的变体（眉、眼睑、瞳孔、人中、法令纹、颏肌……），总共 60 种状态。

---

## 安装

### Claude Code / Claude.ai

```bash
mkdir -p ~/.claude/skills/cinematic-prompt-master
cp SKILL.md ~/.claude/skills/cinematic-prompt-master/SKILL.md
```

### Cursor / Windsurf / 其他 Agent

将 `SKILL.md` 的内容贴进项目规则文件（例如 `.cursorrules`）或 system prompt。

### 其他模型（Seedance、Kling、Sora、Runway、Midjourney…）

直接把 `SKILL.md` 当作 system instruction 贴进去，然后用自然语言描述你的场景。

---

## 语言版本

| 文件 | 语言 | 说明 |
|---|---|---|
| 文件 | 语言 | 说明 |
|---|---|---|
| `SKILL.md` | English | 主版本，推荐 —— 大多数影片模型对英文解析最好 |
| `SKILL_zh-CN.md` | 简体中文 | 想输出中文 Prompt 时用它 |
| `SKILL_zh-TW.md` | 繁體中文 | 想输出繁体中文 Prompt 时用它 |
| `SKILL_ja.md` | 日本語 | 想输出日文 Prompt 时用它 |
| `SKILL_ko.md` | 한국어 | 想输出韩文 Prompt 时用它 |
| `SKILL_es.md` | Español | 想输出西班牙文 Prompt 时用它 |
| `SKILL_ar.md` | العربية | 想输出阿拉伯文 Prompt 时用它（RTL） |

> 电影术语（dolly in、whip pan、3-axis gimbal 等）在所有版本中都保留英文，
> 因为这些词模型更认得。

---

## 用法

```
你：一个古装女子傍晚在城墙上等人，等到天黑都没等到，最后转身离开。
```

Skill 会回你一个完整 Prompt，包含：

- 一条连贯的运镜链（全景 → 甩镜 → 特写）
- 一组随机抽到的微表情，直接写进了 Prompt
- 稳定器与灯光指示

看 [`examples/before-after.md`](examples/before-after.md) 有三个完整示例。

---

## 用得好的贴士

- 🎲 **让它出 3 个 take。** 每次跑会抽到不同的 A/B/C，挑最满意的那张脸。
- 🗣️ **有特定情绪就直接说出来**；不说则由 skill 按氛围帮你挑。
- 📐 **讲清楚你想要的景别**（例如「最后要落到特写」），skill 会设计运镜走到那里。
- 🎭 **是蒙太奇就明说**，skill 会正确地把所有运镜语言去掉。
- 🌏 默认输出英文 Prompt（大部分影片模型 parse 得最好）；需要中文可以叫它切换。

---

## 贡献

欢迎 PR。最有价值的贡献：

- 🎭 新增情绪大类（每种要附 3 个解剖学上明确不同的变体）
- 🎥 新增运镜 pattern
- 🌐 `SKILL.md` 的其他语言翻译

---

## 授权

[MIT](LICENSE) —— 随便用，注明出处就好。
