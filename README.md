# P2A3S2V

**P2A3S2V** · version **2026.8** · Studio & Stage performance keyboard

Created by **Parikshit Kumar Singh** and all family members.

A browser-based Web Audio keyboard for melody practice, bhajan accompaniment, live notation, and ensemble-style play — no install required.

---

## Quick start

1. Keep these files together:
   - `piano_app_html_java_script_web_audio.html`
   - `bhajans_db.js`
2. Open the HTML file in a modern browser (Chrome, Edge, Firefox, Safari).
3. Click or press a key once so the browser can start audio.
4. Play with the on-screen piano or computer keyboard.

Computer white keys (two octaves from the selected start C):

```text
z x c v b n m , q w e r t y
```

Black-key positions use nearby letter/number keys (`s d g h j` and `2 3 5 6 7`).

---

## What you can do (use cases)

### 1. Practice melody freely
Choose an instrument, set volume/octave, and play by mouse/touch or keyboard. Good for warm-ups, improvisation, and learning note positions.

### 2. Play any major/minor scale on white keys
Lock **Key / scale** (for example `D major` or `A minor`). White keys are transposed to that scale so you can run scales and tunes without sharps/flats fingerings on the physical white row.

### 3. Practice Hindu bhajans with suggested scale & taal
Open **Bhajan helper**, search or filter a bhajan, then **Apply scale & taal**. The app locks the matching scale, sets taal, and can start rhythm — useful for practice with a suggested musical frame.

### 4. Jam with auto chords
Enable **Auto chords**. As you play a melody, the app detects key/scale and follows with accompaniment (soft pad, bass, tanpura, or sitar). Watch live chord and scale readouts while you play.

### 5. Add taal / groove
Enable **Taal rhythm**, pick a taal (Keherwa, Dadra, Teentaal, …) and a percussion voice (tabla, dholak, drumset, djembe, …). Tempo can auto-detect from your playing; bols and BPM update live.

### 6. Perform with Studio or Stage tone
Use header **Mix**:
- **Studio** — tighter, cleaner, less hall
- **Stage** — more presence, width, and reverb  

Useful when practicing quietly vs projecting a fuller performance sound.

### 7. Bend expressive phrases
Use the **pitch wheel** (springs back) or **hold slider** (stays) for scoops, meends, and ornaments. Set range to ±2 / ±7 / ±12 semitones.

### 8. Read what you play on staff
Live staff shows:
- Melody notes (with a short trail)
- Current auto-chord tones
- Tempo (`♩ = BPM`), time signature, bar/beat
- FACE / EGBDF (and bass ACEG / GBDFA) learning guides with colored note names

### 9. Record and review a take
**Record → Stop → Play** captures note on/off with accurate timing (including fast passages). Stop or clear playback as needed.

### 10. Practice longer with less eye strain
Header **Eyes**:
- **Comfort** (default) — mid contrast, matte, low glare
- **Focus** — a bit brighter for well-lit rooms  

Preference is remembered in the browser.

---

## Feature guide

### Header controls

| Control | Purpose |
|--------|---------|
| **Eyes** | Comfort / Focus visual modes for long sessions |
| **Mix** | Studio / Stage master bus profile |
| **Audio** dot | Shows whether the audio engine is running |

### Sound & performance controls

| Control | Purpose |
|--------|---------|
| **Instrument** | Melody voice (flutes, piano/organ, fretted, bowed, clarinet/saxes, reeds, harmonium family, basic waves) |
| **Volume** | Master level |
| **Octave** | Keyboard start C (`C3` / `C4` / `C5`) |
| **Sustain** | Hold notes after key release (pedal-like) |
| **Record / Playback** | Capture and replay performances |

### Key / scale & accompaniment

| Control | Purpose |
|--------|---------|
| **Auto chords** | Melody-following harmony on/off |
| **Key / scale** | Auto-detect, or lock any major/minor key (white keys follow locked scale) |
| **Sound** | Accompaniment style: Soft pad / Bass / Tanpura / Sitar |
| **Level** | Accompaniment volume |
| Live **scale** + **chord** readouts | Current detected/locked scale degrees and chord name |

When **Key / scale** is locked, white keys play that scale’s degrees across two octaves. Black keys fill chromatic gaps. **Auto detect (chromatic)** keeps a normal chromatic piano layout.

