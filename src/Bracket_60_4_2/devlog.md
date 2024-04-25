## TODO/Issues list
Some shared issues https://github.com/ZhengPeiRu21/mod-individual-progression/issues/70

- [ ] (see below) Naxx40 spells, boss scripts and encounters are not implemented correctly

- [x] 4horsemen, spell damage adjusted

More todo:
- [ ] (skip) Grobbulus: poison cloud damage reduce damage properly. (requires custom spell+client patch)
- [ ] (waiting upstream) Gothik, waiting for upstream changes
- [ ] (waiting upstream) Blaumeux: Void Zone casts Consumption (28865). Should do 4k damage, radius 2 -> 3
- [ ] Blaumeux+Zeliek: move
- [ ] Horsemen: no pathing on pull
- [ ] Blaumeux+Zeliek: Remove Punish spells for not being in range
- [ ] Heigan: Adjust Eruption calc so it no longer uses SetHitDamage(damage) which ignores defensive CDs?
- [ ] Infectious Ghoul: missing low hp text
- [ ] (skip, do below instead) Eye Stalk, 36y-90y evade smartAI. Stuck in combat, not evading
- [ ] Heigan: Eye Stalk/Heigan room adds should all despawn after defeating Heigan
https://github.com/cmangos/mangos-wotlk/blob/a3a647a0da14f9b6de483f99149e09b6ff6e7c8a/src/game/AI/ScriptDevAI/scripts/northrend/naxxramas/naxxramas.cpp#L419
- [ ] Necro Knight, has smartAI (see Necro Knight Guardian)
- [ ] Necro Knight Guardian, smartAI, similar implementation to Necro Knight might be better?
- [ ] Unholy Staff Arcane Explosion, damage is similar (~2k) but range is 45yd instead of 20yd. Requires spellscript to reduce radius
- [ ] Doom Touched Warrior, missing smartAI, casts dazed?
- [ ] Dark Touched Warrior, smartAI casts whirlwind, should only cast dazed?
- [ ] Death Touched Warrior, missing smartAI, should drop threat?
- [ ] Risen Deathknight, missing smartAI, casts dazed?
- [ ] Sewage Slime, disease cloud 28153. Ticks for 600 instead of 300. Trigger spell requires spellscript HandleDamage
- [ ] Plagued Ghoul - missing smartAI say texts
- [ ] Razuvious DK Understudy. has 2, needs 4

Client side patch:
- [ ] 4H, needs client patch for mograine mark
- [ ] Heigan: disruption should be power burn, 29310, client side patch needed
- [ ] Loatheb: Deathbloom -> Poison Aura. needs custom patch
- [ ] Loatheb: Deathbloom needs to do 200 dps after 6 seconds, patch needed

Bosses
Construct
- [x] Patchwerk
- [x] Grobullus
- [x] Gluth
- [x] Thaddius
- [x] Living Poison aka Frogger before Naxx is missing in lvl 60 instance
- [x] Grobbulus: slime spray damage adjusted
- [x] Grobbulus: debuff explosion damage adjusted
~~-[x] Grobbulus: poison cloud damage, damage reduced by lowering ticktime~~
- [x] Grobbulus: poison cloud damage, use lvl 80 entry what only casts a modified AoE ~3k to ~1.2k
- [x] Gluth: enrage increased, icon not updated (requires custom spell+client patch)
- [x] Thaddius: room Tesla shock reduced damage
- [x] Thaddius: mark damage from 4500 to 2000
- [x] Thaddius: lightning ball (wipe mechanic) adjusted
- [x] Feugen: Power burn 500 every 3 seconds. Missing nature visual shock (requires custom spell). Or do hack with 63705 spell, change yards to 300. -500 mana, -2500 dmg
Military Quarter
- [x] Razuvious: remove throwing knife mechaniac
- [x] Razuvious: reduce damage, range (45yd) of shout. Does not drain mana and ignores LoS. Needs client patch
This is incorrectly fixed in ACore. It uses a spellscript `spell_four_horsemen_consumption` to hardcode 4250 if not 10man normal. Should do proper scaling but 25man damage matches Naxx40. so skip for now
Plague Quarter
- [x] Noth: curse range adjusted, number of curses, faster curses
- [x] Noth: curse damage reduced, range increased
- [x] Heigan: fever dot 3k -> 500
- [x] Heigan: Poison Cloud, (AoE when he teleports), damage reduced to 500
- [x] Heigan: Reduce damage from eruption
- [x] Loatheb: Deathbloom damage reduced to 33dps for 6 sec instead of 200dps
- [x] Loatheb: Spores +50% to +60% caster crit

