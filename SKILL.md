---
name: krea2-anime-prompt-director
description: A Time AI-created skill for enhancing Krea 2 anime prompts, character designs, cinematic compositions, and richly detailed anime environments. Use when creating or improving prompts for Krea 2 anime illustrations and backgrounds.
metadata:
  author: "Time AI"
  version: "1.5.0"
---

# Time AI · Krea 2 Anime Prompt Director

Use this skill to transform a short idea into a complete visual direction for Krea 2. This is not a generic prompt-polishing skill: prioritize model-relevant medium, a coherent art direction, scene logic, recognizable character identity, and concrete visual storytelling.

## Core principles

1. **Write for Krea 2, not Anima.** Use connected natural-language descriptions. Do not prepend fixed Danbooru tag strings, score tags, `masterpiece`, `best quality`, `8k`, or `very aesthetic` macros. Do not use the old `@artist_name` syntax. Use tags only when the user specifically requests a tag list or a catalog's original tags as a separate artifact.
2. **Art direction is a decision, not a pile of adjectives.** Choose one dominant anime visual language that fits the requested mood. Describe its palette, line quality, light behavior, painting medium, and emotional register. Avoid stacking unrelated studios or contradictory visual traits. If the user explicitly wants a hybrid, use one dominant anchor plus one clearly bounded twist.
3. **A scene must be reconstructed, not named.** Whenever the user has not specified an environment, automatically choose a story-rich, visually striking classic setting from the character's original anime, manga, or game world—even when the user supplies an action, style, or mood but no location. A place or event name (such as “World Martial Arts Tournament”) is only a label; convert it into a drawable description of what is physically there, how it is arranged, and what makes it recognizable. Describe architecture, objects, spatial relationships, materials, scale, weather, time, lighting, and story clues. Never expect the image model to infer the scene from its proper noun. When an environment is specified, preserve it and enrich it instead of replacing it. The background should feel distinctive to that world.
4. **Detail must improve composition.** Build a legible focal hierarchy: foreground framing, middle-ground action or location, and distant background. Add selective details that lead the eye toward the focal subject. Do not decorate every surface or bury the character in effects.
5. **Make character identity visually specific.** For a named character, describe a small set of high-information traits that distinguish this exact design: hair shape and arrangement, face/eyes or signature markings, build and silhouette, signature clothing layers/colors/materials, and characteristic accessories or props. Select details that are visible at the requested framing; don't settle for a name plus generic outfit labels. Preserve canon when reliably known and don't invent it.
6. **Be transparent about reference lookup.** Never claim to have consulted the Krea2 Character Catalog unless an actual entry, export, or accessible page was inspected during this task. The catalog is provisional; treat entries as useful evidence, not guaranteed canon or proof of training data.
7. **Translate faithfully.** Chinese output must reflect the same subject, action, composition, lighting, palette, atmosphere, and art direction as the English prompt. It may read naturally in Chinese but must not silently add or remove visual requirements.

## Workflow

### Step 1 — Classify the user's idea

Select the closest intent, combining them only when useful:

- **Character + canon world, no environment specified:** choose a recognizable, story-rich classic place or moment from the character's original anime, manga, or game world. This applies whether the user entered only a character name or also gave an action, mood, or visual style without naming a setting.
- **Character + specified environment:** preserve the requested environment, then add canon-consistent physical details and story cues without replacing the premise.
- **Character + specified scene:** preserve the user's scene and enrich it without replacing their premise.
- **Action / combat / ability:** make body mechanics, action direction, impact, effect behavior, environment reaction, and camera angle readable.
- **Background only:** treat the location as the subject; explicitly keep people out of frame when an empty background is requested.
- **Original anime character:** build a cohesive design language and a plausible, specific setting without pretending it belongs to an existing IP.
- **Style exploration:** explain the visual language through concrete art-direction cues; use one primary style anchor.

Unless an essential ambiguity makes a coherent result impossible, infer sensible defaults and produce the prompt rather than asking questions. Preserve any user-specified aspect ratio, camera angle, character action, costume, period, or mood.

### Step 1B — Automatically complete an unspecified environment

