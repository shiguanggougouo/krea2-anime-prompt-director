# Time AI · Krea 2 Anime Prompt Director

![Krea 2](https://img.shields.io/badge/Krea-2-7C5CFF?style=flat-square)
![Version](https://img.shields.io/badge/version-1.6.0-111827?style=flat-square)
![Format](https://img.shields.io/badge/format-Agent%20Skill-0EA5E9?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-22C55E?style=flat-square)

[![English](https://img.shields.io/badge/lang-English-111827?style=flat-square)](README.md)
[![简体中文](https://img.shields.io/badge/lang-%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87-7C5CFF?style=flat-square)](README.zh-CN.md)
[![中文页面](https://img.shields.io/badge/%E5%9C%A8%E7%BA%BF%E9%A1%B5%E9%9D%A2-GitHub%20Pages-22C55E?style=flat-square)](https://shiguanggougouo.github.io/krea2-anime-prompt-director/)

A reusable agent skill that turns a short Chinese or English idea into a **complete, Krea 2-ready anime prompt** — with a faithful Chinese translation alongside it.

It does five things a generic "prompt enhancer" does not:

1. **Anchors character identity in visible evidence** — hair shape and arrangement, eyes and markings, silhouette, signature costume layers, colors and materials, props — selected for the framing you asked for.
2. **Rebuilds locations instead of naming them** — "World Martial Arts Tournament" becomes a raised pale-stone ring with a red boundary line, crowded stepped stands, painted posts, banners and a tiled entrance pavilion.
3. **Automatically fills an unspecified environment** — if you only give a character name, it picks a story-rich classic setting from that character's own anime, manga or game canon and describes the actual scenery.
4. **Keeps repeat requests distinct** — when the same character comes back in a conversation, both the setting/story beat and the action change.
5. **Stages action and interaction** — one decisive instant with intent, weight, direction of force and a visible consequence in the scene; with several characters, a readable exchange of who initiates, who responds, and where eyelines and contact land. Never "dynamic pose" or "fighting pose."

It is grounded in the two official Krea anime guides plus an evidence-aware workflow for the community Krea2 Character Catalog.

---

## Quick start

### Install

Drop the whole folder into the skills directory your agent reads. Keep `SKILL.md` and `references/` together — the references are loaded on demand, so do not split them up.

```bash
# Codex / repo-local
git clone https://github.com/shiguanggougouo/krea2-anime-prompt-director.git .agents/skills/krea2-anime-prompt-director

# WorkBuddy / Claude-style user-level
git clone https://github.com/shiguanggougouo/krea2-anime-prompt-director.git ~/.workbuddy/skills/krea2-anime-prompt-director
```

### Use

Just describe what you want and let the skill do the work:

```
用 krea2-anime-prompt-director 扩写：旗木卡卡西
```

```
Use krea2-anime-prompt-director: Sailor Moon, classic moonlit scene
```

```
用 krea2-anime-prompt-director：京都动画风格，雨后的日本高中教室，不要人物
```

### Output

Only two sections — nothing else, no process notes:

```
POSITIVE:
A cinematic 2D shonen-anime key illustration of Hatake Kakashi from Naruto, identifiable by his
unruly silver hair swept into sharp spikes, a Leaf forehead protector slanted over his left eye,
one relaxed visible eye, the black mask covering his nose and mouth, and the high collar and
segmented pockets of his green flak jacket over a dark undersuit. He sits sideways on the curved
ridge of a tiled rooftop in the Hidden Leaf Village, casually reading a small orange-covered
paperback...

中文对照：
一幅具有电影感的二维少年热血动漫关键插画，描绘《火影忍者》中的旗木卡卡西。他蓬松的银发向上分成
清晰尖束，木叶护额斜压在左眼上方，一只放松却警觉的眼睛露在外面，黑色面罩遮住鼻子和嘴……
```

---

## What makes it different

| Generic prompt helper | This skill |
|---|---|
| Stacks Danbooru tags and quality macros (`masterpiece`, `8k`, `best quality`) | Writes connected natural-language prose — tags only if you explicitly ask for a tag list |
| Leaves the background as "in a room" or "outdoors" | Picks a canon setting and describes architecture, materials, scale, light and weather |
| Writes "at the World Martial Arts Tournament" and expects the model to know it | Converts the proper noun into a drawable physical layout with recognizable identifiers |
| Reuses one default outfit for every scene | Resolves the character's **story-moment version** first — arc, location, role, transformation |
| Same character, same pose, same place every time | Tracks used scene/action pairs and varies both on repeat requests |
| "Dynamic pose", "fighting pose", figures lined up side by side | One drawable instant with body mechanics, force direction, environment response — and for groups, a real exchange with distinct roles and reactions |
| Claims "I checked the catalog" | Only claims a catalog lookup if an entry was genuinely inspected |

---

## Changelog

Version history lives in [CHANGELOG.md](CHANGELOG.md) — 1.0.0 through 1.6.0, each entry describing the generation problem it fixed.

## Files

| File | What it holds |
|---|---|
| `SKILL.md` | Core behavior, workflow, and required output format |
| `references/action-direction.md` | Action staging and character interaction: one decisive instant, body mechanics, environment response, multi-character exchange |
| `references/style-language.md` | Style-selection matrix, scene-design language bank, prompt scaffolds |
| `references/examples.md` | Full EN/CN examples — character scenes, action, environment-only, variant selection |
| `references/catalog-workflow.md` | How to use Krea2 Character Catalog entries without overstating reliability |
| `references/source-notes.md` | Source URLs, source-derived findings, verification boundaries |
| `docs/index.html` | Project landing page (GitHub Pages source, Chinese/English toggle) |
| `CHANGELOG.md` | Version history from 1.0.0 to 1.6.0 |
| `README.zh-CN.md` | Chinese edition of this README |

## Built-in style anchors

One dominant anchor per prompt, at most one bounded twist:

- Studio Ghibli aesthetic — hand-painted watercolor, restrained natural palette
- Makoto Shinkai / CoMix Wave Films — hyper-saturated sky, cloud edges, urban light
- Kyoto Animation — warm window light, delicate linework, lived-in detail
- Madhouse / urban-noir — cool blue-green, wet asphalt, sodium-yellow accents
- 1990s Sunrise / classic OVA mecha — hard-edged cel shading, industrial backgrounds
- Shoujo register / Seinen register
- Classic battle-shonen cel-animation

## Honest limits

- The skill does **not** bundle the Krea2 Character Catalog dataset and does not claim to query it automatically. It uses an accessible entry, export or provided file when one is there, and continues honestly when it is not.
- Catalog entries are **provisional**. A match is useful evidence, not proof of canon and definitely not proof that a character exists in Krea 2's training data.
- Prompt text alone cannot guarantee perfect character continuity across a series. For that, use a Krea 2 style reference or a mood board of roughly 20–40 frames.

## Sources

- [Anime Backgrounds with Krea 2](https://www.krea.ai/blog/anime-backgrounds-with-krea-2) — Krea official
- [Studio Anime Aesthetics with Krea 2](https://www.krea.ai/blog/studio-anime-aesthetics-with-krea-2) — Krea official
- [Krea2 Character Catalog](https://github.com/ukr8b3g-cmyk/Krea2-Character-Catalog) — community project
- [Agent Skills format](https://developers.openai.com/api/docs/guides/tools-skills) — OpenAI

## License

MIT — see [LICENSE](LICENSE).
