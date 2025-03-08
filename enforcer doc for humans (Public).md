---
tags:
  - Public
---
Enforcer Gang

Several aspects of this are now outdated

This is what naturally happens during development

Don’t marry your docs

# Legend

Needs Tweaking/Being Tweaked

Points of contention

In progress/Not yet implemented

Low Priority/Skippable

# Overview

Details may be out of date

### Shootgun (primary)

- Piercing spread
- Knocks back
- Stops you a bit with each shot

### Shield bash (secondary)

- Does a damaging or two
- Pushes enemies away
- Deflects attacks

### Tear Gas (utility)

- Relatively large area
- Relatively large cooldown
- Weakens (lowers damage, health, movement speed)

### Creme de la creme (special)

- Blocks damage in front of you
- Slows movement
- Increases shotgun attack rate
- Shield lags behind aiming direction
- Moves camera in
- Heavy frame data on setting down and picking up shield

# Moves

Details may be out of date

### Primary

Shootgun:

- Shoots a piercing cone of 4 bullets
- Knocks enemies back
- Stops you a bit with each shot
    - For maximum B E E F

### Secondary

Big bash:

- Pushes enemies away
- Deflects attacks
- Damages
- Generous hitbox for pushing, not too crazy knockback
    - Separate deflect hitbox requiring more skill
- Dash forward when used out of shield

### Utility

Tear gas grenade:

- Creates a lingering cloud of gas that slows enemies and reduces their armor, with potentially other effects. For the time being, the Weaken debuff will work for this.
    - The debuff is instantly applied to enemies entering the gas cloud, and removed when enemies exit the gas cloud.
- The gas should deal no damage, but the grenade itself could deal a bit of explosive damage in a small area.
- Radius should be large. I’d estimate 16-20m, but in-game testing will determine the size.
    - Should last around the same duration as an Engi shield, with a lower (but still relatively long) cooldown.
- Codewise I imagine it would a BuffWard. As a placeholder its appearance can just be a giant yellow warbanner sphere or something, maybe with a simple particle system as well

Alternate Utility: Nostalgia stun grenades

- Bunch of charges, relatively low cooldonw
- Relatively spammable, stuns enemies like old video game for boomers

### Special

Protect and Serve:

- No cooldown
- Place shield and block damage
    - Blocks damage of things in front of you
    - Placing and picking up shield have heavy animation delay
        - encourage committing to it
- Slows movement speed
    - (sets base movement speed)
- Increases shotgun fire rate
    - (not character’s attack speed)
- Shield facing direction lags behind aiming direction
    - So it feels heavy
    - So you can’t as easily look around and block anywhere
    - Feels gud
        - Might wanna mess with slowing it down to the point where unshielding and turning around is faster than turning and waiting for it… hmm
- Camera zooms in to over the shoulder view

# Subjects of Discussion/General Thoughts/Comments

### Our team has an impressive ability to meme

- Proud of you guys

# Extras

### Skins

- Mastery
    - Lucid’s model
- Engi
    - Unlock: stand in bungus for 4 minutes
- Doomguy
    - Unlock: slay 50 imps in one stage
- Drizzle/Monsoon/RainStorm-Trooper
    - Unlock: ~~miss 1000 shots~~ knock people off the edge with shield bash
    - Changes name based on selected difficulty
- ~~Shadow the hedgehog (Desperado skin before I knew it was already a reference)~~

### Unlockable Survivor

- For super authentic character feeling
- Unlocked: idfk. To be determined (with discussion and vote)
    - Tank XXX damage
        - Fits the theme of tanking, and when players try to take damage and die a bunch, they’ll super duper appreciate enforcer being able to block it all
- We may get a lot of complaints from kids angry that their free mod they downloaded doesn’t let them play their extra free character immediately
    - We can have an UnlockImmediatelyForBabies config option
    - Set up a ruthless chefbot reply to them
    - Just send all complaints my way, I’ll take em all one by one put up ya dukes come on

