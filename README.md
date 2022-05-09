# General Ideas for CSE 210 Game project
---
* Idea 1: Maybe some sort of card game, using W03's custom Deck/Card classes?
    * Definitely make a custom deck of cards with fancy effects
    * Perhaps the cards can somehow serve as the weapons used in Idea 2?

* Idea 2: Side-scroller action-y platformer with time travel?
    * "Hold (button) to rewind" style of time travel, similar to Forza racing games.
    * Time travel achieved via holding most-recent 5 second (or X frames, similar to 5 seconds) of game-state variables in an array and applying them to current game-state in backwards order.


## More specific details/Fleshing it out
---
* combine General Ideas 1 and 2
    Title: Ace of the Hourglass
    
    movement: arrow keys
    special abilities: 1-4
        special abilities represented by finding the Aces of the 4 suits of the custom, magical deck.
            MAYBE each magic effect also has a downside?
                maybe make this an optional "hard mode" accessible from the main menu?

        Ace of the Moon allows user to create a 2-way, straight-line portal a certain distance away
            limit 1 portal at a time, portals last indefinitely, but creating a new one deletes the old one
            DOWNSIDE: enemies and projectiles can go through portals, too, maybe?
        Ace of the Sun allows user to reverse the direction of gravity
            walk across ceilings to avoid traps/falling/etc
            flip enemies into traps
            DOWNSIDE: player may take fall damage if they hit a floor/ceiling while going too fast
        Ace of the pocketwatch allows user to pause time for 5 seconds
            stops enemies from moving (so player can avoid them or get some free damage on them)
            stops projectiles (so player can avoid them)
            DOWNSIDE: after the 5 seconds are up, the player himself is frozen for 1 second
        Ace of the Hourglass allows player to rewind time up to 5 seconds into the past
            if player misses a jump they could've made or takes a hit they could've avoided, they can undo it and try again
            pressing multiple times does not send you further back in time.
            DOWNSIDE: rewinding through the same second multiple times damages player
                (i.e. press rewind at 54 seconds, rewind to 49 seconds, if you have to rewind again and end your rewind between 49 and 54 seconds, you take damage)