### Taal rhythm

| Control | Purpose |
|--------|---------|
| **Taal rhythm** | Enable/disable groove |
| **Taal** | Keherwa, Bhajani, Dadra, Rupak, Jhaptaal, Ektaal, Deepchandi, Teentaal |
| **Percussion** | Indian (Tabla, Dholak, Pakhawaj, Mridangam) and world/kit (Drumset, Conga/Bongo, Darbuka, Djembe, Cajon) |
| **Level** | Percussion volume |
| **Bol / BPM** | Live bol display and auto tempo estimate |

Staff meter also follows taal when rhythm is on (for example Keherwa → 4/4, Dadra → 6/8, Rupak → 7/8). With taal off, meter can auto-detect common Western meters from your pulse.

### Bhajan helper (Top 300)

Collapsed by default to keep the keyboard visible — expand the **Bhajan helper** section when needed.

- **Search** with autosuggest as you type (titles and aliases)
- Filters: **Deity/theme**, **Scale** (major/minor), **Key**, **Taal**
- Each card shows suggested scale, taal, and BPM hint
- **Apply scale & taal** — locks Key/scale, sets taal, enables rhythm, applies BPM hint
- **Scale only** — locks Key/scale without changing rhythm

Data file: `bhajans_db.js`  
Scale/taal values are **common-practice suggestions** for practice and may vary by region, gharana, or singer.

### Live staff notation

- **Melody** staff: timed notes in a scrolling measure window + NOW playhead
- **Chord** staff: stacked tones for the current auto-chord
- Colorful noteheads with letter names
- Line/space guides: treble **EGBDF** / **FACE**, bass **GBDFA** / **ACEG**
- Transport chips: meter, tempo, bar/beat

### Pitch bend

| Control | Behavior |
|--------|----------|
| **Wheel** | Temporary bend; springs back to the hold-slider value |
| **Hold slider** | Sustained bend; double-click centers |
| **Range** | ±2, ±7, or ±12 semitones |

Pitch bend applies to live melody voices.

### Master mix (Studio / Stage)

Voices pass through a performance bus:

highpass → soft saturation → compression → body/presence/air EQ → dry + hall reverb + stereo width → limiter

**Studio** is cleaner/tighter; **Stage** is wetter, wider, and more present.

---

## Instruments (melody)

- **Flutes:** Western Flute, Bansuri, Native American Flute, Chinese Dizi, Been (Pungi), Hulusi, Bawu  
- **Keyboard & fretted:** Grand Piano, Organ, Guitar, Mandolin, Ukulele, Banjo, Harmonium, Drone Harmonium, Advanced Harmonium  
- **Bowed & Indian strings:** Violin, Viola, Cello, Sitar, Santoor, Dilruba  
- **Clarinet & saxophones:** Clarinet, Sopranino → Bass Sax family  
- **Reeds:** Shehnai, Nadaswaram  
- **Basic waves:** Sine, Triangle, Sawtooth, Square  

---

## Tips for reliable playing

- Click the page once before serious playing so `AudioContext` can start.
- If a dropdown is focused, piano letter keys are captured so they won’t change the instrument (for example `C` will not jump to Cello).
- You can type freely in the bhajan **Search** box without triggering piano notes.
- For scale practice: lock **Key / scale**, then use only white keys.
- For bhajan practice: Apply from the helper, then sing/play over taal + optional auto chords.
- For long sessions: keep **Eyes → Comfort**.

---

## Files

| File | Role |
|------|------|
| `piano_app_html_java_script_web_audio.html` | Full app (UI + Web Audio engine) |
| `bhajans_db.js` | Top 300 bhajan lookup database |
| `README.md` | This guide |

---

## Notes & limits

- Sounds are synthesized in the browser (Web Audio), not sample libraries.
- Auto key/chord detection is heuristic — lock **Key / scale** when you want a fixed tonic/mode.
- Bhajan metadata is for practice guidance, not a definitive musicological authority.
- Works best in an up-to-date desktop browser; mobile is supported but denser controls are easier on a larger screen.

---

## Credits

**P2A3S2V** version **2026.8**  
Created by **Parikshit Kumar Singh** and all family members.
