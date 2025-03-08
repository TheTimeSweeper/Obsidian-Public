The Ultimate Potion

- The bigger the explosion,
- The better the alchemist!

Moves

# M1: thro bomb

Plague Knight throws a bomb.

- Using his Special, he can change the Casing and Powder of the bomb, which will affect its throwing behavior and exploding behavior respectively
- Throwing bomb is a skill
    - Powders are skilldefs in a genericskill that’ll have all the cooldowns
        - Viewable in loadout
        - ~wait runrecharge is run by genericskill not the skilldef so idk if they’ll cooldown n shit
    - Casings are skilldefs in a genericskill
        - Same
    - Throw bomb will grab a throw action from the casings skilldef
    - Throw bomb will throw a projectile with a component where we can pass in an action from the powder skilldef
- [holy shit valex this is going to be insanely useful](https://github.com/Vale-X/Thunderkit-Henry/wiki/Components#projectile-components)
    - Like god damn he seems so much more possible now

## Casing:

### [Casing Type]

- - Description
    - On-hit-land behavior
        - All powders impact on enemy
    - Fuse timing behavior
        - X timing Based on current powder fuse

### Regular thro (bounce/lob/drop/float? casings)

- - - Straight up just engi bomb
        - Formerly: Commando grenade ezpz (wait engi bomb does exactly what I want how did i not notice)
    - Lob, drop, float casings from shovel knight they’re taken care by direction you aim
        - except maybe float but that’s fine
        - Bounces on land
        - Waits X timing then explodes (total time, not after hitting land)

### Orbit

- - - Throw a little decent distance and they orbit around you
        - Like head of nems hammer head distance or little shorter
            - Which, yeah, melee range essentially
            - Probably they’re fatter so they hit peeps more
        - Direction you aim is the tilt of the orbit
    - World consistent while spinning, if you turn around it doesn’t affect its movement
        - Parent to characterbody ez?
            - Sounds like a violation of mcv
                - ~not really, it’s a gameplay aspect. Parenting to charactermodel would be more violation maybe but melee attacks are already based on this (which makes sense cause it’s related to the visual). Either way think we’re fine
    - Doesn’t touch land
        - It does in sk but for here it would probably be annoying
            - Oh wait it only does on the breakable shit so guess we’re good after all
    - Waits X timing then explodes

### Boomer

- - - No catch
        - actually not sure
        - K i like the way they orbit I’m basically gonna copy that it’s cool
        - it’s gonna throw straight (yz plane), then it’s given a small sideways velocity as the boomer-to-the-character(laterally more than vertically)-code kicks in
    - ~what’s the point of this
        - This’ll be fun/a nightmare to program
            - Nvm. see “holy shit valex” above
    - Doesn’t touch land
    - Waits X timing then explodes

### Homing

- - - Goes straight then stops and hangs for a sec
        - Waits for kniggas nearby
        - Fingers crossed on how much of engi’s mines’ code I can steal
    - Hits land or enemy and goes to homing mode
        - When finds enemy goes to it and explodes
    - Waits X timing then goes into homing mode
        - Then waits consistent timing then explodes

### Remote?

- - Throws like regular case but with the remote fuse and Sticks on land instead of bouncing/exploding
    - Throw normally and press E while looking at one to detonate them all
        - Shows a reticle on all the bombs on and off screen
        - Prompt says _HEE HEE HEE_
    - Sticks on land and peeps
    - Never explodes until you tell it
        - Disregards fuse timing. Just lands on things

### Fuckin whack

- - The one with the handle
    - You just swing it at them in front of you
    - It explodes bigger/stronger/harder/faster

## Powder:

- - Reg, combine, tracer, zappyz, fire, cluster,
    - Charges with cooldown. If you switch to them and use them up, they automatically switch back to reg powder

### Reg:

- - Behavior
        - Throw and explodes. Nothin unusual here
    - Purpose
        - Damage lol
    - Fuse
        - Med (somewhere between engi and mult bomb range)
    - Stats
        - No stocks

### Combine:

- Behavior
    - Makes lingering explosion when explodes
    - “Impacts” with lingering explosion and combines
    - When 3 are combined they gradually expand to a point then blastattack
        - If you throw bombs into it while it’s expanding, the expanding time resets and it continues expanding to an increased area (and damage?)
            - If not damage then area expands at an accelerating rate to encourage
                - And cause i want to see it cover the world
    - Purpose?
        - Most aoe?
- Fuse
    - Med to Short
    - Maybe also on impact
- Stats
    - 3 stocks
    - med-ish cooldown, isbullets
- Thoughts
    - Cluster is for the big damages over multiple hits, decentish aoe.
        - This one either more for aoe, or similar aoe but shorter cooldown.
        - Ah, also this is shorter range.
            - - ~maybe
        - In sk I used this as a main one sometimes, maybe it has no cooldown like default but has that limit of 3
        - Orbit this and blast into enemies that sounds fun
        - Maybe blast jump should be aimable

### Tracer:

- - Behavior:
        - - On explode, Sends 2 or 3 thingys forward they climb stuff n stuff
    - Purpose?
        - Piercing? For long lines of enemies
    - Fuse
        - Impact
    - Stats
        - 2 stocks
        - short-med cooldown, isbullets?

### Zappys:

- - Behavior:
        - Does not impact enemy, only explodes after timer
        - Hangs in air, loader pylon-ing close things
        - pops at the end super weak ion bomb
    - Purpose
        - General dps. Most likely just used with orbit while you switch to other stuff.
        - Throw and leave in areas
        - Maybe add a slow or shock
    - Fuse
        - long
    - Stats
        - 3 stocks
        - short-med cooldown, isbullets

### Fire:

- - Behavior
        - On explode, drops thing to floor
        - Spreads for a bit
            - Cool graphic of fire pillars forming
        - Essentially big shroom cum stain, but wider and maybe shorter
            - Could also be a magefirewallcontroller and be a sideways pillar
    - Purpose
        - Area control
    - Fuse
        - Short-ish
        - Thinkin apex of a throw
    - Stats
        - 1 stocks,
        - med-long-long cooldown
    - Thoughts
        - Proc still 1 on fire ticks
            - Probably more reasonable a first blast that procs, but I want the many proc tics anyways
        - Formerly “Maybe burns dot to differentiate from cluster a bit more”
            - It’s pretty differentiated as the cluster is big burst damage with multiple things (and long range) whereas this is more area denial continuous damages lasting longer

### Cluster:

- - Behavior
        - When explodes, big blast of multiple repeating blastattacks
            - Nice procs
            - Multiple explosion areas venn diagramming in the middle
    - Purpose
        - Big damage long cooldown Das it
        - Less aoe than combine, bit less than fire pool area probably
        - The intersection of the blasts is where big damage happens
        - Repeating?
    - Fuse
        - Long or impact
    - Stats
        - 1 stocks
        - long long cooldown

## Fuse:

- We got Reg/short/long/impact, remote, homing
- Reworked homing and remote as casings
- Reworked the rest as default timings depending on powder

# 

# M2: Arcana

- Idk if we switch arcana on the fly (unless pandemonium heheheh).
- they’re just alts
    - That’ll work fine
- We got big boom, smoke boom, bait boom, vat, fleet flass, bereserk flask, leech flask, up staff, wacky staff

### Big boom:

- - Fuk it it’s a big boom. We can have it knock back to give it utility
        - Knocks away and it’s a get off my ass move
            - Then you’re raining down in all directions at them Ye I like it
        - Perhaps knocks forward way from you so it’s not _too_ scattering
        - Or Knock them inward fuck it?
- Staff animation forming the bomb
    - I wanna incorporate staff into the animation for all of these
- Current powder? Casing too? M1 but huge?
    - Kinda devalues the difference in powders probably. Also probably a nightmare to do with how different the projectiles are.

### Smoke boom:

- - Big ol smoke cloud ~~nothing unusual here~~
    - ~~Maybe~~ actually gives stealth here~~?~~
        - Well that’d suffice the damag part cause being invis lets you just hurl bombs at them while they don’t notice
        - This dynamic is fun. ~~I wanna bump this priority now~~
    - Idk what the animation is in game but in this game, the staff glows and he spins around while it spits out smoke
        - Enforcer tear gas ezpz

### Bait boom;

- - ~~Probably just cut it.~~
    - If I don’t it’s gonna you throw like 3 and it seeks to an enemy and knock them up
    - Stuns
        - Maybe brought to you for epic comboing?
    - Yes
    - Holds staff forward and these little guys spit out

### Vat:

- - We jumpin everywhere and avoidin kniggas everywhere n shiet
    - Smallhop in the air and spawn a floating vat under you you can stand on
        - Get afterburners and spawn a bunch
            - Boom you just did the boss attack heh
        - After a sec the vats fall and explod
    - Staff glows and points downward
        - Maybe vat forms first and staff pukes into it fills it up?

### Fleets:

- - Fits pretty well.
    - Maybe shorter distance?
    - In original you go through stuff. Idk bout this game
        - Maybe hit them and get knocked back. We’ll tinker with it
        - Wait why? I question my design power every day
    - Hmm guess I can’t make the flask ones use the staff
        - Either they’re just pulled out of the animator’s satchel or they also form from the staff somehow
        - Maybe he pulls out the bottle fills it with the staff then drinks it

### Berserks:

- - Invince and maybe drastically lower cooldowns
    - I guess i was too harsh on this earlier. Invince can help pretty good for spamming bombs close range at peeps
        - Guess i need to differentiate from smoke bomb tho. Invince is a little different from invis so that’s probably enough
        - Maybe smoke applies a debuff like tear gas
    - Whatever i decide for flasks above

### Leechs:

- - Hits give health for a bit
    - How the HECK do I balance this?
    - Maybe just keep it busted for healing cause berserk already accomplishes and much better at that the keep you alive to esplod shits
    - Old thoughts
        - How the HECK do I balance this?
        - I suppose just make it only the next hit? Perhaps percent of your health. Super quick heal kinda thing but nothing you can rely on. Yeah that sounds ok
        - I presume he’s gonna be pretty squishy, so this should let you more reliably dish out a lot more damage without dying. If need be it can give barrier too, but that’ll probably be best left to synergizing with items instead
    - Whatever i decide for flasks above

### Up staff:

- - 2 charges
    - Go up do some damages
        - Like 3 hitboxes
        - Maybe holds you in the air or gives you free flight or somethin n you can get some air bombin time
    - Hitbox is a decent area in front of you that brings enemies together (maybe twirls them a bit) and lifts them up with you and drops them in front of you
        - Lift off and fuckin bomb em good
    - Uses staff for animation

### Wack staff:

- - 4 charges (isbullets?)
        - Supafast
        - Get dem mags and supafast some more
    - Big ol range probably just merc or somth
    - Get off my ass knockback move? Stun?
        - Gives mobility? So you can run around and knock things into a bombing spot?
    - Uses staff for animation

## More think:

- Well shit we did it
- So in order of let’s do it:
    - Big boom, Vat, Smoke, Wack,
    - Leech, Bait?, Fleets, berserk, Up staff

# 

# Shift: bomb jump

- The just alts in the loadout
    - Unless you have pandemonium of course
- We got reg boom, shooty boom, reg boomb mini with float, icy boom, spinny boom (bouncy)
    - Is ice boom just float boomb with the ice things?
        - If not it is now
- So I have more excuse to concept out here

### Reg Boom:

- - Does a blast attack and jumps you up (and forward)
        - Ion surge with forward momentum?
        - How much air control?
        - ~it is done and it is funny
            - Oh wait I still need to do the gravity thing

### Shooty Boom

- - Shoots a thing forward
        - Just a phase round? This is pretty meh...
            - ...and I hate to say this...
                - ...in 3d
        - Maybe more like golem Lazer but with tracer like it's an instant ranged blast
            - Or just really really fast
        - Yea It’s not so bad in 3d after all. You gotta aim and you get an extra hit before you bomb on em.
            - I’m cool with it. Could have the utility of blasting around and stunning
                - Oh wait that’s it eureka that makes this good

### Floaty Boom

- - Keeps in the air for you to throw bombs more
    - While using this it essentially gives you an arti hover you can hold, but fades over time kinda

### Icy Boom

- - Guess this needed writing out after all
    - Combine with floaty?
    - K nvm floaty giving little arti hover makes it definitely worth its own thing
    - It’ll be a little floatier than other jumps maybe, just not to the same degree
    - Having the snowflakes do like a slow n stuff is great utility for looking back and bombing on em

### Spinny Boom

- - Spibbity bop bounce off walls n stuff
    - Oh wait bounce was a cloak
        - Hmmmmm
        - Won’t be too bad to make it an alt
    - You do damage to stuff you pass through in the air
    - Throwing bombs interrupts it
    - If you didn’t throw a bomb you can land with it and it does a blast

# Special: change bomb

- He’s gonna be a little micromanagey I love it

**![](<Attachments/Attachment 12.png>)**

Old image without remote casing

Homing casing will be float casing with the homing fuse

Remote casing will be lob or drop casing with remote fuse

- You can still move around while this menu is up, of course
- When you use a powder and it goes into cooldown, if you try to use it again, that’s when it automatically switches back to reg powder and throws that
    - So you can hang on it and wait for another one if you want
    - That or it shows the cooldown for 1 or two seconds then automatically switch back
- Will really have to feel out how this menu is to use in as much faster paced game
- Scepter all powders get an extra charge?
    - You throw your last two selected powders at the same time?
    - You get access to a 7th “powder” selection that throws all types at once?

Other

# Skans

- Ward robe: mastery
    - Now that i’ve worked with folks, the fuckin hardcore amiibo costume might be a thing O.o
- Gold:
    - Get to stage 4 without spending any money
    - Or maybe this is mastery and ward robe is some kinda survival based achievement
- Pandmeonium:
    - Unlock all alt M1 and M1-2 (misc)
    - Gameobject activation
- I mean holy shit if someone wants to make the big boi amiibo model i will totally add that
    - It will be another field, and will work with other skins as paletteS

- skin thoughts (deleted previous thoughts now that I know how game works)
    - Models will be skins, palettes will be a genericskill field
        - Easy to check for the goldyboy animations, and for PANDEMONIUM
        - Then of course easy to check for passive thingys if I do that
    - Big model will definitely be grandmaster or something even harder

He totally smokes hookah (thoughts)

## Important thoughts

- ””””important””””
    - Mainly cause all this stuff has either been decided or is just old
- Thinkin about attack speed
    - You micro manage a bit faster but... eh yeah that’s about it that’s fine
        - I was kinda worried how the relationships of using them with cooldowns n whatever matters but it’s good.
            - It’s gonna be good i can’t wait
        - Little bit of you can throw way more reg bombs while you wait for the others’ cooldowns
    - Holy fucking shit the below one got long and I don’t want to waste my future life time reading through all that. TL;DR
        - Combine powders mainly useful
        - Maybe maybe animation times (but mainly end times. Beginning times feel shit, see CHEF.
            - Weapon entitystate of course different from R switching entity state. No matter what bomb you’ve currently switched to, there’s a bit of waiting for the big boi bombs animation to finish throwing
                - Or just have every bomb interrupt the previous like fuck it dude. Don’t want to make them feel shit just to balance attack speed
        - Maybe maybe maybe throw arc speed is faster too. Attack speed just fast forwards your gameplay in general
            - Might be cool, honestly. Fuse “time” becomes fuse distance (but maybe attack speed allows for longer throws?)
            - HMMMMMMM
    - Usually high enough attack speed becomes “spam primary and throw others in there lil bit” so idk the primary ain’t that great and using the other moves is kinda needed
        - u so - combine powders are mainly what’s gonna benefit from this
        - u other - the m2s?. Yeah that was basically it
            - u - merc lol. That’s it. That’s what in and out always makes me think. Hope there wasn’t another point here that I forgot
        - u m2s - would be very weird but (and well fuck it wojldn’t even work) could have the bombs themselvevs (oh wait) have effects based on attack speed?
        - u - but instead of that, the throw arc could be faster hmmm.
        - Throw arm based on attack speed is a weird concept but like idk. You’re already throwing a projectile so it’s a delay where the thing hits and does damage anyway? -(oh yeah this was fucking horrible on chef).
            - I’ll settle for just the animation getting sillier.
            - Could maaaaaybe already throw the projectile but just hide it til the animation finishes?
- Oh yeah staffy smacky. Should that just have no cooldown fuck it?
    - reason to stop using it would be simply the fact it's melee range and we're not switching out like in Shovel knight so you'll have a lot more consistently in and out playstyle.
    - this was originally a joke idea but yeah now this is straight up feeling like the way it should actually be
    - oh yeah mags will be literally useless
        - hard coded double damage swing fuck it?
        - well in that case I can design a new cooldown thing -(almost like wol dashes actually) where you do have a charge on a cooldown but you can still swing with it on cooldown it just doesn’t have that charge to do double damge or something or other or whateves.
    - So yeah for mags maybe a stock of something on top of swings and without that available it’s just regular swings
- Grab green coins to unlock stuff
    - From Thought What to do to unlock alts?
    - X amount per stage
        - Placed in places, maybe randomized secrets ror1 artifact style
        - Maybe drops from enemies
            - Yoink from lunar coins
    - Little plaguatorium or whatever it’s called in the tunnel to void fields
        - Little lunar cauldrons and you spend your plague coins to unlock each casing/powder
- Special boss plague knight with boss moves?
    - exploding vats
    - shadow clone jutsu
    - Teleport
    - This will absolutely never happen but i would absolutely love it absolutely
        - I fucking want the pandemonium cloak in here somewhere
            - u - Holy fuck I should make it actually the skin
                - Unlocks when you’ve unlocked all other bomb variants
            - Couple other palettes. Default, goldylocks, prob red n black, then pandemonium
                - u red - it’s called ward robe it wins
                - u pal - Goldy’s gonna actually do other animations
- u - when well I freaking learn that these projects with these super legit implementatinos will probably never happen?
    - Granted this is a lot less ambitious than full RogueL child inheritance system, but still. All of the amazing things I wanna do I’m maybe not even gonna be able to do. I gotta get in contact with a good 3d modeler
        - We got an animator boyo kiarac#0417
        - <we also got an animator it’s called fuckin me>
            - <also think rob liked the idea of arms in widepeepoHappy so he might do some too>

## Fun thoughts

- Design vases based on casing, and bowls (and smoke), based on powder (and stem is fuse)
    - Idle
    - Dance emote maybes
        - In which case also hookah emote
- Alchemist’s haven slowly fades in from the background when you’re in the loadout screen
- ~~Ctrl~~ while standing still to do tiny crouch
- Jump victoryanimation when proceeding through the teleporter
    - And twirly one for gold cloak
    - Oh this is an emote c:
    - Guess little crouch and dance can be emote button too.
- sound/effect referencing his life potion thingies increasing his max health on shield/barrier
    - u - Can add it as an equipment too :O
        - Life potion (whatever it’s called). Use to heal and increase maximum health temporarily for each consumed. Enemies have a chance to drop potions that refill charges of this