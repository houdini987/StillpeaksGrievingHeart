# Stillpeak’s Grieving Heart — Startup & Canon Orientation

This file is the single startup reference for working on Stillpeak’s Grieving Heart in this repository.

Its purpose is to help a fresh assistant, author, or coding tool quickly understand:
- where the live canon files are
- which files are authoritative
- the current story spine and campaign direction
- how new scene packets must be structured

This file is a navigation and authoring aid. It does not override live packet canon. When a `.canon.md` file exists for a packet, that packet file remains the authoritative source for its content.

---

## 1. Canon Authority Rule

This repository is the authoritative source of truth for Stillpeak’s Grieving Heart canon.

### Canonical file rules
- Files ending in `.canon.md` are the live canonical source for scene packets.
- Files under `canon/appendices/` are live supporting canon unless explicitly marked otherwise.
- Files under `assets/images/` are the canonical visual asset layer once linked.
- Exported `.docx` and `.pdf` artifacts are derived outputs, not source canon.

### Consumption rule
When answering questions, building new content, or revising scene packets:
1. Read the relevant `.canon.md` files first.
2. Treat packet canon as primary over chat memory or older documents.
3. Preserve exact rules language where canon defines:
   - DCs
   - encounter logic
   - conditions
   - item behavior
   - progression rules
4. Do not create parallel canon layers unnecessarily; revise the existing `.canon.md` file instead of creating alternates.

### Live gameplay rule
Live gameplay state such as:
- HP
- initiative
- temporary conditions
- resource depletion
- inventory drift
- token state

belongs to Roll20 / live session state unless intentionally promoted back into this repo.

---

## 2. Core File Locations

### Canon navigation
- `canon/CANON_MANIFEST.md`
- `canon/README.md`

### Live scene packets
- `canon/scene-packets/packet-01-southwatch-geomantic-observatory.canon.md`
- `canon/scene-packets/packet-02-cold-pass-to-cinderwatch.canon.md`
- `canon/scene-packets/packet-03-cinderwatch-frozen-village.canon.md`
- `canon/scene-packets/packet-04-karagvorn-line-lower-slopes.canon.md`
- `canon/scene-packets/packet-05-mid-slopes-of-stillpeak.canon.md`

### Supporting canon
- `canon/appendices/monsters-of-stillpeak.md`
- `canon/appendices/visual-escalation-model.md`

### Packet directory root
- `https://github.com/houdini987/StillpeaksGrievingHeart/tree/main/canon/scene-packets`

### Recommended first-read order for a fresh assistant
1. `canon/CANON_MANIFEST.md`
2. `canon/README.md`
3. relevant live packet files in numeric order
4. supporting appendices if needed

---

## 3. Repo Working Rules

### Style and tone
- Preserve restrained tone.
- Avoid melodramatic escalation.
- Keep environmental pressure primary.
- Creatures are often expressions of the mountain’s condition, not the main point.
- Preserve the Tremorscope as the most reliable directional truth source.
- Treat the Karagvorn Line as reinterpretation of rules, not blanket suppression of magic.
- Keep checks, DCs, and rewards explicit.
- Prefer modular, segment-based design as danger escalates.

### Editing rule
When editing or extending canon:
- preserve existing structure and naming conventions
- preserve the exact section order used by live packets
- do not invent a new packet schema
- revise in place where possible
- keep scene packets self-contained for live play and DM-AI consumption; by default, include concise BEAT markers, Live Use anchors, selective Likely Player Actions, and selective Run Fast notes inside the packet itself while avoiding separate helper files for packet-level canon support

### Naming rule
- Scene packets use the `.canon.md` suffix
- Filenames containing `vX` represent the actual live canonical version number and should be treated as authoritative current versions when present

---

## 4. High-Level Campaign Premise

**Stillpeak’s Grieving Heart** is a bleak survival-driven mountain campaign set in the eastern Spine of the World, south of Icewind Dale.

