---
name: veo-3.1-prompting
description: Expert guidance for Google Veo 3.1 video generation. Use when the user wants to (1) create text-to-video or image-to-video prompts, (2) optimize for cinematic quality and native audio syncing, (3) maintain character consistency via reference images, (4) structure multi-shot sequences with timestamp prompting, (5) use First/Last Frame interpolation, (6) select between standard and fast generation modes, or (7) troubleshoot physics, motion, or audio issues in generated video.
---

# Veo 3.1 Prompting

## Core Capabilities

Veo 3.1 generates video with native audio synthesis and advanced physical realism. Key specifications:

- **Resolutions**: 720p, 1080p, or 4K
- **Aspect Ratios**: 16:9 (landscape) or 9:16 (portrait)
- **Duration**: 4, 6, or 8 seconds per generation (billed as 8s minimum)
- **Framerate**: 24 FPS (cinematic standard)
- **Native Audio**: Dialogue, ambient sound, and music synchronized to video
- **Reference Images**: Up to 3 images for character/style consistency ("Ingredients to Video")
- **Advanced Controls**: First/Last Frame interpolation, Timestamp Prompting for multi-shot narratives

## The Five-Part Formula

Structure every prompt in this order:

**[Cinematography] + [Subject] + [Action] + [Context] + [Style & Audio]**

**Example:**
> Tracking shot following a weathered fisherman mending nets on a wooden dock. Golden hour sun flares through rigging. Salt spray visible in air. Cinematic 35mm film grain. Sound: seagulls crying, rope creaking, gentle waves.

**Critical:** Lead with camera movement. Veo 3.1 weights early tokens heavily.

## 1. Cinematography Specifications

Always specify shot type, camera movement, and lens characteristics first.

**Shot Framing**
- `Extreme close-up`, `Close-up`, `Medium shot`, `Wide establishing shot`
- `Over-the-shoulder`, `POV`, `Bird's eye view`, `Worm's eye view`

**Camera Movement** (See [camera-techniques.md](references/camera-techniques.md))
- Linear: `Dolly in/out`, `Tracking shot`, `Pan`, `Tilt`, `Truck`
- Dynamic: `Handheld`, `Gimbal smooth`, `Whip pan`, `Rack focus`
- Aerial: `Drone descending`, `Orbit clockwise`, `Crane up`

**Lens & Focus**
- `Shallow depth of field with creamy bokeh`
- `Deep focus everything sharp`
- `Anamorphic lens with horizontal flares`
- `Macro lens for extreme detail`

## 2. Subject Specification

Describe subjects with exhaustive visual detail for consistency:

**Character Anchors** (Essential for multi-clip consistency)
- Physical: "Elderly man, silver hair cropped short, weathered face with scar above left eyebrow"
- Clothing: "Faded navy pea coat, brass buttons tarnished, wool scarf with fringe"
- Distinctive markers: "Red-rimmed glasses", "tattoo of anchor on forearm", "gold pocket watch chain"

**Object Details**
- Material and condition: "Brushed titanium, fingerprint-smudged", "distressed leather with patina"
- Interaction points: "Steam rising from ceramic rim", "condensation beads on cold glass"

## 3. Action & Physics

Use dynamic verbs demonstrating physical interaction:

- **Motion quality**: `strides confidently`, `shuffles nervously`, `explodes outward`, `cascades smoothly`
- **Physics indicators**: `realistic water displacement`, `accurate gravity`, `cloth simulation`, `hair physics`
- **Temporal markers**: `gradually accelerating`, `suddenly freezing`, `continuously swirling`

**Physics Strengths**: Fluid dynamics, fire/smoke, fabric movement, particle systems (dust, snow, sparks).

## 4. Context & Atmosphere

Establish environment and mood:

**Lighting**
- Time: `dawn blue hour`, `golden hour`, `harsh midday`, `neon-lit night`
- Quality: `volumetric god rays`, `chiaroscuro shadows`, `soft diffused overcast`, `practical lamp light`
- Effects: `lens flare`, `bloom`, `atmospheric haze`

**Environment**
- Spatial: `cramped interior`, `vast open landscape`, `claustrophobic corridor`
- Weather: `rain-streaked windows`, `fog-choked streets`, `snow-dusted`

## 5. Style & Audio Synthesis

**Visual Style** (See [style-reference.md](references/style-reference.md))
- Genre: `cinematic noir`, `BBC Earth documentary`, `Pixar 3D animation`, `vintage 16mm`
- Color: `teal and orange blockbuster grade`, `bleach bypass desaturated`, `vibrant anime saturation`
- Texture: `film grain 35mm`, `digital sharpness`, `VHS tracking lines`

**Native Audio** (See [audio-synthesis.md](references/audio-synthesis.md))
- Dialogue: "Smooth baritone voice: 'The package has arrived.'"
- Ambient: "Coffee shop murmur, ceramic cup placed on saucer"
- Effects: "Satisfying mechanical keyboard clack", "metallic slide and lock"
- Music: "Tense strings building to crescendo", "lo-fi hip hop beat 80bpm"

**Audio Sync Tips**
- Time dialogue: "At 2-second mark, character speaks"
- Match motion: "Music swells as camera pushes in"
- Layer sounds: "Base ambiance, then specific Foley, then dialogue"

## Advanced Workflows

### Ingredients to Video (Character Consistency)

Use when maintaining characters across multiple clips:

1. Upload 1-3 reference images (character face, outfit, environment)
2. Prompt structure: "Same woman from reference image, now walking through rainy Tokyo street. Maintaining red leather jacket and bob haircut."
3. Keep anchors consistent: "Same scar on cheek, same gold hoop earrings"

### First & Last Frame Interpolation

Create specific transitions:

1. Describe starting state: "Sealed envelope on mahogany desk"
2. Describe ending state: "Open envelope, letter partially pulled out, handwritten text visible"
3. Veo generates smooth 8-second transition between states
4. Use for: reveals, transformations, camera moves through portals

### Timestamp Prompting (Multi-Shot Narrative)

Break 8 seconds into precise segments for narrative control:
