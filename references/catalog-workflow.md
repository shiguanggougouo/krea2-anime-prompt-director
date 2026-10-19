# Krea2 Character Catalog: Evidence-Aware Workflow

Primary reference: https://ukr8b3g-cmyk.github.io/Krea2-Character-Catalog/
Repository / release notes: https://github.com/ukr8b3g-cmyk/Krea2-Character-Catalog

## What the catalog can contribute

The catalog is a collection of Krea2-generated character and style samples with searchable names/tags and reusable Krea2 prompts. The project README distinguishes several kinds of information:

- **Reusable Krea2 prompt:** the strongest first reference for how that sample was described for Krea2.
- **Original tags:** supporting identity, franchise/copyright, and appearance clues. These are a different data product from the final natural-language prompt.
- **Image sample:** visual evidence for the outfit, silhouette, color palette, pose, and resemblance of that particular entry.
- **Category/context:** character versus style, plus work/franchise and appearance information where present.

Use an entry to inform the requested character or style; do not copy its wording blindly when the user asked for a different action, scene, outfit, composition, or mood. Keep useful identity details, then construct a scene that fits the current request.

## Lookup procedure

1. If web access or a browser tool is available, open the live demo or repository linked above and try the canonical name and common English/Japanese/Chinese spellings. Search by franchise/copyright and outfit/appearance when needed.
2. Confirm the card is actually visible and inspect its sample image and reusable Krea2 prompt. Do not rely only on a search-result snippet or an empty/loading page.
3. If an available local catalog export or uploaded file is present, use its fields directly. Prefer the most relevant matching entry and retain the entry's version/context if known.
4. Use original tags to cross-check identity, hair/eyes, costume pieces, props, or variants. Avoid turning the whole tag list into a comma-separated final prompt.
5. Recompose for the user's intent. Keep the character identity and the scene direction distinct: the catalog may help with identity, while the current request controls action, location, lighting, style, and framing.
6. If there are conflicting entries, state no conflict-resolution claim in the final prompt; choose the best visual match based on image, name/franchise, outfit, and task. If uncertainty materially changes the character, choose a conservative depiction rather than inventing a fact.

## Important availability and accuracy limits

- The public GitHub Pages demo is a simplified, read-only static preview; the full local catalog ZIP contains the wider image collection and tag data. A demo page that only says “Loading…” or “no images available” has not yielded a usable entry.
- The published project describes the collection as incomplete and provisional. Its maintainer warns that names, tags, likenesses, and style assignments may be wrong and that acceptance does not prove the model saw a character during training.
- The README for v0.9.6 describes 3,809 accepted character samples and 110 accepted style samples (3,919 images total); those counts describe that specific release, not a guaranteed current live-demo count.
- Never infer that a character is “in Krea 2's training data” from a catalog result.
- Never say “I checked the catalog” unless you genuinely accessed the entry or user-provided export in the current task.

## When the catalog is unavailable

Proceed with the strongest reliable knowledge already available. For widely known characters, maintain distinctive visual features and place them in a plausible, recognizable location. For niche or ambiguous characters, avoid claiming exact canon details. Do not stop the task just because the optional catalog is unavailable, and do not fabricate a catalog citation or prompt.

## Keep lookup separate from final output

The default final answer remains only `POSITIVE` and `中文对照`. Do not add a catalog report unless the user asks for sources, validation, or an explanation of the choices. If asked for evidence, identify what was actually checked and separate it from inference.