### Core conceit
Grief has become geological.

Stillpeak’s heart pulses with sorrow, and the land responds:
- first with stillness
- then with cold
- then with distortion
- then with the dead who do not fall
- then with warped pressure on burden, movement, and reality itself

### Core systemic truths
- Encumbrance matters.
- Altitude and cold matter.
- Extradimensional storage becomes inert beyond the Karagvorn Line.
- The Tremorscope remains the most reliable directional tool where other orientation tools and assumptions drift.
- Environmental pressure is usually more important than creature lethality.
- The mountain’s influence often expresses itself through systems, not spectacle.

---

## 5. Story Spine — Current Canon Through Packet 5

This section is the campaign spine for orientation and future packet building.

### Packet 1 — Southwatch Geomantic Observatory
The party delivers a dying hunter’s journal to Southwatch. The observatory legitimizes the threat and introduces the Tremorscope. The party learns that Stillpeak’s pulse is deliberate, mournful, and spreading.

### Packet 2 — Cold Pass to Cinderwatch
The wilderness begins to feel afflicted rather than merely dangerous. Silence deepens, natural behavior fails, frost behaves incorrectly, and minor hostile phenomena appear as reactive symptoms of the mountain’s deeper pulse.

### Packet 3 — Cinderwatch: The Frozen Village
The human cost becomes clear. Cinderwatch survives through discipline, storage, and burden-management. The Vault teaches that ascent culture matters. The mountain’s pattern appears selective: guides, route-makers, stone-workers, and those tied to ascent labor seem to have been taken first.

### Packet 4 — The Karagvorn Line & Lower Slopes
The party crosses the Karagvorn Line, where reality does not stop functioning but becomes less helpful. Burden is literalized. Extradimensional convenience fails. The mountain “reads” load. A brief atmospheric reveal hints that the summit conceals a seam, recess, or hidden opening.

### Packet 5 — The Mid-Slopes of Stillpeak
The ascent becomes an attrition threshold. The mountain now feels actively hostile and costly. Through climbing pressure, environmental distortion, prior-climber traces, and Tremorscope readings, the party learns that:
- others deliberately climbed toward the summit before them
- the Tremorscope detects hidden internal structure
- the summit contains a concealed entrance leading inward

By the end of Packet 5, the summit is no longer the final destination. It is the threshold into the real mystery.

---

## 6. Story Spine — Remaining Arc Direction (Binding Guidance for Future Packets)

The following direction is the current narrative spine for building the remaining packets.

### True campaign objective
The ultimate goal is for the party to investigate and ultimately put an end to the worsening tremors originating under Stillpeak Mountain.

### Summit reveal
The party does not understand the true mission until they reach the summit, where a hidden opening leads them into a spiral chamber descending deep inside the mountain.

### Interior campaign mode
Beyond the summit breach, the campaign shifts from exterior ascent into interior descent.

The interior environment should feel unstable and warped:
- at times like a dungeon
- at times like a mining colony
- at times like a place where perception and physical law misbehave

Visual and spatial effects should shift the party’s sense of scale, direction, and place.

### True source of the problem
The party ultimately discovers that the source of the tremors is a bereaved, enraged dwarven undead king.

Backstory spine:
- millennia ago, he lost his queen in a tragic accident
- grief curdled into rage, madness, and evil
- he drew power and life from the stone itself
- he laid waste to the mining establishment within the mountain
- his grief and corruption became bound into the mountain’s deep structure

### Endgame threat
For centuries he has been preparing an unholy forge.

The forge is constructing a weapon that will allow him to escape his lair and walk among the living outside the mountain.

That construction is the source of the worsening tremors.

### Structural implication for future packets
The summit is not the climax.
It is the hinge.

Packets 1–5 = exterior ascent, burden, attrition, grief in landscape  
Packet 6 onward = interior descent, warped dwarven ruin / mining colony, grief in stonecraft, memory, and broken physics

