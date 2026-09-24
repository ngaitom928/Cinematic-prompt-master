# 🎬 Cinematic Prompt Master（繁體中文說明）

**將一段普通嘅場景描述，變成電影級嘅 AI 繪圖／影片 Prompt —— 附帶有目的性嘅運鏡，同隨機化嘅面部微表情。**

> 其他語言：[English](README.md) · [简体中文](README_zh-CN.md) · [繁體中文](README_zh-TW.md) · [日本語](README_ja.md) · [한국어](README_ko.md) · [Español](README_es.md) · [العربية](README_ar.md)

---

## 點解要有呢個 skill

大部分 AI 影片 Prompt 只描述**畫面入面有啲乜**，但從來唔講**鏡頭點郁**、**塊面實際做緊乜**。

結果好 predictable：

- 📷 鏡頭冇目的咁飄 —— 冇主體，冇理由去郁
- 😐 每次特寫都係同一個「喊／笑」嘅罐頭表情
- 🔁 跑十次，出十次一模一樣嘅面

**Cinematic Prompt Master** 同時解決兩個問題。每個 Prompt 都要過兩關：

1. **運鏡審查與優化** —— 有目的、識用遮擋轉場、三軸穩定、有排練感
2. **雙重隨機面部注入** —— 20 種情緒 × 3 種變體 = 60 種面部狀態，隨機抽樣

---

## 兩條核心規則

### 1. 運鏡規則（Camera Movement Rules）

| 原則 | 意思 |
|---|---|
| **建立目的性** | 鏡頭要鎖定明確主體。主體轉換時要描述「流暢交接」。 |
| **遮擋轉場** | 用甩鏡（whip pan），或者用柱、路人、身體遮住鏡頭一瞬間嚟藏剪接。 |
| **推拉＋升降混搭** | Dolly in / out 配 boom / crane，空間轉換時改景別（全景 → 特寫）。 |
| **穩定視覺** | 預設 3-axis gimbal 或 slider，避免晃到暈。 |
| **走位排練感** | 鏡頭、演員走位、燈光要有高度排練感，做到零失誤嘅長鏡頭。 |

> **例外：** 蒙太奇（Montage）同靜態拼貼風格 —— **完全唔需要運鏡描述**。

### 2. 雙重隨機面部核心注入

- **第一層** —— 按場景氛圍揀 1 種情緒大類
- **第二層** —— 由嗰種情緒嘅 **A / B / C** 入面**隨機**揀一種（嚴禁每次都用同一種）

### 20 種情緒大類

`憤怒` · `悲傷` · `恐懼` · `厭惡` · `輕蔑` · `焦慮` · `羞愧` · `內疚` · `嫉妒` · `真心高興` · `假笑` · `滿足` · `感動` · `驚訝` · `困惑` · `懷疑` · `專注` · `隱忍` · `傲慢` · `尷尬`

每種有 3 個解剖學上具體嘅變體（眉、眼瞼、瞳孔、人中、法令紋、頦肌……），總共 60 種狀態。

---

## 安裝

### Claude Code / Claude.ai

```bash
mkdir -p ~/.claude/skills/cinematic-prompt-master
cp SKILL.md ~/.claude/skills/cinematic-prompt-master/SKILL.md
```

### Cursor / Windsurf / 其他 Agent

將 `SKILL.md` 內容貼入項目規則檔（例如 `.cursorrules`）或者 system prompt。

### 其他模型（Seedance、Kling、Sora、Runway、Midjourney…）

直接將 `SKILL.md` 當 system instruction 貼入去，然後用自然語言講你嘅場景。

---

## 語言版本

| 檔案 | 語言 | 說明 |
|---|---|---|
| 檔案 | 語言 | 說明 |
|---|---|---|
| `SKILL.md` | English | 主版本，建議用呢個 —— 大部份影片模型對英文 parse 得最好 |
| `SKILL_zh-CN.md` | 简体中文 | 想輸出簡體中文 Prompt 就用佢 |
| `SKILL_zh-TW.md` | 繁體中文 | 想輸出繁體中文 Prompt 就用佢 |
| `SKILL_ja.md` | 日本語 | 想輸出日文 Prompt 就用佢 |
| `SKILL_ko.md` | 한국어 | 想輸出韓文 Prompt 就用佢 |
| `SKILL_es.md` | Español | 想輸出西班牙文 Prompt 就用佢 |
| `SKILL_ar.md` | العربية | 想輸出阿拉伯文 Prompt 就用佢（RTL） |

> 電影術語（dolly in、whip pan、3-axis gimbal 等）喺所有版本都保留英文，
> 因為呢啲詞模型認得啲。

---

## 用法

```
你：一個古裝女子傍晚喺城牆上等人，等到天黑都未等到，最後轉身走。
```

Skill 會回你一個完整 Prompt，包含：

- 一條連貫嘅運鏡鏈（全景 → 甩鏡 → 特寫）
- 一組隨機抽到嘅微表情，直接寫咗入 Prompt
- 穩定器同燈光指示

睇 [`examples/before-after.md`](examples/before-after.md) 有三個完整示範。

---

## 用得好嘅貼士

- 🎲 **叫佢出 3 個 take。** 每次跑會抽到唔同嘅 A/B/C，揀最靚嗰塊面。
- 🗣️ **有心水情緒就直接講**；唔講就由 skill 按氛圍幫你揀。
- 📐 **講埋你想要嘅景別**（例如「最後要落到特寫」），skill 會設計條運鏡去到嗰度。
- 🎭 **係蒙太奇就明講**，skill 會正確咁掉晒所有運鏡語言。
- 🌏 預設輸出英文 Prompt（大部份影片模型 parse 得最好）。要中文／粵語輸出可以叫佢轉。

---

## 貢獻

歡迎 PR。最有價值嘅貢獻：

- 🎭 新增情緒大類（每種要附 3 個解剖學上明確唔同嘅變體）
- 🎥 新增運鏡 pattern
- 🌐 `SKILL.md` 嘅其他語言翻譯

---

## 授權

[MIT](LICENSE) —— 隨便用，注明出處就得。
