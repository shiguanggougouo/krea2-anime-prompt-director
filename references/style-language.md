# Krea 2 Anime Art-Direction Reference

This reference operationalizes the Krea team's two anime guides. The style names are visual anchors, not magic keywords: pair one anchor with concrete details about palette, linework, light, medium, and mood. When the user prefers a different style, follow the user's preference rather than forcing a studio label.

## Choosing a dominant look

| Direction | Useful visual language | Typical scene fit | Avoid diluting it with |
|---|---|---|---|
| **Studio Ghibli aesthetic** | Hand-painted watercolor feel, restrained natural palette, weathered rural wood and stone, lush layered greenery, soft midday light, gentle weather, subtle brush texture | Rural paths, old houses, forests, hills, quiet fantasy travel, warm pastoral settings | Hyper-saturated neon skies, hard noir shadows, excessive metallic gloss |
| **Makoto Shinkai / CoMix Wave Films aesthetic** | Hyper-saturated sky, intricate cloud edges, sun flare, electric orange/magenta at sunset, blue-hour gradients, telephone wires and poles as framing, luminous urban reflections | Tokyo rooftops, stations, streets after rain, twilight transitions, emotionally charged cityscapes | Muted watercolor restraint as the dominant palette; several competing style anchors |
| **Kyoto Animation aesthetic** | Bright yet gently melancholic, warm natural window light, precise delicate linework, lived-in interiors, small everyday objects placed with intention, soft but clear shadow structure | Classrooms, school hallways, cafés, bedrooms, club rooms, slice-of-life moments | Empty generic rooms with no object-level detail; harsh noir color unless requested as a twist |
| **Madhouse / urban-noir anime direction** | Cool blue-green palette, harder cel-shaded shadows, wet asphalt, urban density, sodium-yellow accent lights, grounded mature atmosphere, restrained linework | Night streets, alleys, rooftops, crime/thriller scenes, tense urban settings | Pastel softness and warm all-over lighting; adding too many accent colors |
| **1990s Sunrise / classic OVA mecha direction** | Hard-edged cel shading, bold linework, painted industrial backgrounds, strong mechanical silhouettes, dense but purposeful machinery detail, weighty shadows | Mecha hangars, industrial decks, classic sci-fi battle compositions | Soft watercolor fields or slick modern 3D-render wording |
| **Shoujo anime register** | Delicate contour lines, pastel or jewel-like accents, floral motifs, luminous soft light, elegant pose, carefully placed sparkles or petals | Romantic rooftop scenes, gardens, moonlit transformations, emotional close-ups | Excessive gritty texture or relentless hard shadows |
| **Seinen anime register** | Restrained linework, grounded city detail, mature mixed colors, a warm window against a cold blue night, controlled shadows, quiet tension | Apartment rooftops, late-night offices, streets, contemplative adult drama | Overly sugary pastel palette and decorative effects without narrative purpose |
| **Classic battle-shonen cel-animation** | Clear action silhouette, graphic shape design, bold cel-shaded forms, directional speed lines, explosive but readable energy shapes, high-contrast focal lighting | Signature attacks, duels, tournament stages, training scenes | Effects that obscure hand pose, weapon trajectory, face, or point of impact |

## Style-selection rules

1. Choose **one dominant style anchor**. For example, choose either a Ghibli-style painted countryside or a Shinkai-style saturated city dusk, not both at equal strength.
2. Add at most **one bounded variation** if the user asks for it, such as “a Shinkai-inspired sky with a more restrained color palette.” The descriptive twist should not cancel the anchor.
3. A named studio or director can help anchor the look, but the prompt still needs specific visual directions. For example, “Kyoto Animation aesthetic” should be supported by warm window light, delicate linework, and carefully selected lived-in objects.
4. For less familiar or niche styles, use an available style-reference image rather than pretending a studio label guarantees precise control.
5. If the user's goal is an identifiable existing character in a new scene, style affects the rendering, not the character's signature colors, silhouette, outfit, or props.