---

## 7. Design Guidance for Packet 6+

### Packet 6 should likely do the following
- pay off the summit seam as a real entrance
- introduce the spiral descent chamber
- pivot the campaign grammar from exterior mountain survival to interior ruin descent
- reveal the first strong signs of ancient dwarven royal / industrial presence
- show that the interior is being transformed toward forge-work
- avoid full exposition too early

### Reveal pacing guidance
Do not reveal the undead dwarven king too early through a clean lore dump.

Prefer this reveal ladder:
1. environmental evidence
2. industrial residue
3. funerary / royal clues
4. warped memory / history fragments
5. confirmation of the king and queen tragedy
6. forge truth
7. endgame threat of emergence

### Tonal guidance for the interior
The interior should not immediately become generic fantasy dungeon space.

It should feel like:
- a sealed wound
- a mining civilization broken by grief and violence
- a place where structure, labor, kingship, and mourning fused into corruption
- a place that was once functional and is now wrong in layered ways

---

## 8. Key World Concepts to Preserve

### Stillpeak
The cursed mountain whose summit fissure leads into a hollow core.

### Karagvorn Line
The “Stone-Sorrow Line,” an invisible boundary where reality subtly reinterprets itself.

### Tremorscope
A lantern-like seismographic tool that:
- displays deep-earth movement
- vibrates within range of significant tremor sources
- guides toward the ultimate source
- remains reliable where other tools become less helpful

### Mountain logic
Stillpeak often expresses grief through:
- stillness
- silence
- cold
- burden
- false geometry
- distance distortion
- distorted utility
- the conversion of effort into cost
- pressure on route-making, climbing, and rescue

---

## 9. Packet Authoring Template (Use This Exact Order)

All future scene packets should follow this exact section order:

1. At-a-Glance Summary  
2. Narrative Setup (Canonical Text)  
3. Read-Aloud Scene Introduction  
4. Environment Overview  
5. Running the Location  
6. Encounter Modules  
7. Player Curiosity Hooks  
8. Escalation Signal  
9. Rewards / Discoveries  
10. DM Reference Sidebar  
11. Map Reference  

### Authoring expectations inside packets
- Keep environmental pressure primary.
- Keep checks and DCs explicit.
- Use segment-based escalation when useful.
- Maintain practical, table-usable design.
- Use creatures to reinforce the location’s condition and theme.
- Preserve transition logic between packets.
- Keep discoveries interpretable before fully explained.

---

## 10. Quick Startup Prompt for a Fresh Assistant or Tool

Use this repo as the authoritative source of truth for Stillpeak’s Grieving Heart.

Before answering or editing:
1. Read `canon/CANON_MANIFEST.md`
2. Read `canon/README.md`
3. Read the relevant live `.canon.md` packet files in `canon/scene-packets/`

Treat packet canon as primary over chat memory or older documents.

Preserve:
- exact packet section order
- restrained tone
- environmental pressure as primary
- Tremorscope reliability
- Karagvorn Line rule reinterpretation
- explicit DCs, mechanics, and rewards
- existing naming conventions

Current story spine:
- Packets 1–5 cover the exterior ascent to the summit seam.
- The summit reveals a hidden opening into a spiral descent chamber.
- The real mission becomes stopping the worsening tremors from inside Stillpeak.
- The deeper source is a bereaved dwarven undead king whose grief, rage, and stone-drawing power destroyed an ancient mining establishment.
- He has spent centuries preparing an unholy forge to create a weapon that will let him emerge into the outer world.
- The forge construction is the source of the tremors.

When building future packets, do not reveal everything at once. Prefer environmental and historical discovery before full exposition.

---

## 11. Maintenance Note

If this file and live canon ever conflict, live packet `.canon.md` files win.

Update this file when:
- new live packets are added
- major directory paths change
- the future narrative spine is intentionally revised
- new supporting canon files become foundational for startup reading