# 

# [Assets](#_msv6kog3jsdx)

The only part of the doc that stayed relevant

Needs Tweaking/Being Tweaked

Low Priority/Skippable

### Reanimations:

- Shield
    - Leg movements are solid
    - Upper body can be made more consistent to play nicer with animations on top of it  
        Aka fuck you humanoid
        - Shield bash is fine
        - Gun shoot
        - Super shotgun reload
        - Hammer swing
        - Aiming yaw (pointing gun around shield)
        - Aiming pitch (leaning his spine up and down

### Animations:

- ~~Character select~~
- ~~Rest Idle~~
    - ~~Back to rest~~
    - Aiming/looking left, right, up, down
- ~~Combat idle~~
    - Aiming/looking left, right, up, down
- ~~Walking~~
    - ~~Fwd, bwd, strafe left, strafe right~~
- ~~Jump~~
    - ~~Jump motion, Ascent, Descent~~
- ~~Shield bash~~
    - ~~regular~~
    - ~~Shield bash while in Protect and Serve~~
    - ~~Shield bash shoulder dash while sprinting~~
        - Perhaps he ends the dash with a roll if he didn’t hit anything
- ~~Sprinting~~
    - ~~Fwd,~~
- ~~Protect and Serve~~
    - ~~Idle position~~
        - ~~Going in shield, coming back out~~
    - ~~Walking in shield~~
        - ~~Fwd, bwd, strafe left, strafe right~~
    - Shotgun arm aiming ~~right left~~ up down, over there and all around
- ~~ShootGun~~
    - ~~Aiming/Shooting forward~~
    - ShootGrenade

### WeeWise:

- ~~Footsteps (or just use existing)~~
- For his neutral special
    - ~~He weilds a gun~~
        - ~~Crit variant~~
    - ~~Configurable classic shoot sound for nostalgia nerds like me~~
    - Shells hitting ground
- Shield bash
    - Plap for hitting enemies
    - Unique reflect sound
- Tear gas
    - ~~grenade launcher FOOMF~~
    - smokescreen/gas Psssss
- Shield
    - ~~Blocking damage (shit hitting shield)~~
        - ~~Ricochet for small hits~~
        - ~~Beef for big hits~~
    - Getting into/out of shield
    - Turning on/off Energy shield
        - Energy shield breaking
- Feel free to meme
    - Oh this is pandora’s box isn’t it

### Models:

- The guy
    - Keep the helmet relatively similar. We’ve grown attached to it
    - Preferably adjust the current model instead of making a new one
        - Otherwise we’ll have to repaint it to the skeleton
    - Armor plating on gun arm
        - He’s gonna reach around the shield
- The shield
    - Hole/divet for gun
    - Straps for arms
    - window
- The gunn
    - Add Grenade launcher attachement
- The grenade
- I feel like I’m forgetting something
- Me too bud, me too.

### graphic design is my Passion:

- Character icon
- Skill icons
    - ~~M1 shotgun~~
    - Alt M1: assault rifle
    - M2 bashybash
    - ~~SHIFT tear gas grenade~~
    - Alt SHIFT: stun grenades
    - ~~R protect and serve~~
        - ~~R you stop that~~
    - Alt R: energy shield
- Buff icon
    - Protect and serve

### Effects:

- Shield bash swipe
- On block effect
- On reflect effect
- BLOCKED damage flyups
- Go nuts

### Item Displays:

- ~~Don’t do it you absolute madman~~
    - ~~You did it you absolute madman~~

### Links:

[Assets](#_ao9lehpmdl1g)

[Animations:](#_u8r7mhc23v6p)

[WeeWise:](#_kjsyu0gvzwuu)

[Models:](#_2m9nalo62kpj)

[graphic design is my Passion:](#_oo4lsotksvc1)

[Effects:](#_26dsmsaa59ls)

[Item Displays:](#_xm2ph8zdxsws)

# Fun Ideas

- Charge move as alternate R
    - R sets down shield normally
    - R again picks up shield and charges through enemies
    - R doesn’t have a cooldown so this is gonna sneak right in there
        - Gonna be hard to communicate that the cooldown is just for the charge part, and the shield stances can be switched in and out as normal
- ClassicItems Scepter
- Skills++ upgrades
- Feel free to add more you crazy characters

Enforcer second draft kinda

Discussion as development started, expanding on previous concepts

# Subjects of Discussion/General Thoughts/Comments

Details may be out of date. Most of these have been addressed. Keeping for record purposes I suppose

### ~~Staying in shield may be too powerful~~

- There’s nothing stopping someone from sitting in shield state and just holding m1
- Especially if you just stay against a wall

### Shield Issue Possible Solutions:

#### Shield health meter:

- - Shield has a certain amount of abuse it can take
        - After which it “breaks”, being disabled until the meter is charged again
        - Shield bashes can give meter
    - Pros:
        - Solves issue; you will want to stop shielding or else you’re going to take damage
        - Solves issue; back to a wall and block all the damage you want, but it’s not gonna last
        - resource management has a new dynamic to it
            - Adds more depth to shield bash
    - Cons:
        - Being forced out of shield don’t feel too good

#### Nerfing Knockback/Movement:

- - Balance his overall knockback
        - Enemies will slowly but surely gain ground on you and can overrun you
        - Use of other abilities doesn’t _keep_ enemies away from you indefinitely
    - Pros:
        - Solves issue; you will want to pick up your shield before you get overrun
        - Solves issue; you can’t walk backwards against a wall, reducing the amount of valuable relative space you could be gaining
        - Keeps the essence and feeling of bunkering down
    - Cons:
        - Very tricky to balance, if even possible

### Camera zooming in may be too limiting

- Pros:
    - Adds to the feeling of shielding
    - Makes more clear the effective area of your shielding
- Cons:
    - Lowers situation awareness
        - This seems like too much of a detriment to gameplay to justify the pros

### Experiment with shield aim limiting

- Pros:
    - Depending on balance, may add more depth to your decision to shield
- Cons:
    - Fucking aiming is being limited

Enforcer First Draft

Enforcer gang’s early discussion

### Overview

#### M1: Shootgun

- Small knockback

#### M2 ~~R~~: Grenade

- Stuns
- Has multiple charges with low-ish cooldown

#### Alt M2: Grenade

- Pulls them inward
- Normal cooldown

#### SHIFT ~~M2~~: Bash away

- Pretty much same

#### R ~~Shift~~: Protect and Serve

- Expands to decent area, and curved at edges to cover some more of your sides
- Camera zooms out so you can see past the shield
- ~~Rotating shield around is slow and limited, but aiming shooting is kept free~~
- Press jump while in shield stance to do a short dash hop

#### ~~R + CTRL :c~~

- ~~New charge move~~
    - ~~Stuns and knocks enemies above you~~
    - ~~Lets you reposition in this new crazy world with 360 more degrees where you can get fucked~~
    - ~~Kinda like mulT shift but no stopping~~

## Moves

#### M1: Shoot the shootgun. nothing unusual here

- Shooting enemies knocks them back, ~~and slows them a bit~~
    - ~~Encouraging you to stand and hold your ground and keep hitting is a great feel and simply the knockback we were already gonna do is great for this~~
        - ~~Shoot them a bunch and they slow more and more, shoot them a little and the slow is relatively negligible~~
- Long story short yea nothing unusual

#### M2: Stun Grenade

- Multiple charges

#### M2: Variant

- (K there’s something kinda unusual that i wanted it to do)
- Goes through enemies and implodes, pulling them in a bit
    - Not really unusual as this would be just expanding on the value it originally had: Keeping enemies infront of you so you can continue to wail on them.

#### Shift: Bash away. nothing unusual here

- Bash away. nothing unusual here
- We’ll be pretty generous with the hitbox and also the hitbox will expand in shield stance
    - (since the shield is gonna expand when you’re in shield stance which we’ll get to soon)
    - Range extends back a bit to even affect some enemies behind you

#### R: Take aim. I forgot the other name. Little unusual here

- Shield area will be pretty big in front of you, and curve around the sides as well, to provide a little cover so you’re a little less bombarded from all directions
    - Camera zooms out so shield can be big and not block vision
        - This also helps you look out for shit coming your left and right and a little behind
- ~~Locking the orientation from the old game has definitely got to go.~~
    - ~~Slowing the shield down is a good solution for this~~
    - ~~But I want the gun to be independent of the shield. I completely agree that rotating the shield quickly and being able to block everything is too much, but also restricting aiming I think is too much~~
- Movement will be pretty momentum heavy
    - After moving a bit and keeping your direction, you can get a good decent speed to keep blocking and shooting stuff, but not right away
- Jump while in shield stance to do a little dash hop (a la breath of the wild sneaking)
    - From the devs: “Ror2 is built a lot more around dodging than Ror1 - how will we translate the bunker down playstyle into the new game in a way that’s engaging?”
        - Running around and dodging isn’t very enforcery, but this is a nice compromise.
        - It’ll be a quick burst that slows down. Over distance it won’t be making you more mobile, but it’ll be good for small repositioning

~~R+ CTRL~~

- ~~Charge. Very unusual here~~
- ~~Press sprint while in shield state to charge forward. Stuns and knocks upward and behind you~~
    - ~~This is to have an effective move for repositioning and continuing the enforcering.~~
    - ~~This is the big solution to why everyone’s worried about bringing him to ror2 where shit’s fucking everywhere and bullshit and crazy and fun.~~
        - ~~His style of play is that bunker down thing we’ve mentioned, so this is needed to complement that and you can bunker down more~~
    - ~~Kinda like mulT shift but not weight based so doesn’t stop at enemies~~
- ~~This is what will take the cooldown of SHIFT~~
    - ~~A huge importance of this is we needed a move with a cooldown here, (and we needed it to be good). And that’s pretty much just for afterburners. It’s an incredible detriment to afterburners or any ability based item if Shift is just switch stances with no cooldown~~

# Gnome Comments

Questions:

- How is the shotgun going to work? A proper shotgun (like commando’s alt secondary) or like it was in the first game (kinda like a blast attack)
    - TS: I imagined simply a cone of bullets that pierce

Suggestions:

- For **Protect and Serve**, How about when you enter the move, it enters an alternate camera view. Kind of like an over the shoulder type thing. You’d be able to move your reticle around at the same speed, but there would be limits on how far you can move it in one direction. Or, perhaps bring the reticle to the edge of your limit causes you to turn slowly in that direction. Your movement controls would be based on the center of your aim window (which would be movable in the second scenario). This is a little hard to type out but I think it’s an idea you might be familiar with.
    - Thought of a better way of describing this. So the view of the screen is fixed, reticle moves around the screen like a cursor
        - TS: hmmmmmmm
    - Maybe I’ll try and work on a demo of just this move. Also if you just straight up hate any of my ideas feel free to say so
- For **Protect and Serve**, Maybe also give an attack speed buff
    - Maybe also aim cone reduction / distance buff?
- For **Crowd Control**, I’m think of having it be very similar to the commando’s grenade, except more charges, less damage, different sort of launch, explode on impact, and different fuse mechanics
- For **Shield Bash**, maybe make it reflect projectiles, might be cool and also make up for the lack of good movement

Things I’m not sure about:

- I’m not super sure about having so many of his attacks slow, feels like this overlaps with the purpose of crowd control. I think it makes more sense to have crowd control be the only move that debuffs but make it more spammable, especially since it’s such a fun move to use because of the ricochets
- Not sure about the ctrl + shift. I feel like we should really stick to the bunker down niche
    - TS: this is anticipation of the bunkering down inevitably screwing you over. I wanted this to be able to reposition and continue bunkering down

# Moffein Enforcer Concept

Core Principles:

- General playstyle should make him good at holding down an area (ex. Protecting an Engineer’s sentries)
- Probably should not have dashes or anything for closing the distance to far-off enemies

M1 - Shotgun

- Range-limited to 80 like MUL-T’s nailgun
- Probably should not have much knockback because it would lose DPS at high fire rates due to falloff unless it has falloff disabled.

M2 - Shield Bash

- Knocks enemies back with a generous hitbox.
- Stuns
- Directional force? Like being able to splat things against walls, or being able to jump and aim downwards to not push enemies too far.

Idea is that it’ll be somewhat like MUL-T’s M2 where you can stunlock things with multiple backup mags.

Slots Undecided:

Ability 3 - Tear Gas Grenade

- Long cooldown
- Covers an AOE in Tear Gas (size? No idea).
- Tear Gas slows enemies and lowers their attack speed. Possibly even stuns?
- Potential for armor debuff or dealing passive damage like Acrid’s puddles?

Goal is for this to sort of be like a more proactive Engineer shield. Could toss it down to turn a group of enemies into easy prey for teammates, or toss it near teammates to weaken enemies coming at them. Playing into the whole idea of “Protecting and Serving” and being more of a defensive character.

Ability 4 - Shield

- Movement/Jump penalties would probably be suicide.
- Turn speed penalties would probably make it feel awkward to use.
- No idea about the rest, would probably have to actually go in-game and test out different ideas.

# Discussion Conclusions

Primary

Primary will be a spread shot of piercing bullets with limited range

- Similar to twitch shotgun

Secondary

I think we decided that shield bash will be secondary

- Deflects projectiles

Utility - Designing around Tear Gas for now

Grenades

- Basic stun grenade
    - high charge count
    - medium cooldown
    - Meant to be mildly spammable
- Tear gas grenade
    - Creates cloud of tear gas which debuffs
    - Brings flying enemies to the ground
    - Area control-focused

Special

Shield

- No cooldown
- Quick enter animation
- Longer exit animation
- Can’t jump
- Limited movement
- Possibility of zooming in camera
- Should not block allied shots

We need to work on this one the most

Points of Contention

- Shield Turn limits?
    - Pros:
        - Could add a heavy feeling to the shield
        - More conducive to bunker down playstyle
    - Cons:
        - Touching/restricting player aim feels very awkward
        - Making the shield’s movement unsynced with the gun could feel odd
- Zoom in when shielding?
    - Pros:
        - More clear about what you’re blocking
        - Adds depth to bunker down idea
    - Cons:
        - Limiting player situational awareness
- Should grenades or bash be secondary?
    - Bash should be secondary if we do Tear Gas

Needs Discussion

- - How should the shield’s block hitbox work?

# For Next Time

- I (Gnome) will try to get started on shield bash
- Rob working on model

Tear Gas Specs:

- Creates a lingering cloud of gas that slows enemies and reduces their armor, with potentially other effects. For the time being, the Weaken debuff will work for this.
- The debuff is instantly applied to enemies entering the gas cloud, and removed when enemies exit the gas cloud.
- The gas should deal no damage, but the grenade itself could deal a bit of explosive damage in a small area.
- Radius should be large. I’d estimate 16-20m, but in-game testing will determine the size.
- Should last around the same duration as an Engi shield, with a lower cooldown.
- Codewise it could be a BuffWard. As a placeholder its appearance can just be a giant yellow warbanner sphere or something.

Enforcer Actual First Draft

- Timesweeper’s original original concept

### Overview

M1 :

- Shootgun
    - Small knockback small slow

M2:

- Bash away
    - Pretty much same

SHIFT:

- Protect and Serve
    - Expands to decent area, and curved at edges to cover some more of your sides
    - Camera zooms out so you can see past the shield
    - Rotating shield around is slow and limited, but aiming shooting is kept free
    - Press jump while in shield stance to do a short dash hop

SHIFT + CTRL:

- New charge move
    - Stuns and knocks enemies above you
    - Lets you reposition in this new crazy world with 360 more degrees where you can get fucked
    - Kinda like mulT shift but no stopping

R:

- Grenade
    - Stuns, slows, then pulls and knocks them inwards and away a little respectively

### Moves

#### M1: Shoot the shootgun. nothing unusual here

- Shooting enemies knocks them back, and slows them a bit
    - Encouraging you to stand and hold your ground and keep hitting is a great feel and simply the knockback we were already gonna do is great for this
        - Shoot them a bunch and they slow more and more, shoot them a little and the slow is relatively negligible
- Long story short yea nothing unusual

#### M2: Bash away. nothing unusual here

- We’ll be pretty generous with the hitbox and also the hitbox will expand in shield stance
    - (since the shield is gonna expand when you’re in shield stance which we’ll get to soon)
    - Range extends back a bit to even affect some enemies behind you

#### SHIFT: Take aim. I forgot the other name. Little unusual here

- Shield area will be pretty big in front of you, and curve around the sides as well, to provide a little cover so you’re a little less bombarded from all directions
    - Camera zooms out so shield can be big and not block vision
        - This also helps you look out for shit coming your left and right and a little behind
- Locking the orientation from the old game has definitely got to go.
    - Slowing the shield down is a good solution for this
    - But I want the gun to be independent of the shield. I completely agree that rotating the shield quickly and being able to block everything is too much, but also restricting aiming I think is too much
- Movement will be pretty momentum heavy
    - After moving a bit and keeping your direction, you can get a good decent speed to keep blocking and shooting stuff, but not right away
- Jump while in shield stance to do a little dash hop (a la breath of the wild)
    - From the devs: “Ror2 is built a lot more around dodging than Ror1 - how will we translate the bunker down playstyle into the new game in a way that’s engaging?”
        - Running around and dodging isn’t very enforcery, but this is a nice compromise.
        - It’ll be a quick burst that slows down. Over longdistance it won’t be making you more mobile, but it’ll be good for quick repositioning

#### SHIFT + CTRL: Charge. Very unusual here

- Press sprint while in shield state to charge forward. Stuns and knocks upward and behind you
    - This is to have an effective move for repositioning and continuing the enforcering.
    - This is the big solution to why everyone’s worried about bringing him to ror2 where shit’s fucking everywhere and bullshit and crazy and fun.
        - His style of play is that bunker down thing we’ve mentioned, so this is needed to complement that and you can bunker down more
    - Kinda like mulT shift but not physics based so doesn’t stop at enemies
- This is what will take the cooldown of SHIFT
    - A huge importance of this is we needed a move with a cooldown here, (and we needed it to be good). And that’s pretty much just for afterburners. It’s an incredible detriment to afterburners or any ability based item if Shift is just switch stances with no cooldown

#### R: Stun Grenade.

- uh long story short...  
    ahem…  
    nothing unusual here
- K there’s something kinda unusual that i wanted it to do
- Goes through enemies and implodes, pulling them in a bit
    - Not really unusual as this would be just expanding on the value it originally had: Keeping enemies infront of you so you can continue to wail on them.

# Beef

## [Assets](#_dl55q99sop3)

Low Priority/Skippable

In progress/~~Needs Tweaking~~

### Animations:

- Main Animations
    - Idle
    - Run fwd, left, right, back
    - Sprint fwd, left, right
- Abilities
    - M1
        - Swing hammer 1, 2
    - M2
        - Charge
        - Dash
        - Uppercut small, med, heavy
    - Utility
        - Jump up
        - Slam down
- Minigun
    - M2
        - Slam

- Additional/Polish/Legitness/Hopoo Touch™
    - Aim pitch, yaw
    - idlein (stop running - idle)
    - Jump up
    - Landing impact
- Extra/rob Touch™
    - Emotes
    - Rest idle
- Running ~~Fwd,~~ bwd, strafe left, strafe right
- Sprinting ~~Fwd,~~ strafe left, strafe right
- Landing impact
- Dominance (not in minigun)
    - ~~Charging, Charging~~, uppercut small/mid/larg,
    - Charging descend in air

#### Done

- ~~Walking with minigun~~
    - ~~Fwd~~, ~~bwd~~, ~~strafe left~~, ~~strafe right~~
- ~~Jump~~
    - ~~Ascent~~, ~~Descent~~
- ~~Character select~~
    - ~~Standing on hammer~~
- ~~Combat idle~~
    - ~~Hammer stance~~
    - ~~Minigun stance~~
- ~~Rest Idle~~
- ~~Idlein~~
- ~~Spawn~~
- ~~Pitch/Yaw~~
- ~~Throw grenades hammer stance, minigun stance~~
- ~~Going in Minigun~~, ~~back to hammer~~
- ~~Minigun Spinning~~
- ~~Golden Minigun~~
    - ~~Minigun Pitch~~

## Not Assets

### Skills:

Shift

- Void grenades

Minigun

- Cannon alt
    - Cannon lookin model from the original concept
    - Slow, beefy, pierce
    - Hurts multiple times while it’s piercing like I’m led to believe sawmerang does

Scepter

- Gatling missile launcher

### Extra:

#### Skins

- Templar skin
- Use dunestrider ‘leg’ things for the mechanical arm
- Someone design a hammer
- Mithrix
    - Alternate minigun animation, just using his left arm to shoot needles
- Draymarc’s badass damaged armor concept
    - We can apply to the invader boss

#### Taunts (not emotes)

- Lowtiergod
- salute

The Re-Beefening

Not done

Low prio (second pass)

Low prio (other)

Rig fucked, needs redone

But actually unfucked?

Don, looking for tweaks/improvement

~~Good enough but could still be better~~

_~~Done and sexy~~_

### Animations:

#### Bod

- Idle pose
- Idle anim
- Run L/R/F/B
- Sprint
- IdleIn (walk, sprint)
- Jump
- Ascend/Descend
- Landing impact
- ~~CSS~~
- ~~CSS idle~~
- Aim pitch
- Aim yaw
- Aim yaw (chair)

#### Shield

- Shield idle pose
- Sheild idle
- Shield in/out
- Shield walk L/R/F/B
- Shield aim pitch
- Shield ascend/descend
- Shield Idlein
- _Shield aiming if I’m a fucking maniac_

#### Neutral special

- Shoot, Shoot(shield)
- Shoot SSG, Shoot SSG(shield)
- Shoot AR, Shoot AR(shield)
- Swing hammer, swing hammer(shield)
- Stop with shots
- Shield Bash, Shield Bash(shield)
- Shield Bash (shield) (air)
- ~~Shoulder Bash~~
- Aim grenade
- Throw grenade

#### Other

- Skateboard riding
- Skateboard in/out
- Skateboard shoot
- Skateboard hammer swing
- _Skateboard shield bash dash smash_

#### Other other

- ~~Fuckin chair lol~~
- Default dance
- Earl run (with scaling)

### Skins:

To take seriously

- ~~Default~~
- ~~Sexforcer (lucid (but actually me))~~
- ~~Grandmastery (bruh)~~
- ~~Nemesis~~
- ~~N-4CR (holy shit where’d that come from)~~
- Heavy (not tf2)
- ~~Classic~~

Less serious but I really don’t want to put them behind cursed

- ~~Engi~~
- ~~Doom~~
- ~~Stormtrooper~~
- ~~Desperado~~
- Oh wow it’s all the old skins

Definitely cursed

- ~~Minecraft~~
- ~~Fem (anon)~~
- ~~frog~~
- ~~pig(cut)~~