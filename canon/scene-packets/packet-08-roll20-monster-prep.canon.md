# Scene Packet 8 Supplement — Roll20 Monster Prep

## Canon Status

This supplement is canon for Scene Packet 8 / Chapter 8 table preparation.

Use this file when building Roll20 tokens, token notes, GM notes, and quick reference macros for the Implosion Threshold and King's Chamber encounters.

Primary mechanics are consolidated in `packet-08-current-stat-blocks-quick-reference.canon.md`.

---

## Roll20 Setup Principle

Use existing Roll20 stat blocks for fast setup, then override behavior in token/GM notes.

Do not run chassis monsters straight from the compendium if their default behavior conflicts with canon.

Most important overrides:

- Crystal Tremorborn does **not** use Earth Elemental two-slam multiattack by default.
- Dhurak and Veyra do **not** use Stone Golem slam multiattack by default.
- Dhurak and Veyra do **not** have druid spell lists.
- The Mourning King does **not** act as an active lich boss while beams remain active.
- The Mourning King has **0 legendary actions** and **0 legendary resistances**.

---

# Token Setup — Implosion Threshold

## Crystal Tremorborn Token

**Recommended Roll20 Base:** Earth Elemental.

**Token Name:** Crystal Tremorborn

**HP:** 80 default; acceptable range 75–85.

**GM Notes:**

```text
CRYSTAL TREMORBORN
Base: Earth Elemental chassis for AC/saves only.
HP: 80.
Do NOT use Earth Elemental multiattack by default.

Role: short pre-boss tremor foreshadowing / debuff bruiser.

TRAIT — Tremor-Body:
First time Tremorborn takes damage each round, creatures within 5 ft make DC13 Dex save or nearby ground becomes difficult terrain until start of Tremorborn's next turn.

ACTION — Crystal Slam:
Use Earth Elemental attack bonus.
Hit: 13 (2d8+4) bludgeoning/piercing.
Target DC13 Con save or crystal-rattled until end of next turn.
Crystal-rattled: no reactions; first 10 ft of movement counts as difficult terrain.
Simpler option: failed save = prone.

OPTIONAL RECHARGE 5–6 — Fault Pulse:
20-ft line, 5 ft wide. DC14 Dex.
Fail: 10 (3d6) bludgeoning/piercing + prone.
Success: half/no prone.
Line becomes difficult terrain.
```

**Quick Macro Text:**

```text
Crystal Slam — Melee, Earth Elemental attack bonus. Hit: 13 (2d8+4) bludgeoning/piercing. DC13 Con or crystal-rattled: no reactions; first 10 ft movement is difficult terrain.
```

```text
Fault Pulse Recharge 5–6 — 20-ft line, DC14 Dex. Fail: 10 (3d6) bludgeoning/piercing + prone. Success: half/no prone. Line becomes difficult terrain.
```

---

## Crystal Shardling Token

**Recommended Roll20 Base:** Magma Mephit.

**Token Name:** Crystal Shardling

**HP:** default Magma Mephit HP.

**GM Notes:**

```text
CRYSTAL SHARDLING
Base: Magma Mephit.
Do not add HP or damage.
Remove flight if hallway/map makes it awkward.

Reskin:
Claws = jagged crystal cuts.
Fire Breath = green-white crystal flare / dead-lamp burst.
Fire/heat language = searing crystal pressure.

Death Burst:
Use only if party is fresh or fight too easy.
Fallback Shard Pop: on death, creatures within 5 ft DC12 Dex or 3 (1d6) piercing.
```

**Quick Macro Text:**

```text
Shard Pop Optional — On death, creatures within 5 ft DC12 Dex or 3 (1d6) piercing. Use only if fight feels too easy.
```

---

# Token Setup — King's Chamber

## Mourning King Token

**Recommended Roll20 Base:** Optional lich chassis only if the DM needs a token sheet for saves/HP reference. Do not run as lich.

**Token Name:** The Mourning King

