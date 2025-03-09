![](Games/img/SpellCasting.png)

Simple as that

We love casting spells

Legend:

Text in blue are things I would do if I have more time

Text in first person were written by me (TheTimesweeper) before I added folks to the team

### Credits

**thetimesweeper** - main development

**sweepersecret** - concept art and icons

**dotflare** - 3d modeling and texturing

**skeletorchampion** - enemy concepts

Overview

The goal of the game is to feel like a true spellcaster.  
In every game, “casting” a spell is the result of hitting a button, and the character doing everything for you. I want to open the player up to a wide array of interactivity so they really feel like they are more in control of the spells.

The player plays as a wizard who has control over the elements. Casting spells involves using a button to summon a mass of the element, and using mouse movements to manipulate the elements in different ways.

The world of the game is made of procedurally generated rooms, with points of interest that can be found to alter the elements which you control.

# Theme Interpretation

## Alchemy

Interpreting alchemy as manipulation of the elements, more than simply casting spells with the elements, the alchemy in this game involves manipulating the base properties of the elements, transforming them into different elements.

## Shadows

One must be careful when attempting to alter the fundamental laws of nature. For every light, a shadow can be cast. For every successful manipulation of the elements, something else is released into the world.

# Inspirations

## James Lambert

[Can Portal 64 be saved? - Libdragon](https://youtu.be/WDNU9k8uTc4?si=nc9xMQpJuUjhgrlK&t=357)

In this video James Lambert expresses his thoughts on spellcasting in games.

He says it feels “empty,” like you aren’t the one developing the magic.

In his game, he takes the direction of studying magic and developing spells. My game takes this in a bit of a different direction, where I want you to actively manipulate the magic, but the general idea stemmed from this.

## Wizard of Legend (Modding)

[Wizard of Legend on Steam](https://store.steampowered.com/app/445980/Wizard_of_Legend/), [Thunderstore mod database](https://thunderstore.io/c/wizard-of-legend/)  
Modding this game showed me a very fun experience making spells.

No spellcasting feels quite as good as it does in this game. Their game feel is truly remarkable. Naturally, being engrossed in a game is the #1 reason to want to make mods for it, and that’s what I was and did, respectively.

The base game inspired the general idea of elemental spellcasting, while my modding experience inspired not only creating new spells for the game ([shameless plug](https://thunderstore.io/c/wizard-of-legend/p/TheTimesweeper/)), but also inspiring ideas of adding new whole elements to the game, as combinations of the existing elements.

## Risk of Rain 2 (Modding)

[Risk of Rain 2 on Steam](https://store.steampowered.com/app/632360/Risk_of_Rain_2/), [Thunderstore mod database](https://thunderstore.io/)

Much of the code for this game is inspired by some of the code I have learned and developed in making Risk of Rain 2 mods ([shameless plug](https://thunderstore.io/package/TheTimesweeper/)). All re-written though. No copy paste.

Gameplay

# Player

You play as Joanna, a wizard who seeks to master all the elements. You have access to the four basic elements, bound to four buttons (M1, M2, Space, and Shift), and you use the mouse to manipulate them.

  
Each button controls a respective element. Controlling the elements is performed as follows:

- Pressing and holding the button summons a mass of the element at the mouse position
- Move the mouse to move the mass as you please
- Perform gestures my moving the mouse or joystick, and release to cast one of 2 spells depending on the gesture:
    - Swiping the mouse in a direction
    - Swirling the mouse around
    - Shaking the mouse left and right
- Double-Clicking the mouse will result in a simple primary attack
    - Unique to each element

# Elements

## Basic Elements

![](<Games/img/SpellCasting 1.png>)

Fire: Bound to m1, general damage

- Swipe: throw a fireball
- Swirl: aoe explosion

![](<Games/img/SpellCasting 2.png>)

Earth: Bound to m2, damage and stuns

- Swipe: throw a rock
- Swirl: create a ring of stone around you. No one can get in, no one can get out

![](<Games/img/SpellCasting 3.png>)

Water: Bound to shift, utility and debuffs

- Swipe: shoot a wave in a direction. Pushes and slows enemies
- Swirl: create a whirlpool dot zone that slows enemies

![](<Games/img/SpellCasting 4.png>)

Air: Bound to Space, movement and knockback

- Swipe: push yourself in the mouse direction
    - You have no dash. Manipulating air is your dash
- Swirl: a quick vortex that sucks enemies in

Each element has its own mana bar. It slowly regenerates over time, but is mainly replenished by using your primary in close range.

![](<Games/img/SpellCasting 5.png>)

## Secondary Elements

The four basic elements can be combined to create new elements, each with their own spells as well.

Hold one element, then input the second element to combine them

![](<Games/img/SpellCasting 6.png>)

Disclaimer: I know some of these combinations physically make no sense. I combine their properties based on their gameplay purposes first

![](<Games/img/SpellCasting 7.png>)

FIre and Earth: Metal: Earth but heavier

- Swipe: throw, less distance more damage
- Swirl: big block fall from the sky big stun

![](<Games/img/SpellCasting 8.png>)

Fire and Water: Lava: Area damage over time

- Swipe wave that leaves pools on the ground
- Swirl: covers land in a dot zone, burns enemies hit and reduces armor

![](<Games/img/SpellCasting 9.png>)

Water and Air: Light: Self buffs and healing

- Swipe: heal
- Swipe: slight push, move speed boost after
- Swirl: heal and mana field

![](<Games/img/SpellCasting 10.png>)

Fire and Air: Lightning: Fast

- Swipe: lightning bolt dash
- Swirl: lightning storm in area, cause hits to chain lightning between enemies

![](<Games/img/SpellCasting 11.png>)

Earth and Air: Sand: Air but wider area and more damage

- Swipe: move but damage and affects enemies
- Swirl: Sandstorm by Darude, very large dot zone

![](<Games/img/SpellCasting 12.png>)

Earth and Water: Ice: Water but more solid, freezes

- Swipe: throw, freezes enemy hit
- Swirl: area freeze

Combination elements use mana from the pools of both its component elements.

![](<Games/img/SpellCasting 13.png>)

Design

# Levels

- The game is a procedurally generated roguelike, with prefabricated rooms that are put together
- Some unique rooms include
    - Milestone rooms that allow you to find new elements
    - Chest rooms that require enemies to be defeated and grant items
    - A portal room that spawns enemies, whose defeat leads way to the next level
    - A final boss room that cannot be entered until enough elements are mastered (discovered)
    - Secret rooms one must find by using the elements
- After each level, new rooms can be discovered, and enemies are given buffs

# Progression

- Power items that are lost on death
- New elements that are not lost on death
    - Permanent gain of a new element will also permanently alter the world, adding enemies and obstacles to match your progressed power
    - Fire is granted on start, air is granted next, and the other elements cannot be found until those two are unlocked.
    - After the first four elements, you will find altars of combinations of those elements

## Items

- Stat ups
    - Max health, damage, move speed, max mana, mana regen, health regen, attack speed, stun resistance, cast range  
        ![](<Games/img/SpellCasting 14.png>)
    - Meat of damage  
        ![](<Games/img/SpellCasting 15.png>)
    - Coffee of speed

![](<Games/img/SpellCasting 16.png>)

- - Bread of life (max health)  
        ![](<Games/img/SpellCasting 17.png>)
    - Bread of mana (max mana)  
        ![](<Games/img/SpellCasting 18.png>)
    - Blue Cookie of regeneration (mana regen)  
        ![](<Games/img/SpellCasting 19.png>)![](<Games/img/SpellCasting 20.png>)
    - Regen globes (temporary)
- Interesting items
    - Elemental interactions
    - On-kills

# Enemies

![](<Games/img/SpellCasting 21.png>)

Each time you gain an element, the shadow of that element is released into the world. This causes new enemies to appear, using that shadow element. These elements will encourage the player to use the element in question as a counter to them

- Fire: basic damage, first element, introductory
    - Basic enemies, for the basic element, doesn’t move much, throws a fireball at you
    - Perhaps enemies that group up to be taken out by the explosion
- Air: second element, movement
    - Enemies that run away from you. You use your mobility to catch up to them
    - Enemies that strafe or scatter from each other. Use your swirl to pull them together.
- Earth: stuns and stone ring
    - A summoner enemy that doesn’t move, but summons small enemies that follow you and overwhelm you
        - Use the stone wall ability to isolate the summoner from the summons and take him out
        - When he dies, the summons die too
- Water: debuffs
    - Fast enemies that rush to you. You wanna use splash to push them away and slow them
    - Whirlpool will also help control/contain
- More enemies for the other elements
- Enemies vast their abilities by manipulating an element in a similar fashion to you

## Boss

A reflection of yourself. The boss uses the same 10 elements you use, but a little bit differently

Fire: darker

- Swipe: throw a fireball
    - -> 3 fireballs
- Swirl: aoe explosion
    - Ok like none of the other ones swiped. Maybe he just does this

Earth: darker, sharp crystals on it

- Swipe: throw a rock
- Swirl: create a ring of stone around you. No one can get in, no one can get out
    - -> smaller ring that traps you
    - -> cursor follows you at a slight delay so you have to be moving to avoid it
        - Or it follows you perfectly and the way to avoid it is to get out of his range

Water: darker (purpler?)

- Swipe: shoot a wave in a direction. Pushes and slows enemies
    - -> bigger?
- Swirl: create a whirlpool dot zone that slows enemies
    - -> no different?

Air: darker

- Swipe: push yourself in the mouse direction
- Swirl: a quick vortex that sucks enemies in
- ~~Shake~~ Swirl: area blast that pushes you away from them

FIre and Earth: Metal: darker. Spiky balls

- Swipe: throw, less distance more damage
- Swirl: big block fall from the sky big stun
    - -> shadow telegraph

Fire and Water: Lava: darker, bubbling idk

- Swipe wave, burns enemies hit and reduces armor
    - -> slow moving big magma projectile
- Swirl: uh covers land in a dot zone
    - -> starts small and slowly spreads to larger and larger area

Fire and Air: Lightning: darker/red

- Swipe: lightning bolt dash
- Swirl: lightning storm in area, cause hits to chain lightning between enemies
    - -> causes his hits to call down a lightning bolt on you

Earth and Air: Sand: darker

- Swipe: move but damage and affects enemies
- Swirl: Sandstorm by Darude, dot zone and slowly pulls enemies together
    - -> larger area, slows and pulls you, makes it hard for you to avoid things

Earth and Water: Ice: darker, different shape

- Swipe: throw, slows enemy hit
- Swirl: area freeze
    - -> even more telegraphed
        - Shatter damage?

Water and Air: Light: darkness?

- Swipe: slight push, move speed boost after
- Swirl: heal and mana field
    - -> destroyable ball that heals both you and them after a delay

For the extra extra curious, see the early development document here [Spellcasting Game (document for freaks)](https://docs.google.com/document/d/1MwCD4AOq0vDqkOD5l1Ary0EaokNBrQMlRZD9raH-Tvc/edit)