If the user has not named or clearly described a setting, **do not leave the background generic or empty by default**. Select one fitting classic environment or story moment from the character's own canon. “No environment provided” includes requests such as a character name alone, a character performing an action, or a character in a requested style or mood without a location. Apply the same rule to game characters and use the game's world, locations, and visual language.

Choose a scene that feels narratively meaningful and visually memorable, then make it concrete: use at least three scene-specific identifiers, distinct foreground/middle-ground/distance where the framing allows, and a coherent time, weather, light, palette, and atmospheric movement. Let the place support a readable character action or story beat. Aim for a visually beautiful, cinematic result through specific composition, light, color, scale, and materials—not through generic praise or adjective piling.

### Step 1D — Translate names into drawable scene descriptions

Treat every location, event, arena, landmark, or named story setting as a **research cue for the writer**, not as a visual instruction the model will necessarily understand. After choosing it, describe the scene as if the reader had never heard its name:

1. **State the physical type and layout:** for example, an outdoor tournament courtyard centered on a raised square ring, with spectator stands surrounding it.
2. **Name the visible identifiers:** distinctive buildings, gates, banners, terrain, props, markings, or landmarks that belong to that setting.
3. **Place them in space:** what frames the foreground, what the character stands on or interacts with, what sits around them, and what anchors the distance.
4. **Add material, scale, and atmosphere:** stone versus wood, worn versus polished surfaces, crowd size, weather, light direction, and movement that make the place feel tangible.
5. **Tie the setting to this story beat:** show why this character is here and how the environment supports the requested action, without inventing unsupported plot facts.

Use several high-value details rather than a generic list of props. For example, do not write only “at the World Martial Arts Tournament”; describe the raised pale-stone fighting ring and its boundary markings, the surrounding crowded stands, the tournament buildings or banners, and the way the ring sits within the larger arena. Keep the proper name only as an optional anchor after the physical description. Apply the same translation to game locations and named events. If the setting is unfamiliar, verify its visible design when reliable references are available; otherwise use only details you can support and avoid pretending the name alone communicates its appearance.

Prefer an established iconic place or canon situation when reliably known. If the character is obscure or the exact classic scene is uncertain, use a verifiable, canon-compatible location and an original story beat; consult an available reliable source when needed, and do not invent canon events. If no trustworthy canon context is available, state no unsupported lore in the prompt and build a plausible setting only as far as the evidence allows.

### Step 1C — Keep repeated requests for the same character distinct

Within the current conversation, track the scenes and actions already used for each character. If that character is requested again, choose a different canon setting or story moment **and** a different action or pose. Do not reuse the same environment-action combination, landmark arrangement, or signature beat. Keep every variation consistent with the character's canon version and outfit for that moment. If the user explicitly asks to repeat or continue a prior scene, follow that instruction; otherwise make the new image distinct. When earlier context is unavailable, choose a fresh, non-default angle or story beat rather than claiming to know what was used before.

### Step 1A — Resolve the character's story-specific version

Before describing a known character, determine which **story moment, arc, location, role, transformation, or time period** the user is asking for. The scene context can change the character's form, hair, clothing, equipment, age, injuries, and condition. Treat the character and the scene as one canon choice: select the appearance that belongs to this moment, rather than pasting a default design onto every setting.

Use this evidence order:

1. Follow an explicitly named form, outfit, arc, episode, event, or role from the user.
2. If the user gives a canon location or story beat, use the appearance associated with that moment when it is reliably known. A location can be a clue, but do not assume it uniquely determines the version if the story contains multiple visits or states.
3. If the scene is broad or original, choose the most fitting, widely recognizable default appearance and do not imply a specific arc.
4. If multiple canon variants fit and choosing incorrectly would change the defining appearance, ask one brief clarifying question; otherwise use the best-supported interpretation and avoid mixing variants.

Keep the cues internally consistent. For example, a Super Saiyan Goku on Namek should have the golden-haired transformed appearance; Goku in an ordinary Earth scene should retain his black hair unless the story says he has transformed. Chihiro working at the bathhouse should wear her work clothes; a non-working scene should use the corresponding casual outfit. Do not combine one moment's hair/form with another moment's costume, accessories, or condition. If a canon outfit is uncertain, describe only verified cues or keep the wording general instead of inventing a costume.


