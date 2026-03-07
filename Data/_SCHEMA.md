# JJK RPG — Master Schema & Buff Key Standard

## Canonical Buff Keys
All `buffs` objects across every file use ONLY these keys:

| Key | Type | Description |
|-----|------|-------------|
| `strength_add` | int | Adds to strength value |
| `speed_add` | int | Adds to speed value |
| `durability_add` | int | Adds to durability value |
| `biq_add` | int | Adds to battle IQ value |
| `iq_add` | int | Adds to intelligence value |
| `luck_add` | int | Adds to luck stat |
| `ce_add` | int | Adds flat CE units (e.g. 500) |
| `ce_efficiency_mult` | float | Multiplies CE cost reduction (1.5 = 50% cheaper) |
| `ct_mastery_add` | int | Adds to CT mastery level (1–10) |
| `weapon_mastery_add` | int | Adds to weapon mastery level (1–10) |
| `domain_mastery_add` | int | Adds to domain mastery score (0–10) |
| `rct_level_add` | int | Adds to RCT level (0–3) |
| `exp_mult` | float | Multiplies XP gained |
| `black_flash_mod` | float | Multiplies black flash trigger chance |
| `attack_mult` | float | Multiplies all outgoing damage |
| `ce_cost_mult` | float | Multiplies CE costs (1.3 = 30% more expensive) |
| `can_regen_with_ce` | bool | Cursed spirits only. Regain HP by spending CE |

## Root Key Convention
Every file uses its own filename (without .json) as root key:
- `age.json` → `{ "age": [...] }`
- `ce.json` → `{ "ce": { "amounts": [...], "efficiency": [...] } }`
- `combat.json` → `{ "combat": { "rct": [...], "luck": [...] } }`
- CT files → `{ "id": ..., "name": ..., ... }` (flat, no wrapper)
- WP files → `{ "id": ..., "name": ..., ... }` (flat, no wrapper)

## Cross-Reference IDs
Files reference each other by these stable IDs:
- Identities: `jujutsu_sorcerer`, `curse_user`, `death_painting`, `reincarnation`, `heavenly_restriction`, `sukuna_vessel`, `bounty_hunter`, `cursed_corpse`, `cursed_spirit`
- Clans: `gojo`, `zenin`, `kamo`, `inumaki`, `ashiya`, `fujiwara`, `abe`, `hasaba`, `sugawara`, `no_clan`
- Factions: `jujutsu_high`, `curse_users_association`, `culling_game`, `independent`
- Grades: `grade_4`, `semi_grade_3`, `grade_3`, `semi_grade_2`, `grade_2`, `semi_grade_1`, `grade_1`, `special_grade`
- CT IDs: match filename without extension (e.g. `blood_manipulation`, `ten_shadows`, `limitless`)
- Weapon IDs: match filename without extension (e.g. `playful_cloud`, `standard_katana`)
