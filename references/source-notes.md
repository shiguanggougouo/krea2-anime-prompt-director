# Source Notes and Verification Boundaries

Prepared on 2026-10-18. The instructions in this skill synthesize the sources below with general prompt-design judgment. When an instruction is directly grounded in a source, the note says so; additions about workflow and quality control are operational recommendations rather than quotes from the sources.

## 1. Krea official: Anime Backgrounds with Krea 2

URL: https://www.krea.ai/blog/anime-backgrounds-with-krea-2

The article describes anime backgrounds as a specific painting tradition: cel-painted color, mostly hand-drawn linework, deliberate brush texture, clear light direction, and atmospheric color decisions. It recommends naming the medium early, stating the time of day, explicitly excluding people for a clean background plate, using studio references sparingly, and avoiding generic AI-gloss words such as “beautiful,” “stunning,” “masterpiece,” and “8k.” It also describes the role of style references and mood boards in maintaining palette, cloud shapes, line weight, brush texture, and project consistency.

Applied in this skill: medium-first background prompts; concrete time/weather/light; explicit no-people language; one clear style anchor; foreground/middle-ground/distance; specific physical detail instead of generic boosters.

## 2. Krea official: Studio Anime Aesthetics with Krea 2

URL: https://www.krea.ai/blog/studio-anime-aesthetics-with-krea-2

The article emphasizes that anime is not a single look: studio aesthetics differ in palette, line weight, light, and emotional register. It describes Studio Ghibli's restrained watercolor/natural settings, Makoto Shinkai/CoMix Wave's saturated sky and urban light, Kyoto Animation's warm natural interiors and lived-in detail, Madhouse's cooler urban noir, 1990s Sunrise/classic OVA's hard-edged cel-shading and industrial palettes, plus shoujo and seinen visual registers. It advises choosing a single dominant studio look rather than stacking studio names, and suggests style references or a mood board of roughly 20–40 frames for stronger continuity.

Applied in this skill: an explicit style-selection step; a reference matrix; one main aesthetic with at most one controlled twist; consistent style-reference guidance for series projects.

## 3. Community project: Krea2 Character Catalog

Live demo: https://ukr8b3g-cmyk.github.io/Krea2-Character-Catalog/
Repository / README: https://github.com/ukr8b3g-cmyk/Krea2-Character-Catalog

The repository README describes a Krea2-generated character and style catalog with image samples, reusable Krea2 prompts, searchable tags, and an editor. It distinguishes reusable generation prompts from original-tag CSVs and provides the schema of the original-tag file (`tag`, `category`, `count`, `insert_mode`). The README for v0.9.6 states 3,809 accepted character images and 110 style images, 3,919 total. It explicitly labels the catalog incomplete and provisional and warns that manual review does not guarantee correct names, tags, likenesses, or a character's presence in training data. The README also notes that the GitHub Pages site is a simplified read-only static demo, while the full local release ZIP contains the larger image collection and data.

Applied in this skill: optional evidence-aware catalog lookup; prioritize the reusable Krea2 prompt plus image; use original tags as supporting clues; do not confuse tags with the final prompt; do not overclaim accuracy or training-data membership; handle the live demo's limits honestly.

## 4. OpenAI: Agent Skills format

URL: https://developers.openai.com/api/docs/guides/tools-skills

The official documentation describes a skill as a directory containing a `SKILL.md` manifest with YAML frontmatter and instructions, plus optional supporting references/assets. This package follows that structure and keeps extended matrices, source notes, and examples outside the main `SKILL.md` so the core workflow remains easier to load and maintain.
