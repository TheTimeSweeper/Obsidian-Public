meh this one didn't convert so well. [Koal](https://docs.google.com/document/d/19QxwHmiLL0ORkXkdVE_uowtixcsOHM6kjcGITx209XE/edit)
# Combo attackin

M1 and M2 are attack combos. Leaning toward action dmc-style whatevs with different moves, but not going the red mist input direction route to do it. We’ll do it somewhat like a fighting game

- M1 is let’s say 4 hit combo with sword/spear
    - Fancy n swipy n elegant n such
- M2 is let’s say 4 hit combo with shield
    - So a “use” of a “charge” gives you 4 attacks to use before it goes on cooldown
- So, M1+M1+M1+M1 is fancy sword combo
    - M2+M2+M2+M2 combo with shield
- Alternate between these to make different combos
- Some thoughts, I’d like first m2 of any combo to have a dash to it, for some mobilitizing
    - Lunge a bit, shield bash
    - The dash will go in the direction you’re inputting first, then attack forward
- That’s as an example. We can have different parts of the combos have different utilities to them

## Ways to go about this

### M1 and M2 always do those 4 attacks, and you can spread them however you like

- 1 1 1 1 sword combo
- 2 2 2 2 shield combo
    - Mix and match how you like
- When you finish one of the combos, the combo concludes
- Easiest on development (only need 8 moves), but least exciting
- Examples
    - 2 1 2 1 2 1 2 7-hit combo which will end in a shield finisher
    - 1 1 2 2 2 2 and the 4th m2 has been used so it ends it at 6 hits
    - 1 1 2 1 1 with a sword finisher
    - 1 1 1 2 2 2 1 for another full 7 hit
- To add some variety, we could have the last finisher vary with how long the combo has been, or the moves you used to get there, etc

### Just do marth side b

- Combos are always 8 moves. Swapping the move always plays the same move at that place
- (Now 16 moves. Maybe only 6 so just 12 moves)
- Again, boring, but feasible

### Interrupting moves with the other kind changes the combo

1. So you have

- The default combos
    - 1 1 1 1 is the default set of sword attacks
    - 2 2 2 2 is the default set of shield attacks
- But use m1 first, then follow with m2s, it leads to a different shield combo
    - So with 1 1 2 2 2 2, those m2’s are the second set of shield attacks
- Every two moves changes the combo
    - 2 2 2 2 default shield set
    - 1 2 2 2 2 default shield set
    - 1 1 2 2 2 2 alternate shield set
    - 1 1 1 2 2 2 2 alternate shield set
    - 16 moves, 4 finishers
        - Can reduce to 12 with 3 hit combos

1. Finally, we finish the combo by doing a full set in a row

- So a combo is actually infinite if you keep alternating
- Combos would look like
    - 1a 1a 1a 1af default sword
    - 1a 1a 2b 2b 1b 1b 1b 1bf def sword → alt shield → alt sword
    - 2a 2a 1b 1b 2b 1a 1a 2b 2b 2b 2bf def shield → alt sword → alt shield → def sword → alt shield
    - 1a 2a 1a 1a 2b 1a 2a 1a 2a 1a 1a 1af etc
- You can just do 1 2 1 2 1 2 1 2 but you’re gonna run out of m2 stonks
    - So backup mags will extend how long you can combo

### Number 2 but every combo is personalized

Simplify to 3 moves, every move in a combo changes the next combo
- 1a 1a 1af spear set 1 - basic spammable combo
	- Spirit orbs increase final hit range
- 2a 1b 1b 1bf spear set 2 - dazzling between enemies
	- Spirit orbs increase amount of enemies dashed to?
- 2a 2a 1c 1c 1cf spear set 3 - beyblade spin, repeated hits, lots of procs
	- Spirit orbs increase number of spins
- 2a 2a 2af shield set 1 - knocks enemies forward
	- Spirit orbs shoot seeking projectiles
- 1a 2b 2b 2bf shield set 2 - slam floor, big shockwave that gathers enemies in middle
	- Spirit orbs give barrier per enemy hit
- 1a 1a 2c 2c 2cf shield set 3 - combine spear and shield big axe finisher
	- Spirit orbs increase execution threshold

- That’s 18 moves
- But really it’s only 6 combos. The finishers are the only moves that need to stand out. The others can be fodder to get there.

# Ragon’s Sexy Concepts

![](_Public/img/Attachment%203.png)

![](<Attachment 1 1.png>)