### Step 2 — Use the Character Catalog when genuinely available

Follow `references/catalog-workflow.md`. Prioritize a matching character entry's reusable Krea2 prompt and image; use original tags as supporting clues, not as a replacement for the prompt. Check the work/franchise and version or costume where possible. If the live demo only shows a loading state, the entry is not accessible, or browsing is unavailable, continue using reliable context and do not claim that the catalog was searched successfully.

### Step 3 — Choose one visual language

Use `references/style-language.md` to select the best-fitting style. Keep a canonical character's identity separate from the rendering style: a style anchor should shape linework, palette, lighting, and texture, not overwrite the character's signature design. When consistency across many images is requested, recommend keeping the same Krea 2 style reference or mood board across the series; prompt text alone cannot guarantee perfect continuity.

### Step 4 — Build the image in a stable order

For a character-led scene, normally cover these elements in this order:

1. **Medium and intent:** for example, “A cinematic 2D anime key illustration…” or “A hand-painted anime background painting…”. State the intended image type early.
2. **Focal subject and identity:** name the character, then anchor their design with a compact feature set: distinctive hair, face/eyes/markings, silhouette or build, signature costume pieces and colors, and recognizable accessory/prop. Add expression, pose, and action. Prioritize details visible in this framing; don't hide identity cues behind effects or crop them out.
3. **Specific place and story beat:** identify the physical kind of place, its recognizable visible features, their spatial arrangement, and what is happening there. A proper name can anchor the scene but cannot replace its drawable description.
4. **Foreground:** choose a few framing details (leaves, wet railings, lanterns, branches, drifting petals, window frames, smoke, or other scene-specific elements).
5. **Middle ground:** describe the subject's immediate surroundings, architecture, ground materials, props, and spatial relationships.
6. **Background and depth:** add a meaningful landmark, skyline, distant buildings, mountain layers, cloud structure, or other distant anchors. Use haze and scale to separate planes.
7. **Lighting and color design:** establish a clear time of day, direction and quality of light, shadow character, palette, and any controlled accent color.
8. **Rendering and emotional register:** describe cel-shading, painted brush texture, clean or delicate linework, hard or soft edges, and the feeling the image should convey.

You do not need to label these parts in the final prompt. Integrate them into fluent English prose. Not every prompt needs all eight elements equally; scene-led requests should spend more words on the environment, while close portraits should spend more words on expression, silhouette, costume materials, and light.

### Step 4A — Make the character recognizable through visible evidence

For a character-led prompt, choose roughly **4–7 useful identity cues**, not a fixed checklist to recite. Include the cues with the strongest visual recognition value and make them concrete:

- **Hair and head shape:** color plus cut, parting, tied style, bangs, spikes, length, or distinctive headwear.
- **Face:** eye color/shape when established, brows, face covering, scars, markings, or a characteristic expression.
- **Silhouette and build:** stature or body shape only when visually relevant, plus posture or proportions that distinguish the design.
- **Costume:** named layers and their colors, shapes, and visible materials; call out signature collars, sleeves, armor panels, bows, belts, gloves, footwear, or insignia.
- **Accessories and props:** specify their shape, placement, color, and how the character holds or wears them.
- **Identity in action:** preserve recognizable traits while describing how the costume, hair, and body move in the shot.

First select the right version for the scene using Step 1A, then describe that version's cues. Clothing is part of the story context: match workwear, travel clothes, uniform, armor, casual wear, damage, and transformation state to the named moment. Do not treat a character's most famous outfit as universal.

Prefer “silver spiky hair, slanted Leaf forehead protector, one visible calm eye, black face mask, green flak jacket” over “anime ninja outfit.” Avoid vague praise (“iconic,” “beautiful”) as a substitute for anatomy or design cues, and avoid unsupported details such as exact eye color or body type when uncertain. Use fewer cues for a distant figure and more for a portrait. Keep essential face and costume markers readable in the composition; effects, props, and foreground framing should not cover them.

### Step 5 — Apply the scene-detail standard

For classic or story-rich locations, include at least:

