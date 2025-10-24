Elemental Shootout: Galactic Siege — One-Page Game Design Document (MVP)

Version: 0.1
Target Unity: 2022.3 LTS
Target Input: Unity New Input System
Primary Targets: Windows (desktop) + WebGL (hosted demo)
Scope: Single-player near-finished MVP (focused vertical campaign)

Vision
A polished 2D action shooter with deep class-based combat and elemental weapon modifiers. Fast, responsive movement, satisfying guns and abilities, and cinematic boss encounters across diverse biomes. The MVP should feel like a complete mini-game: campaign progression, unlocks, UI, polish, and performance-ready builds.

Core Loop
1. Accept mission → 2. Traverse level (platforming + exploration) → 3. Engage enemies using class and weapon loadout → 4. Complete objectives / defeat boss → 5. Earn XP & loot → 6. Upgrade weapons/abilities.

MVP Goals (what must be finished)
- Single-player campaign with 4 levels across 3 distinct biomes (Forest, Desert, Neon City)
- 6 playable classes (Blaster, Tank, Sniper, Engineer, Mage, Healer) with unique abilities
- Core combat (shooting, melee where applicable), movement (run, jump, dodge/roll), elemental weapon modifiers (fire/ice/lightning)
- One major boss with multi-phase mechanics (General Krovax: gravity mechanics)
- Progression: XP, ability unlocks, simple crafting/upgrading UI
- HUD, Main Menu, Options, Pause, Save/Load (3 slots + autosave)
- Placeholder high-quality pixel art + SFX and music
- Build pipeline for Windows and WebGL

Core Mechanics
- Movement: Rigidbody2D-based character controller, responsive air control, dash/dodge with invulnerability frames.
- Combat: Hitscan and projectile weapons; cooldowned abilities per class; enemy AI with simple state machine (patrol, attack, flinch, die).
- Elemental Modifiers: Weapons can be infused with elements (fire = DoT, ice = slow/terrain freeze, lightning = chain damage). Upgrades increase effect strength.
- Abilities: Each class has 2 active abilities + 1 passive.
- Loot & Progression: Enemies drop credits and rare components; vendors allow upgrades; simple crafting UI to slot modifiers.

Classes (MVP set)
- Blaster (mobility, rapid-fire, dodge)
- Tank (high HP, shield ability)
- Sniper (charge shot, headshot bonus)
- Engineer (deploy turret)
- Mage (area elemental spells)
- Healer (heals & buffs)

Level Structure
- Levels are semi-linear with optional side objectives (rescue, gather).
- Each level has platforming segments, arenas, and exploration zones with secrets.
- Environmental hazards and destructible props for tactical gameplay.

Boss Example (MVP)
- General Krovax: Gravity manipulation—platforms rotate/flip, gravity wells spawn, phases unlock new attack patterns. Requires timing and mobility, uses telegraphed attacks.

UI & UX
- HUD: Health, Shield, Ammo, Ability cooldowns, Mini objective indicator.
- Menus: Main Menu, Options (audio, graphics quality, controls remap), Pause, Save/Load.
- Accessibility: Key remapping, colorblind palette option.

Art & Audio
- Style: Polished high-resolution pixel-art (modern pixel aesthetic) for fast production and strong visual polish. Parallax backgrounds for depth.
- Audio: Placeholder SFX & looped music for each biome; polished SFX for weapons and boss telegraphs.

Tech & Tools
- Unity 2022.3 LTS, New Input System, Cinemachine for smooth camera, Tilemap for level editing, Addressables for assets.
- CI: optional GitHub Actions to produce WebGL + Windows builds (later).

Non-Goals for MVP
- Co-op / PvP
- Full crafting tree or massive loot variety
- Very large open-world systems

Success Metrics (MVP)
- Playable 20–40 minute campaign (all 4 levels + boss)
- Combat feels responsive (player movement < 150ms input-to-action perceived latency)
- No major crashes, stable 30–60 fps on target platforms
- Clean, navigable UI and save system

Risks
- Too many classes reduce polish—limit and iterate on 6 for MVP.
- Boss/mechanic complexity—prototype boss early (Week 1–2).

Acceptance Criteria
- All MVP features implemented and tested
- Playthrough of full campaign without blockers
- Documented build for Windows and WebGL with README and settings