## Reference images and cross-image consistency

When the user is creating a series and Krea 2's interface supports the relevant controls:

- Use a **style reference** to pin a specific palette, cloud design, line weight, or painted texture for one visual target.
- For a larger series, a **mood board** made from around 20–40 references from the desired visual world can help maintain a shared palette, line weight, and atmosphere across different scenes.
- A reference image is a style guide, not a command to reproduce a specific copyrighted frame exactly. Use the reference to extract the visual language and construct an original composition.

## Scene-design language bank

Use only words that match the intended image. Pick a few precise details from relevant groups instead of appending every term.

### Spatial depth
- foreground leaves softly occluding one corner
- layered rooflines receding into pale evening haze
- a low stone wall guiding the eye toward the subject
- distant ridgelines separated by atmospheric perspective
- overhead power lines converging toward the horizon
- window frames forming a natural frame within the image

### Surface and material
- weathered cedar grain, rain-darkened ceramic roof tiles, chipped plaster, moss in stone joints
- brushed metal, scuffed enamel, worn wood, frosted glass, paper lanterns, hand-painted signage
- chalk dust on a blackboard, fine scratches on a desk, water beads on glass, softened ink edges

### Light
- warm late-afternoon shafts breaking through leaves
- cool skylight filling the shadow side of the subject
- window light falling in a long diagonal across the floor
- sunset color reflected beneath the cloud deck and in wet pavement
- thin rim light separating a silhouette from the distant skyline
- a lantern's small amber pool against a broad field of blue night

### Atmospheric movement
- wind lifting only the loose edge of a sleeve
- a few wet leaves pinned against the pavement
- fine dust becoming visible inside a sunbeam
- rainwater slipping from a roof edge into a shallow puddle
- drifting petals catching the backlight
- thin steam rising from a vending machine or street-food stall

### Composition cues
- low angle with the landmark held behind the shoulder
- foreground branches framing but not covering the face
- diagonal rooflines leading toward the subject's gaze
- broad negative space reserved for a luminous sky
- a clear silhouette separated from busy background shapes
- a quiet asymmetrical composition with the brightest area offset from center

## Useful prompt scaffolds

### Character-led scene

“A cinematic 2D anime key illustration of [character name in the version appropriate to this arc, place, role, or moment; concrete visible cues for that version's hair/form, face, silhouette, costume, and accessories], [specific action and expression that keep those cues readable], in [the user's specified environment, carefully enriched, or—if none was provided—a fitting classic environment/story moment from the character's anime or game canon]. Describe the location's physical layout and recognizable visible features; use its proper name only as a supporting anchor. In the foreground, [two or three framing details that do not obscure the face or signature design]. Around the character, [middle-ground structures, props, materials and spatial relationships]. Beyond them, [recognizable distant landmark and atmospheric depth]. [Time of day, light source/direction, palette and shadow behavior]. Rendered with [one coherent linework/painting/cel-shading direction], creating [specific emotional register]. For repeat requests, choose a different canon setting/story beat and action than those already used for this character in the current conversation.”

### Empty background

“Anime background painting of [specific location], [one style anchor]. [Time of day and weather]. In the foreground, [details framing the view]; across the middle ground, [specific empty structures and material details]; in the distance, [landmarks, skyline, hills or cloud layers]. [Light direction and palette]. [Brush/cel-painted surface qualities and atmosphere]. No characters, no people, no figures.”

### Action scene

“A dynamic 2D anime action key visual of [character] performing [specific technique]. The body is [readable pose mechanics], with [weapon/hand/foot direction] leading toward [point of impact]. [Energy/impact effect] radiates from [physical source] and interacts with [environmental surfaces]. [Foreground debris or framing], [mid-ground combat space], and [distant set or sky] create depth. [One coherent palette and cel-animation style].”
