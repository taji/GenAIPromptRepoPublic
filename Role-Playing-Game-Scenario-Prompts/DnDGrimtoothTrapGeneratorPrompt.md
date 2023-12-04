[//]: # (Version 1.0.0, ready for use, but could use some refinement).
[//]: # - Some of the details feel a bit simplistic
[//]: # - Clues should cascade on top of each other
[//]: # - As in the clues should reveal additional clues ala "You see scuff marks underneath the bed (forcing them to move the bed)" instead of "you find a trap door under the bed"

[//]: For helping make grimtooth traps more polished and ready for use in a DnD session. 
[//]: How to use: Some of the prompts below are optional and should be used as needed.

[//]: Good prompting advice here: https://youtu.be/493h3MxcF6Q 

[//]: Good advice on designing traps here: https://docs.google.com/document/d/1poHINLUeD-FP_rWyZz94svRVk9eqAp60IJb5bGoNMiM/edit?usp=sharing

# P1

You are a role playing game senario analyzer.

Here is the description of a trap found in a dungeon: {TRAP_DESCRIPTION}.

TRAP_DESCRIPTION = "The trap is called "The Fountain Trap" The trap appears to be a beautiful fountain, with a sign written using an ornate engraving that indicates "The Balming Basin of Boo-Hoo".  Its waters cascade down the fountain into the basin, with a slight blue glow emanating from the water's depths, enticing the player characters to drink from the fountain and be healed. The fountain is, in reality, a living creature. Any adventurer who touches this fountain or (perish the thought!) drinks from it will be quickly engulfed and eaten, with varying chances of avoiding certain doom, depending upon the circumstances. The "water' is actually a digestive fluid, which can dissolve any substance but gold . A character stuck in this thing is in a lot of trouble and only a few turns before it is suffocated by the monster."

Answer with "..." if you acknowledge. 
Don't write anything yet.

# P2

Your task is to analyze the trap provided and determine the following components of the trap:

BAIT: [Insert the bait of the trap, similar to this: "The BAIT of the trap is the promise of healing provided by the message in the engraving.  This causes the characters to touch the fountain or drink from the waters. 

TRIGGER: [Insert the trigger of the trap, similar to this: "The TRIGGER of the trap is any player character touching the fountain or the fluid, which wakes the monster and allows it to attack."]

CONFINE: [Insert the details on the element of the trap that confines or restricts the player character and prevents them from escaping, similar to this: "The CONFINE is the fountain creature's enormous mouth that grapples the players and attempts to swallow them."] 

TIME: [Insert the amount of time until the players meet their doom and describe how the players will meet thier doom in the trap, similar to this: "The TIME of the trap is less than a minute until the player's body dissolves inside the creature." ]

CLUES: 

- [Insert a list of 4 clues that would help the player characters detect the purpose or danger of the trap and/or how to avoid it]

Answer with "..." if you acknowledge. 
Don't write anything yet.

# P3 (Execution with new input)

Fill out the template above for a trap described as : {TRAP_DESCRIPTION}.

TRAP_DESCRIPTION = Simply present your characters with the end of a golden thread. The thread can meander through corridors, up and down stairs, through doorways and into pits. If the characters reel in the thread as they go, they might very well become lost. If they merely follow the line to its source, they re in for a nasty surprise. The thread, you see, is really a line of web from a Very Big Spider.

# P4 (Optional)

How can we change the golden web trap so that it is not lethal, but will cost the player characters some kind of resource like health, food, light, time, speed, magic spells or weapons?

# P5 (Optional with a single parameter):

Here is another template: 

OPPORTUNITIES: [Given the {MONSTER} living in the the same dungeon, insert 4 opportunities the player characters could exploit so that the trap could be used against the {MONSTER}, similar to this:  "Given a werewolf in the same dungeon, the player characters could coat the golden web with blood to lead the werewolf to the spider's lair so that the spider and the werewolf will attack each other." ] 

MONSTER = Carrion Crawler

Fill out this template above for the {MONSTER} monster and using the trap described earlier.

# P6 (Optional, but useful):

Shorten the last answer as much as possible.