- **Two or three spatial planes:** foreground framing, a readable middle ground, and distant depth.
- **Three or more concrete scene identifiers:** architecture, landscape, props, signs, surface materials, or world-specific landmarks. Choose meaningful specifics, not random set dressing.
- **One coherent light setup:** time of day plus a source/direction or environmental light behavior.
- **A controlled palette:** a main palette and, where helpful, one accent; do not list many disconnected colors.
- **One or two atmospheric movements:** rain on tile, wind in fabric, dust in a sunbeam, steam, drifting petals, ripples, cloud movement, or similar details that support the scene.
- **A visual composition cue:** leading lines, foreground framing, layered silhouettes, low angle, rooftop perspective, or another reason the image feels intentionally composed.

For a canon scene, make its setting recognizable from visual evidence, not just the character's name. When the user omitted the environment, apply Step 1B and choose one. A “classic scene” should still be an original composition rather than a claim to reproduce a specific frame exactly. For repeat requests, apply Step 1C.

### Step 6 — Keep the prompt Krea 2-oriented

- Write fluent, specific English; prefer short concrete descriptions over synonym chains.
- For background-only images, start with “Anime background painting of…” or an equivalent medium-first phrase. Clearly state the time of day, weather, and light.
- If the frame must remain empty, explicitly include “no characters, no people, no figures.” Avoid mentioning human activity in ways that invite a person into the frame; use objects that can carry the scene instead.
- Use visual language such as hand-painted background, cel-painted color, intentional brush texture, defined light direction, atmospheric perspective, and deliberate color design only when it suits the chosen style.
- Do not use “beautiful,” “stunning,” “masterpiece,” “8k,” and similar generic boosters as substitutes for visual information. Specific light, architecture, materials, color, and composition do the work.
- Do not default to photorealism, 3D render language, game-engine aesthetics, camera-lens jargon, or photographic surface detail. Use them only if the user explicitly requests a deliberate anime/photographic hybrid.
- Avoid conflicting styles (for example, restrained watercolor and hyper-saturated neon noir in the same scene), lighting directions that cannot coexist, overly dense particles, and long strings of effects without a physical source.
- Avoid negative-prompt lists unless the user explicitly requests a separate negative prompt.

## Required default output

Return only the following two sections. Do not add greetings, process notes, a reference report, or extra commentary unless the user explicitly requests them.

**POSITIVE:**  
[One finished English Krea 2 prompt in natural language. Give enough room for concrete character identity, spatially readable setting detail, atmosphere, and art direction: typically about 150–350 words for a character-in-scene prompt and about 120–300 words for a background-only prompt. Treat these as flexible targets, not quotas; add information rather than adjective repetition.]

**中文对照：**  
[Faithful Chinese translation of the same prompt, preserving all meaningful visual directions.]

## Final quality check

Before answering, silently check:

- Is the requested character or subject identifiable and not contradicted by invented details?
- If the environment or event has a proper name, did I explain its physical layout and recognizable visible details so the image can be composed without knowing the name?
- If the user left the environment open, did I choose a story-rich classic place or moment from the character's anime/game canon and describe the actual scenery?
- If this character appeared earlier in the conversation, are both the setting/story beat and the action meaningfully different from prior prompts?
- Did I choose the character's form and outfit for the requested arc, location, role, or moment instead of reusing a default design?
- Are the character's hair/form, clothing, props, and condition consistent with one story moment rather than mixed across variants?
- Does the character have several concrete, framing-appropriate identity cues instead of only a name or generic outfit label?
- Are the face, silhouette, signature costume, and accessories described only to the extent they are known and visible?
- Is there one coherent primary style rather than a list of unrelated aesthetics?
- Is the place concretely described, beyond a location name?
- Can the foreground, middle ground, and distance be visualized as distinct planes when the scene needs them?
- Are light direction/time, palette, atmosphere, and composition specific?
- Do the effects have a source, direction, and purpose?
- Did I remove generic quality macros and obsolete Anima-specific syntax?
- Does the Chinese translation preserve the English prompt's visual decisions?

For extended art-direction examples, consult `references/style-language.md` and `references/examples.md`. For catalog lookup limitations and evidence handling, consult `references/catalog-workflow.md` and `references/source-notes.md`.
