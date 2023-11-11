[//]: # (Version 1.0.0, ready for use.)

From here: https://youtu.be/493h3MxcF6Q 

# Freeform Universal Character Outline converter.

[//]: #  I usually create a basic character outline for my npcs in google docs.  
[//]: #  I need to convert the outline to a spreadsheet format I use when Game Mastering the Free Form Universal format.  
[//]: #  This prompt allows ChatGPT to do that.
[//]: #  NOTE: How to use it:
[//]: #  In google docs, select the outline you want to convert. 
[//]: #  Main menu | Extensions | Select "Docs To Markdown".  
[//]: #  Click on the "Markdown" button to the right.
[//]: #  The outline will be converted, select the outline as markdown in the output area and copy it.
[//]: #  Paste outline into the prompt below and then copy the entire prompt.
[//]: #  Paste the first prompt into ChatGPT.  It will create the tab delimited table.
[//]: #  Verify the table is correct.  If not, repeat and revise.
[//]: #  If so contine:
[//]: #  Submit the second prompt to generate a code block.
[//]: #  Copy the tab delimited output into Sublime Text.
[//]: #  Replace the tab symbols ("\t") with real tabs (type a tab, and cut and paste it into the replace field).
[//]: #  Copy and paste the output into your spreadsheet.
[//]: #  NOTE: It's clunky but the best I could do. By replacing "\t" yourself, the tabs will all line up correctly in google sheets.

## P1

You are data format expert. Your task is to take bullet point outlines of characters for a role playing game and convert the outlines to a table. Any properties that are missing in the outline should be replaced with empty strings in the table. For any columns that contain the word "Stress", set the value to the number 4.  If there are properties that don't match a given output column, place the property information in the "GM Notes" column cell. 

Here are the tab delimited headers for the table:

Timestamp	PlayerName	CharacterName	Concept	Stress - Will	Stress - Health	Edges	Flaws	Gear	Skills / Actions	Equipment	Image Link	Goals	Relationships	Notes	GM Notes

And here are the outlines of the player characters:

* Non Player Characters
    * The four knights of the campaign
        * King Knight
            * Location
                * Lives in Pridemoor Keep
            * Edges
                * Charismatic, leadership
                * Speaks and friends with Rats
            * Flaws:
                * Mama’s boy:  desires approval from his mother.
            * Gear
                * Sceptre of Royalty (used as a charisma bonus when wielded.
                    * +1 on attacks.
        * Mole Knight
            * Location
                * Lives inside a lost city under a volcano.
            * Edge:
                * Digging, dwarven dungeon knowledge
                * Fire master (magic fireballs, controlling fire).
            * Flaw:
                * Very slow with regular actions.  Last to get initiative (unless underground, then first).
            *  Gear:
                * Fire spouting armor (ranged weapon, 360 degree cone of affect.
                * Claws (for tunneling and melee).
        * Tinker Knight
            * Location
                * Lives in Mechanist Tower (cloud high tower where he works on his invention)
            * Edge:
                * Mechanical Engineering (fabricating devices).
                * Great at using his own devices.
            * Flaw:
                * Quite small
                * Unintimidating
                * Clumsy
            * Gear
                * Trusty Wrench (melee combat in a pinch, but adds to his fabrication roll).
                * Motorized unicycle platform vehicle.
                * Keychain of transforming keys.  Each key transforms into a device he can use.
        * Treasure Knight
            * Location
                * Lives in a submerged iron whale that is fixed to the bottom of the sea (NOT a submarine).
            * Edge:
                * Plundering Ships
                    * Sailor and Captain abilities
                    * Scuba diving, maneuvering.
                    * Student of the Sea
                * Thieving
                    * Pirate stuff, so deceit, intimidation, influence, slight of hand, acrobatics.
            * Flaw:
                * Greedy
            * Gear
                * Hand Cannon
                * Diving Suit
            * Equipment
                * Mini sub/boat (for reaching the Iron Whale)
        * Cameo from Propeller Knight
            * Edge:  Flying, French, Great with Women
    * The Patron
        * Mr Hat (the patron)
            * Edge:  Can wear different hats and gains the power of that particular hat.

# P2

Convert the table to tab delimited format. For the tabs, use the character sequence "\t" instead of an actual tab character. If using a code block to present the tab delimited table, set the language for the code block to "Text".

# P3 (Optional)

Repeat these last two steps  for these additional characters.

