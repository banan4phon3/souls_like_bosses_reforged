# **![](https://media.forgecdn.net/attachments/1052/219/curseforge_logo.png)**

# Souls Like Bosses: Reforged

Souls Like Bosses: Reforged brings four cinematic, multi-phase boss fights to
Minecraft: **Nightlord**, **Melkor**, **Soul of Cinder**, and the
**Abyss Watchers**. Each encounter includes custom models, animations, attacks,
arenas, rewards, and extensive configuration options.

## Supported versions

| Minecraft | Mod loader |
| --- | --- |
| 1.20.1 | Forge |
| 1.21.1 | NeoForge |

## Found a bug?

Please use the structured [bug report form](../../issues/new?template=bug_report.yml).
It asks for the information needed to reproduce and diagnose the problem.
Before submitting, keep your `latest.log` and, if Minecraft crashed, the matching
crash report ready. See [Support and log files](SUPPORT.md) if you are unsure where
to find them.

Do not post access tokens, passwords, e-mail addresses, or other private data in
an issue or log file.

## <span style="color:#fff"><strong>Required Mods</strong></span>

*   **<span style="color:#ba372a">minimum of 6 GB allocated memory required</span>**
*   Huge Structure Blocks  
    [https://www.curseforge.com/minecraft/mc-mods/huge-structure-blocks](https://www.curseforge.com/minecraft/mc-mods/huge-structure-blocks)
*   AttributeFix  
    [https://www.curseforge.com/minecraft/mc-mods/attributefix](https://www.curseforge.com/minecraft/mc-mods/attributefix)

### **<span style="color:#fff">If you enjoy the mod, please consider supporting me on Patreon :)</span>**

[![](https://media.forgecdn.net/attachments/856/404/patreon.png)](https://patreon.com/bananaphoneminecraftmods)

# **<span style="color:#fff">Boss Battle</span>**

<span style="color:#fff">The Nightlord</span>

![](https://media.forgecdn.net/attachments/1443/777/2025-12-27_00.png)

## <span style="color:#fff">Boss Arena</span>

*   **Tree of Light**  
    Generates inside the Ocean biome

# <span style="color:#fff"><strong>FAQ &amp; Configuration</strong></span>

### <span style="color:#fff">Texture Issues</span>

If textures do not load correctly, place the **Mod Resources** resource pack at the top of your resource pack list.

### <span style="color:#fff">Boss Spawning &amp; Damage</span>

/function souls\_like\_bosses:adjust\_config/spawn\_night\_lord  
/function souls\_like\_bosses:adjust\_config/despawn\_all\_night\_lords  
/function souls\_like\_bosses:adjust\_config/despawn\_nearest\_night\_lord  
/function souls\_like\_bosses:adjust\_config/spawn\_darkmoon\_greatsword

### <span style="color:#fff">1 vs 1 Mob Battles</span>

By installing the Carpet Mod, you can enable 1v1 mob battles  
[https://modrinth.com/mod/neoforge-carpet](https://modrinth.com/mod/neoforge-carpet)

/function souls\_like\_bosses:adjust\_config/mob\_battle\_mark\_nearest\_mob

### <span style="color:#fff">Locating Boss Structure</span>

/locate structure souls\_like\_bosses:tree\_of\_light

### <span style="color:#fff">Boss Health Configuration</span>

Min: 100 | Max: 490000  
/scoreboard players set .s\_l\_b\_global nl\_health number

### <span style="color:#fff">Combo Length Configuration</span>

/scoreboard players set .s\_l\_b\_global nl\_combo\_length number

## **<span style="color:#fff">Modpack Configuration via Helper Datapack</span>**

You can configure the mod using a helper datapack.  
use the following code inside your load.mcfunction and adjust the values.

```
# --- Create scoreboard objectives ---
scoreboard objectives add gamerule_keep_inventory dummy  # 1=Keep items when dying to boss, 2=drop items
scoreboard objectives add boss_difficulty dummy          # 1=Easy, 2=Normal, 3=Difficult, 4=Hard, 5=Hardcore
scoreboard objectives add bossbars_enabled dummy         # 1=show boss bars, 2=hide boss bars
scoreboard objectives add slb_ability_cooldown dummy     # Cooldown time for player abilities
scoreboard objectives add heolstor_spawned dummy         # 0= gets spawned at the start
scoreboard objectives add nl_health dummy                # Health for Night Lord
scoreboard objectives add nl_combo_length dummy          # average combo length for Night Lord

# general config
scoreboard players set .s_l_b_global gamerule_keep_inventory 1
scoreboard players set .s_l_b_global boss_difficulty 2
scoreboard players set .s_l_b_global bossbars_enabled 1
scoreboard players set .s_l_b_global slb_ability_cooldown 1600
scoreboard players set .s_l_b_global heolstor_spawned 0

# boss health values
scoreboard players set .s_l_b_global nl_health 600

# boss combo lengths
scoreboard players set .s_l_b_global nl_combo_length 2
```

# **<span style="color:#fff">Credits</span>**

*   **Night Lord model** — based on a model by **chromexception**, used and heavily modified with the creator's permission
*   **Dark Moon Greatsword model** — based on [this PlanetMinecraft datapack](https://www.planetminecraft.com/data-pack/custom-sword-datapack-moonlight-great-sword/)
*   Everything else — boss design, animations, structures and code — is my own. No code from other mods is included; GeckoLib is a dependency, not bundled. Code written with AI assistance (Claude).
