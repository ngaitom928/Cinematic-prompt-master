# 輸入 → 輸出 實例

三個完整示範，展示兩條核心規則點樣運作（包括「蒙太奇唔使運鏡」嘅例外情況）。

---

## Example 1 — 古裝 · 城牆等待（動態連續場景）

### 📝 用戶輸入

> 一個古裝女子傍晚喺城牆上等人，等到天黑都未等到，最後轉身走。

### 🎯 分析

- 動態連續場景 → **需要運鏡**
- 情緒大類：**Sadness（悲傷）**
- 第二層隨機抽樣 → 今次抽中 **B**

### ✅ 輸出 Prompt

```
Cinematic continuous shot, dusk on an ancient city wall.

Opening: wide shot. A woman in flowing ancient costume stands alone against
a vast indigo sky, wind pulling at her sleeves. 3-axis gimbal, rock steady.

Camera move: slow dolly in from the wide, the frame tightening toward her
back. As she begins to turn, a hanging lantern swings through frame and
occludes the lens for a single beat — whip pan on the reveal, the camera
now locked on her face from the front, shot scale shifted to a medium
close-up. Choreographed blocking: she turns exactly as the lantern clears,
warm lantern light catching her cheekbone at the same instant.

Facial close-up: her double-eyelid lines look lifeless from heavy eyelids,
the eye sockets slightly bloodshot, the mouth corners drawn into a tight
inverted arc. She holds the expression for two seconds, then looks away.

Closing: the camera booms up and dolly out in one motion, leaving her
small against the empty wall as night falls.

Warm-to-cold color grade, shallow depth of field, 35mm anamorphic look,
no handheld shake.
```

---

## Example 2 — 現代戀愛日常 · 第一人稱（動態連續場景）

### 📝 用戶輸入

> 第一人稱視角，我喺咖啡店等佢，佢推門入嚟嗰刻我抬頭。

### 🎯 分析

- 動態連續場景，第一人稱 POV → **需要運鏡**（但要模擬人眼， stabilization 依然要穩定）
- 情緒大類：**True Joy（真心高興）**
- 第二層隨機抽樣 → 今次抽中 **C**

### ✅ 輸出 Prompt

```
First-person POV, cinematic one-shot, inside a warm cafe in the late afternoon.

Opening: the camera sits at eye level across a small table, coffee steam
drifting through the foreground. Gimbal-stabilized, no shake.

Camera move: subtly push in (dolly in) as the door chime rings. The camera
lifts — a gentle boom up, as if the person looked up from their phone.
A waiter crosses frame and briefly occludes the lens; on the whip pan past
him, the shot has already transitioned smoothly to the door, now a medium
shot. Continue dolly in until we land on her face in close-up.

Facial close-up: brows relaxed and lifted, the smile spreading from the eyes
to the mouth, showing completely symmetrical and relaxed facial lines.
Eyes brighten a half-second after the smile starts — the delay makes it real.

Ambient practical lighting only, golden rim light from the window, 50mm,
shallow focus, film grain.
```

---

## Example 3 — 蒙太奇 · 城市早晨（例外：唔使運鏡）

### 📝 用戶輸入

> 用蒙太奇講一個城市由清晨醒過嚟嘅過程。

### 🎯 分析

- 蒙太奇 / 靜態拼貼風格 → **唔加任何運鏡描述**
- 面部特寫未必適用；若某一條 shot 有人面，先至隨機抽一組

### ✅ 輸出 Prompt

```
Montage sequence — static, precisely composed frames. No camera movement
descriptions.

Shot A: extreme wide. Empty wet street before dawn, single streetlight still
burning, reflection doubling in the puddles.
Shot B: close-up, static. A bakery shutter rolling up, flour dust hanging in
the first light.
Shot C: close-up, static. An old man's hands wrapping a steaming bun.
Shot D: close-up of a face, static. Street vendor mid-yawn — facial: eyes
squint slightly, brows relaxed into a gentle arc, a soft, slightly tipsy
expression. (Contentment — variant B)
Shot E: extreme wide. The same street at full morning, crowds crossing,
the streetlight now off.

Hard cuts between every shot. Consistent cool-to-warm grade across the
sequence. No transitions, no whip pans, no camera motion.
```

---

## 重點對照

| | Example 1 | Example 2 | Example 3 |
|---|---|---|---|
| 運鏡 | Dolly in → 遮擋甩鏡 → Boom out | Dolly in → Boom up → 遮擋 → Close-up | ❌ 完全冇 |
| 情緒 | Sadness · B | True Joy · C | Contentment · B |
| 穩定器 | 3-axis gimbal | Gimbal-stabilized | 不適用 |

同一句輸入跑多次，第二層隨機抽樣會抽到唔同嘅 A / B / C，出到唔同嘅面 —— 呢個就係個 skill 防止「十次十個一樣」嘅關鍵。
