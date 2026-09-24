# 🎬 Cinematic Prompt Master（Español）

**Convierte una descripción de escena corriente en un prompt de imagen/video IA de grado cinematográfico — con movimiento de cámara intencional y microexpresiones faciales aleatorizadas.**

> Otros idiomas: [English](README.md) · [简体中文](README_zh-CN.md) · [繁體中文](README_zh-TW.md) · [日本語](README_ja.md) · [한국어](README_ko.md) · [العربية](README_ar.md)

---

## Por qué existe este skill

La mayoría de los prompts de video IA describen **qué hay en el encuadre**, pero nunca **cómo se mueve la cámara** ni **qué está haciendo realmente esa cara**.

El resultado es predecible:

- 📷 La cámara flota sin propósito — sin sujeto, sin razón para moverse
- 😐 Cada primer plano tiene la misma cara genérica de «llanto / sonrisa»
- 🔁 Ejecútalo diez veces, obtendrás diez expresiones idénticas

**Cinematic Prompt Master** resuelve ambos problemas. Cada prompt pasa por dos filtros:

1. **Revisión del movimiento de cámara** — intencional, con oclusiones, estable en 3 ejes, con sensación de ensayo
2. **Inyección facial doblemente aleatoria** — 20 emociones × 3 variantes = 60 estados faciales muestreados al azar

---

## Las dos reglas centrales

### 1. Reglas de movimiento de cámara (Camera Movement Rules)

| Principio | Qué significa |
|---|---|
| **Movimiento intencional** | La cámara fija un sujeto claro. Si el sujeto cambia, describe «el plano transiciona suavemente». |
| **Transiciones por oclusión** | Usa un whip pan, o deja que una columna, un transeúnte o un cuerpo bloqueen la lente un instante para ocultar el corte. |
| **Dolly + boom mezclados** | Combina dolly in / out con boom / crane, y cambia la escala del plano al cambiar el espacio (plano general → primer plano). |
| **Estabilidad visual** | Por defecto, gimbal de 3 ejes o slider. Sin temblores que provoquen náuseas. |
| **Bloqueo coreografiado** | Cámara, bloqueo de actores e iluminación con alta sensación de ensayo: un plano continuo sin errores. |

> **Excepción:** el montaje y el collage estático — **no necesitan ninguna descripción de movimiento de cámara**.

### 2. Inyección facial de doble aleatoriedad

- **Primera capa** — elige 1 categoría emocional según el ambiente de la escena
- **Segunda capa** — elige **una al azar** de las variantes **A / B / C** de esa emoción (está prohibido usar siempre la misma)

### Las 20 categorías emocionales

`Ira` · `Tristeza` · `Miedo` · `Asco` · `Desprecio` · `Ansiedad` · `Vergüenza` · `Culpa` · `Celos` · `Alegría verdadera` · `Sonrisa falsa` · `Satisfacción` · `Conmoción` · `Sorpresa` · `Confusión` · `Escepticismo` · `Concentración` · `Supresión` · `Soberbia` · `Apuro`

Cada una con 3 variantes anatómicamente específicas (cejas, párpados, pupilas, filtrum, pliegues nasolabiales, mentoniano…) — 60 estados en total.

---

## Instalación

### Claude Code / Claude.ai

```bash
mkdir -p ~/.claude/skills/cinematic-prompt-master
cp SKILL.md ~/.claude/skills/cinematic-prompt-master/SKILL.md
```

### Cursor / Windsurf / otros agentes

Pega el contenido de `SKILL.md` en el archivo de reglas del proyecto (p. ej. `.cursorrules`) o en el system prompt.

### Cualquier otro modelo (Seedance, Kling, Sora, Runway, Midjourney…)

Simplemente pega `SKILL.md` como instrucción de sistema y describe tu escena en lenguaje natural.

---

## Versiones de idioma

| Archivo | Idioma | Nota |
|---|---|---|
| `SKILL.md` | English | Versión principal — recomendada, la mejor interpretada por la mayoría de modelos de video |
| `SKILL_zh-CN.md` | 简体中文 | Si quieres prompts en chino simplificado |
| `SKILL_zh-TW.md` | 繁體中文 | Si quieres prompts en chino tradicional |
| `SKILL_ja.md` | 日本語 | Si quieres prompts en japonés |
| `SKILL_ko.md` | 한국어 | Si quieres prompts en coreano |
| `SKILL_es.md` | Español | Si quieres prompts en español |
| `SKILL_ar.md` | العربية | Si quieres prompts en árabe |

> Los términos de cinematografía (dolly in, whip pan, 3-axis gimbal…) se mantienen en inglés en
> todas las versiones, porque los modelos reconocen estos tokens de forma más fiable.

---

## Uso

```
Tú: Una mujer con vestimenta antigua espera a alguien en la muralla al anochecer.
    Cae la noche y él no llega; ella se da la vuelta y se marcha.
```

El skill devuelve un prompt completo que incluye:

- Una cadena de movimientos de cámara continua (plano general → whip pan → primer plano)
- Una microexpresión muestreada al azar, escrita directamente en el prompt
- Indicaciones de estabilizador e iluminación

En [`examples/before-after.md`](examples/before-after.md) hay tres ejemplos completos.

---

## Consejos para obtener mejores resultados

- 🎲 **Pide 3 tomas.** Cada ejecución muestrea una variante A/B/C distinta: elige la mejor cara.
- 🗣️ **Di la emoción en voz alta** si ya tienes una en mente; si no, el skill la elegirá según el ambiente.
- 📐 **Nombra la escala del plano** («quiero que termine en un primer plano») y el skill diseñará el movimiento para aterrizar ahí.
- 🎭 **¿Es un montaje?** Diló explícitamente: el skill eliminará correctamente todo el lenguaje de cámara.
- 🌏 La salida es en inglés por defecto (la mejor interpretada por la mayoría de modelos de video). Pide español si lo necesitas.

---

## Contribuciones

Se aceptan pull requests. Las contribuciones de mayor valor:

- 🎭 Nuevas categorías emocionales (cada una con 3 variantes anatómicamente distintas)
- 🎥 Nuevos patrones de movimiento de cámara
- 🌐 Traducciones de `SKILL.md` a otros idiomas

---

## Licencia

[MIT](LICENSE) — haz lo que quieras, se agradece la atribución.
