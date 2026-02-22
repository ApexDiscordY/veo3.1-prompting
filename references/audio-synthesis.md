# Native Audio Synthesis

Veo 3.1 generates synchronized audio including dialogue, ambient sound, and effects. No external tools required.

## Audio Capabilities

- **Dialogue**: Character speech with emotional tone
- **Ambient**: Environmental background (weather, crowds, nature)
- **Foley**: Object interaction sounds (footsteps, impacts, mechanisms)
- **Music**: Instrumental score synchronized to action

## Dialogue Best Practices

**Voice Specification**
Describe voice qualities for consistency:
- `Smooth baritone narration`
- `Crisp female voice with slight rasp`
- `Elderly man with gravelly texture`
- `Child's voice, excited and high-pitched`

**Timing Control**
Sync dialogue to visual beats:
- "At 2-second mark, character says: 'We need to move.'"
- "Dialogue begins after door closes: 'Did you hear that?'"
- "Overlapping conversation: Character A starts at 1s, Character B interrupts at 3s"

**Length Limits**
Keep dialogue brief for clarity:
- **Optimal**: 1-2 short sentences per 8-second clip
- **Maximum**: 10-12 words for single utterance
- **Pauses**: Specify breathing room: "Pause for 1 second, then continue"

## Ambient Sound Design

**Layering Strategy**
Build audio in layers:
1. **Base layer**: Continuous ambience (wind, room tone, traffic)
2. **Mid layer**: Specific environmental (birds, distant conversation, machinery)
3. **Top layer**: Synced effects (footsteps, object handling, impacts)

**Examples:**
- "Base: gentle forest wind. Mid: distant bird calls. Top: rustling leaves as character passes."
- "Base: cafe air conditioning hum. Mid: murmured conversations. Top: ceramic cup on saucer at 4s."

## Sound Effects (Foley)

**Timing Precision**
Match sounds to visual impacts:
- "Sound of high heels on marble, echoing, matching footfalls exactly"
- "Satisfying mechanical keyboard clack at 2s, 3s, and 5s"
- "Heavy door slam with reverb at 6s"

**Texture Words**
Use descriptive texture for better generation:
- `Satisfying pop` — Seals, bubbles, corks
- `Metallic scrape` — Swords, machinery, sliding metal
- `Organic crunch` — Leaves, snow, vegetables
- `Wet impact` — Water, mud, blood (use tastefully)
- `Digital chirp` — Electronics, futuristic UI

## Music Generation

**Style References**
- `Epic orchestral trailer music`
- `Lo-fi hip hop beat 80bpm`
- `Tense ambient drone`
- `Uplifting acoustic guitar`
- `Cyberpunk synthwave 120bpm`

**Dynamic Instruction**
Sync music to narrative:
- "Music starts minimal, builds at 4s, crescendo at 7s"
- "Sting at impact moment (3s), then silence"
- `Diegetic` — Music coming from source in scene (radio, car stereo)
- `Non-diegetic` — Background score only

## Audio Limitations & Workarounds

| Limitation | Solution |
|------------|----------|
| Text intelligibility | Keep dialogue short; Veo text often sounds like "nonsense" if too long |
| Voice consistency | Use identical voice descriptions across clips; consider post-production voiceover for series |
| Lip sync precision | Describe "mouth moving in sync" but expect approximate alignment |
| Complex music | Request simple melodic lines over complex harmonies |

## Audio Prompt Examples

**Full Audio Design:**
> Dialogue: Smooth baritone narrator says "The journey begins." Ambient: Desert wind whistling. Effects: Sand shifting under boots at 2s, 4s, 6s. Music: Sparse western guitar, lonely, distant.

**Action Scene:**
> Effects: Sword unsheathing (metallic ring at 1s), clash at 3s, grunt at 4s. Ambient: Echoing stone chamber. Music: Intense percussion building to hit.

**Product Demo:**
> Effects: Satisfying packaging tear at 2s, click at 4s. Ambient: Clean studio silence. Music: Minimal, elegant, premium brand aesthetic.