**GM Notes:**

```text
THE MOURNING KING
Canon: NOT undead. NOT evil aura. Living-preserved throne-bound vessel.
Do NOT run as active lich boss.

Combat role while beams active:
- inert vessel/battery/grief-focus
- fastened to throne
- cannot move
- no normal combat turns
- no spell list
- no legendary actions
- no legendary resistance
- not commanding Druids

Defense while beams active:
Dhurak/Veyra protect him. If party attacks King, living Druid intercepts by default.
Both beams active: first 30 damage/round absorbed if damage reaches King.
One beam active: first 15 damage/round absorbed if damage reaches King.
Both beams broken: protection ends.

Speech:
Can speak as plea, denial, queen-memory, fragment, clarity flash. Not tactical command.

After both beams break:
Pivot to clarity/mercy/relic-salvation. Do not start second caster phase.
```

**Quick Macro Text:**

```text
Druid Interception — If King is attacked while a Druid beam remains, a living Druid intercepts by default. Redirect attack/effect to that Druid or have it take the damage/effect in King's place. Visual: beam yanks taut, roots lunge, fault-wall erupts, titan tears itself into attack path.
```

```text
King Speech Beat — The King speaks a fragment only; no action/spell. Use plea, denial, queen-memory, or throne-echo. He is vessel, not commander.
```

---

## Dhurak Stonevein Token

**Recommended Roll20 Base:** Stone Golem or durable earth creature.

**Token Name:** Dhurak Stonevein, the Fault-Tender

**HP:** 180.

**AC:** about 17.

**Legendary Resistance:** 1/day.

**GM Notes:**

```text
DHURAK STONEVEIN, THE FAULT-TENDER
Base: Stone Golem chassis for AC/HP/saves only.
HP 180. AC about 17.
Legendary Resistance 1/day.
Do NOT run Stone Golem multiattack by default.
No druid spell list.

Role: tremor Stone Druid; forced movement; bowl destabilization.
Beam: While Dhurak lives, one green beam to King remains active. Destroying Dhurak breaks his beam.

ACTION — Stone Druid Strike:
One melee attack, chassis attack bonus.
Hit: 16–18 bludgeoning/piercing + crystal force.
On hit: DC15 Str save or pushed 10 ft, preferably downhill / crack / beam lane.

RECHARGE 5–6 — Fault-Tender Stomp:
30-ft line or 15-ft cone. DC16 Dex.
Fail: 21 (6d6) bludgeoning/piercing + prone.
Success: half/no prone.
Area becomes difficult terrain. Bowl-slope slide may also trigger.

REACTION — Fault Resonance:
Trigger: takes meaningful damage, usually 20+ from one source, crit, or focused strike.
At most once/round. One cracked line within 30 ft trembles.
One creature on/near line DC14 Dex.
Fail: slide 10 ft toward bowl center or fall prone. Success: no effect.
Do not use if Stomp already made round busy.

OPTIONAL — Bridgefall Pull:
One creature within 60 ft DC15 Str or Wis.
Fail: pulled 10 ft toward crack/beam/slope/hazard and loses reactions until start of next turn.
```

**Quick Macro Text:**

```text
Stone Druid Strike — Melee, chassis attack bonus. Hit: 16–18 bludgeoning/piercing + crystal force. Target DC15 Str or pushed 10 ft downhill/crack/beam lane.
```

```text
Fault-Tender Stomp R5–6 — 30-ft line or 15-ft cone, DC16 Dex. Fail: 21 (6d6) bludgeoning/piercing + prone. Success: half/no prone. Area difficult terrain; slope check if relevant.
```

```text
Fault Resonance Reaction — Trigger: Dhurak takes 20+ damage from one source/crit/focused strike. DC14 Dex for one creature on cracked line within 30 ft. Fail: slide 10 ft toward center or prone. 1/round. Skip if Stomp made round busy.
```

---

## Veyra Deeproot Token