Trash
Plague Quarter
- [x] Infectious Ghoul: damage unchanged, updated rend, update frenzy
- [x] Plague Slime: unchanged
- [x] Mutaged Grub, reduce aoe dmg ~400 -> ~200
- [x] Frenzied Bat, update frenzy id
- [x] Plagued Bat, update IC timings
- [x] Plague Beast, smartAI trample
- [x] Eye Stalk, smartAI reduce damage, movement speed reduction is less
- [x] Eye Stalk, smartAI missing OOC rp and birth animation

Military Quarter
- [x] Horse mounts from trash before Razuvious are lvl 80
- [x] Death Knight Captain, updated smartAI to cast whirlwind/stun
- [x] Plagued Gargoyle, smartAI
- [x] Unholy swords, looks the same
- [x] Unholy Axe, looks the same
- [x] Death Lord, add smartAI
- [x] Deathknight, update smartAI
- [x] Skeletal Smith, update SmartAI
- [x] Bony Construct, update smartAI
- [x] Spirit of Naxxramas, update smartAI reduce shadow bolt damage from 2.2k to 1.8k
- [x] Skeletal Steed, smartAI add trample and intercept

Construct Quarter
- [x] Sewage Slime, slime that spawns from Grobulus are lvl 80
- [x] Pathwerk Trash (see below): awkward pathing with formations?
- [x] Bile Retcher 351022  - 27807 Bile Vomit - ~5k instant, ~1200 dot to ~1500 instant, 250 dot
- [x] Patchwork Golem - cleave based on weapon damage instead of raw damage in classic. Requires custom patch
- [x] Embalming Slime - same AoE damage, unchanged
- [x] Mad Scientist - Heal, reduced from ~20% hp to ~10% hp. Vanilla is raw ~3k
- [x] Mad Scientist - Mana Burn ~3.5k to ~1.5k
- [x] Surgical Assitant - Mind Flay damage from 1.5k to 600 per tick
- [x] Living Monstrosity - Chain Lightning damage from ~4k to ~1k. (Chain Lightning should 3 to 10. Range 45 to 30, requires custom script)
- [x] Living Monstrosity - Summon lvl 62 Lightning Totem
- [x] Lightning Totem - lvl62 - Shock damage ~3k to ~2k
- [x] Stitched Spewer - unchanged, weapon damage instead of raw 2k dmg
- [x] Toxic Tunnel - unchanged, damage should be 300->200. Triggered spell 28369. Requires custom patch
- [x] Necropolis Acolyte - add smartAI, Casts Shadow Bolt Volley and Arcane Explosion
- [x] Plagued Ghoul - 351078, add smartAI
- [x] Deathknight Vindicator, add smartAI
- [x] Razuvious, removed knife throw mechanic, disrupting shout adjusted to 45yd and less damage. No power burn without client patch or remove animation

- [x] Issue Bony Construct patrol/creature_formation guid 3612410
VMangos/CMangos show 5 points. No waypoints. 3 mobs wander with 15yd, 2 path
https://youtu.be/4UTQFrMRk5c?si=ye3fIhp7pg88f03C&t=5222 classic shows 4+2 pathing
ACore 25 shows 4+2 pathing

- [x] Issue Patchwerk Trash:
Creature formations of patchwork golems. Awkward pathing
Removed wandering from non-leader, but does not look correct
(361229, 361227, 10.8064, 306.6246666000065, 515, 0, 0),
(361229, 361228, 7.08383, 261.72081828001365, 515, 0, 0),
(361229, 361246, 6.33888, 349.3644533277902, 515, 0, 0),

