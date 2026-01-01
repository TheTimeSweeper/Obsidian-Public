## New Bots
- m1
- m2
- Ability to trickshot
- Movement
- Skill Ceiling
- deflecting/some interaction with projectiles
- knockback?
- interaction with collider shield? (everyone but epitaph, deadlift, collider lol)
- possibly some kind of trick shot that doesn't require swapping
    - steeltoe: hammered
    - router: backboard
    - deadlift: live ammo
    - aphid: pan-seared
    - tachi: chain
    - collider: bodied
    - epitaph: rally
    - thistle: pierced
### Whip Guy
latch on to things and spin around to damage with the line
- m1 energy whip
    - wind up animation
    - if holding input at whip crack time, latch
    - release to let go
    - anyone that makes contact with the whip is hurt
- m2 dash
    - hurts people based on your speed
    - use to initiate orbiting when your whip is latched
- movement: dash
- trickshot: just keep spinning
- deflecting: 
    - whip? 
    - during windup (and then you hit the thing you deflected with the whip)
- knockback:
    - windup is a shove into sweet spot range?
    - sweet spot hits back if you're not holding for a latch?
- idk where to fit, probably an upgrade: pull enemy opposite your direction, so you can just spin around together and fly in a direction like a bolas
### Electrician
throw conductors and chain zap between them and enemies
- m1 zap
    - long sustained zap (let's say 6 bolts)
    - maybe just hold to keep zapping
    - chains 2 times, prioritizing conductors
- m2 throw conductor
    - if zapped duplicates the bolt at whatever chain length it was
        - or extends the chain by 2
        - conductor dies
- lightning prioritizes targets it hasn't hit before, but will still bounce back if nothing else is found
    - or maybe it's just random
- movement: if you directly target a conductor with m1, zap into it, then zap out a short distance in movement/input direction
- trickshot: repeated primary fire, and slight delay on chain lightning bouncing
- deflecting:
    - conductors block projectiles?
        - they're charged by enemy shots? 
- knockback: uh
    - when conductors explode?
#### whelllp
- implemented and sucks
- landed on (good enough for now)
    - m1 zap, chains to 1
    - m2 conductor
        - has an area around. when enemies in the area are hit by m1, the conductor also zaps them
- thoughts
    - should add subtle tether from bot to conductor so yo know whose is whose
    - bring back m1 bouncing off conductor (or make it an upgrade), disallow returning to the same target (or make it an upgrade)
    - ai changes
        - bot aim lags behind
            - stops moving aim once casting
        - bot only decides to attack from shorter range
            - but keep decide throw m2 range the same?
            - bring back up with ai level?
    - conductor grabbable by collider (no longer yours)
    - m1-m2 at the same time to detonate conductor as gwonam suggested
        - launches enemies (and you) (and projectiles?) that are near it
    - projectiles that hit the conductor
        - do damage?
            - plays animation on death, this is a chance to detonate it or it fizzles harmlessly
        - bounce back but only if you detonate it?
        - bounce back charged if you detonate it right when it hits?
        - stick to conductor and get charged? once detonated release ball of charged projectiles in the direction you're detonating
            - probably upgrade
    - still not high skill enough
        - currently the m1 is multiple bolts over a time, with the highest damaging bolt being at the end
            - as a player this rewards being able to keep your cursor on the enemy for the whole duration
            - for trickshots this also rewards leading the final hit as you swap out
        - suppose we can lean into this, and remove the shapecast, requiring pinpiont aim like thistle
### Koal comboer
mix m1 and m2 to do fighting game combos
- 1, 11, 111 finisher
- 2, 22, 222 finisher
- 1, 11, 2, 22, can be mixed and matched indefinitely
- longer the combo the bettter the finisher
- sword and shield bot? chivalry knight bot like that's the joke it's medieval knight even though we're in robot age
    - 1 swipe\, 11 spin, 111 slam shield in the ground
    - 2 shield bash dash smash, 22 shield throw, 222 big sword stab
    - 1 and 2 are better single target, 11 has area, 22 has range
- movement: 2
- trickshot: finishers
- deflect: 2, 22, 111
- knockback: 222, 111
### Desolator
- m1 shoot
    - does this game have debuffs?
    - applies 3 stacks of radiation on enemy
    - m1 and m2 damage increases per stack on enemy
- m2 spread the doom
    - hold to build up pump, release to spread a large area that applies radiation
        - stops movement. can be recasted indefinitely
        - goes on cooldown when you move or use primary
    - holding builds up strength up to a limit.
        - can keep holding past the limit, at the cost of health
        - if you don't release in time, you just die
- movement: increased speed in radiation zone?
    - stacks with each overlapped application of the zone
- trickshot: big lingering aoe
- deflect: uh
- knockback: uh
- upgrades:
    - if you die while holding charge, you explode the amount charged
### Chrono Legionnaire
freeze an enemy in time. use chronosphere to isolate an enemy
- m1 tether to an enemy
    - freezes them, unable to do anything or be damaged
    - after a while, vanishes from existence
- m2 chronosphere
    - highlight an area, then highlight second area
    - enemies (not tethered, and not you) in the first area are teleported to the second area
    - welcome bugs, the food is on the floor and the door is open
- does not move normally:
    - project image while inputting movement, leaving body behind
    - stop inputting movement to teleport to image
    - after teleporting, disable self for a period of time based on teleport distance
- movement: teleport
- trickshot: vanish
- deflect: freeze projectiles in chronosphere initial highlight. on cast, projectiles are teleported, and converge under your control (or continue on their merry way)
- knockback: how bout total relocation lol
- thoughts
    - gonna take a bit of a support role. use chronosphere to rearrange enemies for use by other bots, primary completely locks down a priority target
- upgrades:
    - primary chains to +1 target
    - chronosphere second area is smaller (pulling enemies together)
### Gatherer
- idk I just want someone to pull enemies together
- black hole? that explodes?
- wind magic?
### Stance Swapper
switch axe but robot
both stances react to being hit differently
starts in a random stance
### Katamari LOL
# Code notes for enemy api or whatevs
## P0: Bare Minimum
- consts
    - *`ClassName.const_field_name`*
        - *`ClassName.function_we_need_to_fix_if_we_cant_change_const`: Priority | hook ugliness*
            - *comment*
    - `GameManager.enemy_scenes`
        - `GameManager.spawn_enemy` : P0 | ugly
            - well damn I could swear there was more
            - in any case it's not a very clean hook. we have to copy past it all

Allows manually calling `GameManager.spawn_enemy` (or rather `spawn_and_place_enemy`) and playing as them

## P1-0: MVP add bot to runs
Goals:
- P1-0: spawn enemy in run
    - support enemy being level 1 2 or 3 and distribute them in run spawns accordingly
- P1-0: kill enemy
    - fitness score

- consts
    - `Enemy.ENEMY_NAME`
        - `Fitness.add_kill_to_score_feed`: not requried | ugly
            - has failsafe, otherwise would be nice for MVP
    - `Fitness.enemy_score_values`
        - `Enemy.calculate_score_value`: P1 | ugly 
                - another ugly copy the whole thing hook but we can do it
- extend/hook/etc
    - `DiscreeteEncounter.sprinkle_in_lvl2_bots`, `sprinkle_in_lvl3_bots`, `sprinkle_in_later_bots`: P1 | Ugly
    - `SpawnZone.enemy_type set():`it's the one. it's like THE one. | ugh
        - P1: extend `Encounter.activate`, or `DiscreteEncounter.start_wave`, or `DiscreteEncounter.handle_exotic_enemy_spawns`, and essentially do our own sprinkle_in_lvl1_bots
## P1-1: MVP but actually
Goals:
- P1-1: get upgrades for enemy
    - in upgrade drops and shop items
        - sacrifice "random common upgrade" buttons in shop for now

- consts
    - `UpgradeManager.LV1_ENEMY_TYPES, LV2_ENEMY_TYPES, LV3_ENEMY_TYPES` then update `VALID_ENEMY_TYPES` and `LEVEL_UPGRADE_POOLS`
        - `LV1_ENEMY_TYPES, LV2_ENEMY_TYPES, LV3_ENEMY_TYPES`
            - `UpgradeManager.get_host_pool_for_given_level`: P1 | easy
                - not bad hook. returns a duplicate that we can append to
            - `UpgradeManager.get_random_upgrade_for_given_level`: P1 | ugly
                - less not bad but not the worst. probably have to copypaste again
- extend/hook/etc
    - `Upgrades` collections are all static vars yaay
        - `upgrades`: P1
    - `UpgradeInfoMenu.set_enemy_icon`: P1
        - if it failsafes we can skip
    - `ShopUpgradePanel.set_upgrade`: P1
## All
```
P0 : bare minimum
P1 : MVP
P2 : likely next after MVP
P2+: past MVP
```
- consts
    - *`ClassName.const_field_name`*
        - *`ClassName.function_we_need_to_fix_if_we_cant_change_const`: Priority | hook ugliness*
            - *comment*
    - `GameManager.enemy_scenes`
        - `GameManager.spawn_enemy`: P0 | ugly
            - well damn I could swear there was more
            - in any case it's not a very clean hook. we have to copy paste it all
    - `HordeEncounter.ENEMY_TIERS, ENEMIES`
        - skipping
    - `Enemy.ENEMY_NAME`
        - `DialogueUtil.player_host_string`: P2+
        - `Fitness.add_kill_to_score_feed`: P2 | ugly
            - has failsafe, otherwise would be nice for MVP
            - this failsafe hard checks the enum so hook is unavoidable
    - `Enemy.PlayableEnemyType`
        - `LevelManager.generate_daily_run`: P2+
        - `DiagnosticsMenu.set_up_upgrade_grid`: P2+
    - `Enemy.enemy_icon_paths`
        - literally none of the uses of this are required? P2+
    - `EliteEnemyUtil`
        - whoof put a pin in it for now
    - `Fitness.enemy_score_values`
        - `Boss.calculate_score_value`: P2+
            - not needed for custom enemy MVP but needed for any custom bosses
        - `Enemy.calculate_score_value`: P1 | ugly
    - ~~`UpgradeManager.enemy_menu_display_order`~~
        - ~~`UpgradeManager.upgrade_type_sort` don't even have to hook~~
    - `UpgradeManager.LV1_ENEMY_TYPES, LV2_ENEMY_TYPES, LV3_ENEMY_TYPES` then update `VALID_ENEMY_TYPES` and `LEVEL_UPGRADE_POOLS`
        - `LV1_ENEMY_TYPES, LV2_ENEMY_TYPES, LV3_ENEMY_TYPES`
            - `UpgradeManager.get_host_pool_for_given_level`: P1 | easy
                - not bad hook. returns a duplicate that we can append to
            - `UpgradeManager.get_random_upgrade_for_given_level`: P1 | ugly
                - less not bad but not the worst. probably have to copypaste again
            - `RouletteShopSelectionPanel.init` P2 | ugly
        - `VALID_ENEMY_TYPES`
            - `UpgradeManager.get_random_upgrade` P2 | super ugly
            - `GolemBoss.spawn_ad`: P2+ | ugly
        - `LV1_ENEMY_TYPES`
            - `MountainBossAI.spawn_pillar_ring_for_player_to_bonk_against` P2+
        - `LEVEL_UPGRADE_POOLS`: unused?
    - `ShopUpgradePanel.abbreviated_bot_names`: unused
- extend/hook/etc
    - `GameManager.get_player_skin_paths_for_enemy_type` : P2+
        - can be skipped if your bot has ignore_skin true 
    - `Upgrades` collections are all static vars yaay
        - `upgrades`: P1
        - `hyperupgrades, antiupgrades, GOLEM_upgrades, story_upgrades`: P2+ or n/a
    - `Options.enemy_kills enemy_deaths enemy_swaps`: unused?
        - not consts, these can probably be added to
    - `Progression.bot_tutorial_completed` for the maniacs that actually build tutorials for their bots
    - `World.spawn_zones`: Unsure
        - need to look into it, but for mod compat we can say hey make your enemydefinition choose one of these zones
        - `World.import_zones` ? looks like editor script
    - `DiscreeteEncounter.sprinkle_in_lvl2_bots`, `sprinkle_in_lvl3_bots`, `sprinkle_in_later_bots`: P1 | Ugly
    - Where is `EnemyDispenser` used?
    - `EnemyConveyor.add_enemy` : P2+
    - `GolemSpider.load_skin`: P2+
        - I never noticed spiderbot has unique colors for each bot
        - doesn't break, we just don't get a skin
    - `GolemBoss.generate_and_apply_upgrades`: P2
        - add to `GolemBoss.valid_upgrades`, which isn't const thankfully
    - `GolemBoss.attempt_trickshot`: P2+
        - massive props to the maniacs who even do this
        - actually probably doesn't need to be in the api
    - `GolemBoss.apply_host_buffs`: P2
        - that's so mean bro I love it
        - also probably doesn't need to be in the api, but might be nice
    - `SpawnZone.enemy_type set():`it's the one. it's like THE one. 
        - please tell me we can hook these properties
        - we cannot
        - we also run into a bit of a design dilemma, because enemy encounters are designer authored, not randomly placed. 
        - P1: hook `Encounter.StartWave`, or `DiscreteEncounter.handle_exotic_enemy_spawns`
    - `DiagnosticsMenu.data` where it's read
    - `DiagnosticsMenu._process`
        - oh god they needed to hard code all the gamepad directions for each tab I'm so sorry
    - `DiagnosticsMenu.set_selected_bot
    - `DiagnosticsMenu._on_[BOT]_pressed`
        - I respect more than anyone the "just get it done" hustle
    - `PaintShopMenu`
        - yadda yadda yadda
    - `UpgradeInfoMenu.set_enemy_icon`
    - `Fitness.calculate_kill_score`
        - for progression tracking, which...
    - `SwapManager.update_swap_stats`
    - `DeathFadeOverlay.vboxes, set_up_character_icons`
        - looks like the death showing your items situation
    - `DebugConsole.entities` except not really
    - `ItemPanel.set_icon`
    - `ItemPopup.setup_upgrade_panel`
    - `TierdUpgradePanel.set_icons`
    - `UpgradePanel.set_icons` 
    - `CharacterInfoBar.swapped_host`
        - heere's the UI
    - `TabMenu.vboxes, set_up_character_icons, show_post_boss_1_tabs, show_post_boss_2_tabs
        - oh no this is not dynamic haha
        - seeing some `set_up_collider_icon` which seems to be an editor tool
    - `RouletteShopSelectionPanel`
        - uh
        - probably not really hooks, but we'll have to setup functions to our UI
    - `ShopUpgradePanel.set_upgrade`