**Recommended Roll20 Base:** Stone Golem or durable earth creature.

**Token Name:** Veyra Deeproot, the Root-Seer

**HP:** 150.

**AC:** about 17.

**Legendary Resistance:** 1/day.

**GM Notes:**

```text
VEYRA DEEPROOT, THE ROOT-SEER
Base: Stone Golem chassis for AC/HP/saves only.
HP 150. AC about 17.
Legendary Resistance 1/day.
Do NOT run Stone Golem multiattack by default.
No druid spell list.

Role: root Stone Druid; restraint; preservation pressure; anti-mobility.
Beam: While Veyra lives, one green beam to King remains active. Destroying Veyra breaks her beam.

ACTION — Crystal-Root Lash:
Ranged/melee spell attack within 60 ft, chassis attack bonus or +7.
Hit: 13–16 piercing/psychic.
On hit: target speed -10 ft until end of next turn.

RECHARGE 5–6 — Crystal Root Snare:
Up to 3 creatures within 60 ft standing on stone/crystal. DC15 Str.
Fail: restrained + 10 (3d6) piercing/psychic.
Success: speed -10 ft until end of next turn.
Escape: action DC15 Athletics or Acrobatics.

REACTION — Root Preservation:
Trigger: takes meaningful damage, usually 15+ from one source, crit, or focused strike.
At most once/round. One creature within 30 ft standing on stone/crystal, usually attacker, DC14 Str.
Fail: speed 0 until start of target's next turn.
Success: speed -10 until start of target's next turn.
Do not use same round as Crystal Root Snare unless party overwhelming.

OPTIONAL — Green Beam Reinforcement:
When King takes damage, reduce damage by 10–15 OR attacker DC15 Wis or 7 (2d6) psychic.
If used as reaction, cannot also use Root Preservation that round.
```

**Quick Macro Text:**

```text
Crystal-Root Lash — Ranged/melee spell attack within 60 ft, +7 or chassis bonus. Hit: 13–16 piercing/psychic; target speed -10 ft until end of next turn.
```

```text
Crystal Root Snare R5–6 — Up to 3 creatures within 60 ft on stone/crystal, DC15 Str. Fail: restrained + 10 (3d6) piercing/psychic. Success: speed -10. Escape action DC15 Ath/Acro.
```

```text
Root Preservation Reaction — Trigger: Veyra takes 15+ damage from one source/crit/focused strike. One creature within 30 ft DC14 Str. Fail: speed 0 until start of next turn. Success: speed -10. 1/round.
```

---

# Shared Roll20 Reminders

## Beam State Tracker

Create a simple visible/GM-only tracker:

```text
Dhurak beam: ACTIVE / BROKEN
Veyra beam: ACTIVE / BROKEN
Both active: King absorbs first 30 damage/round if hit.
One active: King absorbs first 15 damage/round if hit.
Both broken: King exposed; pivot to clarity/mercy/relic route.
```

## Attuned Offense Backlash Macro

```text
Attuned Offense Backlash — While at least one beam remains, Erny/Maelreth offensive action against boss can trigger once/round. All crystals flash. All party DC14 Dex. Fail: 7 (2d6) piercing/force. Success: half. Slopes may slide. One beam broken: weakened/discretionary. Both beams broken: ends.
```

## Bowl Slope Reminder

```text
Bowl Slope — Lower slopes difficult terrain. Upper slopes difficult + unstable. After tremor/shove/beam/falling shards, DC14 Dex or DC13 Ath/Acro as appropriate. Fail: slide 10 ft toward center, fall prone, lose movement, or take 1d6 if meaningful.
```

## No-Use List

Do not use these by default:

- Earth Elemental multiattack for Tremorborn.
- Stone Golem multiattack for Dhurak/Veyra.
- Druid spell lists for Dhurak/Veyra.
- Lich spell list for King.
- Lich legendary resistance for King.
- Lich legendary actions for King.
- Final-arena minions.