potential upstream/acore fixes:
- [ ] Bombard Slime spell position is not random. Pos is pulled form spell_location template. Not present in acore, in VMangos/TC/CMangos from what I see
- [ ] Thaddius is stuck in position and does not move
- [ ] Lightning Totem does not aggro properly?
- [ ] Razuvious' Death Knight Understudy should switch between AttackReady (333) and Attack (36), out of combat RP missing
- [ ] Relinquery of Souls / Eye Stalk use OOC submerge spell // 28819 - Submerge Visual
implemented in TrinityCore: https://github.com/search?q=repo%3ATrinityCore%2FTrinityCore%20spell_reliquary_of_souls_submerge&type=code
- [ ] (pr #18807) 4 horsemen, Blaeumeux summons a Void Zone that periodically (every 1s) triggers Consumption (28865) which deals AoE damage. A spell script decides hardcoded damage based on difficulty. Proper spells should be used instead. `spell_four_horsemen_consumption` with hardcoded damage that ignore defensives. Should use proper IDs

https://github.com/TrinityCore/TrinityCore/blob/e0e1b6a4098badb6f48ba1d5cb1cc1739e310959/src/server/scripts/Northrend/Naxxramas/boss_four_horsemen.cpp#L65
28863, 57463
summons 16697 values 3000,4500 for 10M/25M

1 second timer, casts spell 28865
(28865, 'spell_four_horsemen_consumption')
    ```
    void HandleDamageCalc(SpellEffIndex /*effIndex*/)
    {
        uint32 damage = GetCaster()->GetMap()->ToInstanceMap()->GetDifficulty() == REGULAR_DIFFICULTY ? 2750 : 4250;
        SetHitDamage(damage);
    }
    ```

```
Boss - summonspell - effect2 dummy bp
Netherspite  - 37063 - 1110
Blaumeux 10M - 28863 - 2999
Blaumeux 25M - 57463 - 4499
```

acore :Summon Void zone - Netherspite 37063 summons 16697 which triggers 28865
trinitycore :Summon Void zone - Netherspite 37063 summons 16697

Confusion as in:
1.12
aura 28867 which applied 28865
naxx40

Summon Void zone - Netherspite 37063 summons Void Zone (16697) - Void zone which casts Consumption (28865) which damage calculated by 4 horsemen script with a SetHitDamage() to be 4250/2750 for 25M/10M

Trinitycore 4H:
https://github.com/TrinityCore/TrinityCore/blob/e0e1b6a4098badb6f48ba1d5cb1cc1739e310959/src/server/scripts/Northrend/Naxxramas/boss_four_horsemen.cpp#L65

Netherspite:
Void Zone (16697) casts Void Zone Effect (46264) deals 3000 dmg
https://github.com/TrinityCore/TrinityCore/blob/e0e1b6a4098badb6f48ba1d5cb1cc1739e310959/sql/old/3.1.3/05031_world_scripts_netherspite.sql#L7

## GM commands to help test

attunement - reputation honored - complete quest
```
.mod reputation 529 10000
.quest complete 9121
.go creature 54192
```

teleport to naxx entrance inside strat
```
.go xyz 3960 -3392 121 329
```

reset instance
```
.instance unbind all
```

10man HC
```
/script SetRaidDifficulty(4)
```

go Thaddius
```
.go c 130957
```

4H door
```
.gobject activate 65753
.go c 130961
```

patchwerk
```
.go c 128135
```

Naxx cauldron
```
.go xyz 3124 -3732 134
```

# Editing 80 spells / custom spells
Workflow went like this:

Look in CPP or smartAI with Keira3 https://github.com/azerothcore/Keira3
what spellIds need changing

https://github.com/stoneharry/WoW-Spell-Editor
Import from DB (Mysql)
if using default DB. user root, password password, port 3306, db acore_world
import spells.dbc, create new spell 90000+ i.e. 90004
Edit attribute, save and use db viewer to export row id from `spell`

create second folder and open 1.12

2 WoW-Spell-Editors side by side to compare 335 and 112

create custom spell in 335 and match 1.12 values

Go to ./Export folder and grep `grep 90004 Spell.sql`

copy the query into `progression_60_4_2_naxx_spells.sql`

Change smartAI or cpp to use new custom spellID

## SmartAI CMangos 1.12
cmangos db,
cmangos core,
Database Editor smartAI -> write smartAI with Keira

## Exploring, comparing DBC Spells.
Editing/exporting did not work for me with SpellWork. I used WoW-Spell-Editor instead
https://github.com/azerothcore/SpellWork
extract to azerothcore-wotlk/env/dist/data and run .exe
