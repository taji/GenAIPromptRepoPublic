[//]: # (Version 1.0.0, rough, but ready for use).

[//]: # (

Thoughts on the design of this prompt:
  - There are three main pieces used in this prompt, the story outline to analyze, the template of the desired output (the CLUE TEMPLATE), and the list of properties to use to guide the AI in generating the CLUE OUTLINE (which lists the clues and how they are connected to the details of the case). I wanted to clearly define these so I used unique delimiters for each piece.  Not sure if this was necessary, but by displaying the pieces after injecting them into the Chat, I verified that ChatGPT was recognizing them.
  - One of the things that helped a lot was adding the AUTHOR and STORY_TYPE parameters.  Switching to Lovecraftian Horror added lot's of Lovecraftian tropes and ChatGPT did a good job of mixing them with the Hogwarts details. 
}

> NOTE: 
 - This is a complex prompt so sometimes it will add too much or too little detail in the generated outline.
 - Regenerate until the structure is correct.
 - This one requires some finessing after decent results are generated.  See the additional prompts for details.
 - Each of the clues in the outline has a specfic name. Once you have a halfway useable outline, copy it to a text editor and keep working on the clues of the outline in ChatGPT, mergine the new clues into your text editor. 

# P1 The STORY OUTLINE example.

*Paste this into ChatGPT as-is.*

You are a mystery roleplaying game scenario author. 
Here is a STORY OUTLINE of details for a potential crime. The contents of the STORY OUTLINE is delimited by triple colons below:

:::
TITLE: THE GRINGOTT'S HEIST

STORY SUMMARY: As soon as Harry Potter, Hermione Granger, and Ron Weasley discovered the existence of a horcrux that belonged to Voldemort and was stored in a magically secured vault at Gringott's Bank, they knew that they had to retrieve it. With the help of a goblin accomplice named Griphook, they planned to use polyjuice potion to disguise themselves as Gringott's employees, and an invisibility cloak to slip past the security measures. They knew that they would have to be quick and careful, but they were determined to succeed in their mission.

STORY OUTCOME: The potential outcome of this heist could mean the end of Voldemort's reign of terror. If the young wizards are successful in their mission, they will be able to destroy the horcrux, and Voldemort will lose a significant part of his power. However, if they are caught, they could face severe consequences, including imprisonment in Azkaban.

CRIME MEANS: Harry, Hermione, and Ron will use a goblin accomplice named Griphook to gain access to Gringott's Bank. They will also use polyjuice potion to disguise themselves as employees and an invisibility cloak to avoid being detected.

CRIME MOTIVE: The young wizards' motivation for committing this crime is to find and destroy a horcrux that belongs to Voldemort. They believe that this is a necessary step in defeating him and ending his reign of terror.

CRIME OPPORTUNITY: The opportunity to commit the heist arises when the goblin accomplice, Griphook, agrees to help them. The young wizards also learn of the location of the horcrux and the security measures in place, which they will use to their advantage.

STEPS NEEDED TO BE PERFORMED BY THE CRIMINALS TO COMMIT THE CRIME:

Obtain polyjuice potion and invisibility cloak.
Meet with Griphook to plan the heist.
Use polyjuice potion to disguise themselves as Gringott's employees.
Infiltrate Gringott's Bank using Griphook's help.
Use the invisibility cloak to avoid detection by security measures.
Break into the vault
Retrieve the horcrux.
Escape Gringott's Bank undetected.
Destroy the horcrux.
:::

Display the contents of the STORY OUTLINE excluding the delimiters.


# P2 The corresponding STORY PROPERTIES LIST example.

*Paste this into ChatGPT as-is.*

Here is the STORY PROPERTIES LIST that provides data to be used when analyzing the STORY OUTLINE:

STORY_TYPE = harry potter type fantasy

AUTHOR = J.K. Rowling

INVESTIGATORS = Death Eater

START_NODE = Hogwarts School of Wizardry

START_PERSON = Draco Malfoy

NODE1 = The Forbidden Forest

NODE2 = Shell Cottage

NODE3 = Griphook The Goblin

END_NODE = Gringott's Bank

CLUE_TYPE = Any items in this list: spell books, magic history books, a book in the library, an item in Hagrid's hut, an item in the Room of Requirement, the statues at Hogwarts, a trophy in the trophy case at Hogwarts, a secret passage, the Marauder's Map, the paintings at Hogwarts, tools, trash, rubbish, blood stain, broken window, broken door, broken mirror, broken branches, arcane residue, footprints, psychic residue, receipt, clothing, weapons, weapon parts, witnesses, questioning, official records, a home address, background check, body, body part

Display the contents of the STORY PROPERTIES LIST.

# P3 The CLUE TEMPLATE example

*Paste this into ChatGPT as-is.*

Here is a CLUE TEMPLATE that provides the format to be used when displaying the generated analysis of the STORY OUTLINE.  The CLUE TEMPLATE is delimited by triple carats below:

^^^
TITLE: [Insert story title here. Use ALL CAPS]

START: [Insert {START NODE} and {START_PERSON} values here, in all caps]
  \- CLUE TO NODE1: [Insert details for a clue that leads the investigators to {NODE1} from {START_NODE} or {START_PERSON}, like this: "Footprints found at Hogwarts match the shoes of Harry, Ron and Hermione. The footprints lead  into the Forbidden Forest"]
  \- CLUE TO NODE2: [Insert details for a clue that leads the investigators to {NODE2} from {START_NODE} or {START_PERSON}, like  this: "Draco Malfoy informs the investigators that Ron Weasley's brother Bill lives at Shell Cottage near Ron Weasley's famiily home.  Harry, Ron and Hermione may be staying with Bill at Shell Cottage."]
  \- CLUE TO NODE3: [Insert details for a clue that leads the investigators to {NODE3} from {START_NODE} or {START_PERSON}, like this: "A Slytherin student at Hogwarts informs the investigators that a Goblin named Griphook was traveling with friends of Harry, Ron and Hermione."]
  \- CLUE TO END_NODE: [Insert details for a clue found at {START_NODE} that leads the investigators to {END_NODE}, like this: "A deposit slip found on a Hogwarts student reveals that a Horcrux is stored in one of the vaults at Gringott's bank."]

NODE1: CLUES AT  [Insert {NODE1} here, in all caps]
  \- CLUE TO NODE2: [Insert details for a clue that leads the investigators to {NODE2} from {NODE1}, like this: "A centaur in the Forbidden forest witnessed Ron Weasley using the Floo Network to travel to Shell Cottage."]
  \- CLUE TO NODE3: [Insert details for a clue that leads the investigators to {NODE3} from {NODE1}, like this: "One of Griphook's accomplices is captured in the Forbidden Forest.  He reveals where Griphook is hiding."]
  \- CLUE TO END_NODE [Insert details for a clue found at {NODE1} that leads to {END_NODE}, like this: "A list of ingredients to make Polyjuice potion is found in the Forbidden Forest.  Written on the list are notes about the security at Gringott's Bank." ]

NODE2: CLUES AT [Insert {NODE2} here, in all caps]
  \- CLUE TO NODE1: [Insert details for a clue that leads the investigators to {NODE1} from {NODE2}, like this: "Bill Weasley is captured at Shell cottage.  He crack's under questioning and reveals that Harry, Ron, and Hermione were brewing Polyjuice Potion in the Forbidden Forest."]
  \- CLUE TO NODE3: [Insert details for a clue that leads the investigators to {NODE3} from {NODE2}, like this: "At Shell Cottage, there is food and drink that is preferred by Goblins. This may indicate that Griphook is staying at the cottage."]
  \- CLUE TO END_NODE [Insert details for a clue found at {NODE2} that leads to {END_NODE}, like this: "A set of floor plans for Gringott's bank is found in the trash bins at Shell Cottage." ]

NODE3: CLUES AT [Insert {NODE3} here, in all caps]
  \- CLUE TO NODE1: [Insert details for a clue that leads the investigators to {NODE1} from {NODE3}, like this: "The investigator's are notified by the Ministry that Griphook has been captured in the Forbidden Forest."]
  \- CLUE TO NODE2: [Insert details for a clue that leads the investigators to {NODE2} from {NODE3}, like this: "Searching Griphook's backpack, they find a photograph of Griphook, Harry, Ron, Hermione and Bill on the beach near Shell Cottage."]
  \- CLUE TO END_NODE [Insert details for a clue found at {NODE3} that leads to {END_NODE}, like this: "Questioning Griphook reveals that Harry, Ron and Hermione are planning to rob one of the vaults in Gringotts Bank." ]
^^^

Display the contents of THE CLUE TEMPLATE excluding the delimiters.

# P4 Sanity Check (for testing and debugging).

*Paste this into ChatGPT as-is.*

Analyze the STORY OUTLINE and apply the STORY PROPERTIES LIST to the contents of the CLUE TEMPLATE above to generate a CLUE OUTLINE. Fill out the CLUE TEMPLATE for a {STORY_TYPE} story in the style of {AUTHOR} involving the player character investigators beginning their investigation of {CRIMINAL} committing the crime of {CRIME} at {START_NODE} or {START_PERSON} and finding clues that lead to {NODE1}, {NODE2}, {NODE3} and {END_NODE}.

# P5 Here is a STORY OUTLINE I'm working on

*Replace this with any outline you choose.  Be sure to call it the "**NEW** STORY OUTLINE".*

Here is a NEW STORY OUTLINE of details for a potential crime. The contents of the NEW STORY OUTLINE is delimited by triple colons below: 

:::
TITLE: THE SOUL JAR

STORY SUMMARY: The Death Eaters have hatched a plot to restore Voldemort to power by using a spell called "The Soul Jar" to store his soul inside the body of a young boy. They have identified a suitable candidate, a young wizard named Rupert Ham, who they plan to hypnotize and use as a vessel for Voldemort's soul. To carry out their plan, they will need the help of a professor named Aldus Norwitch, who has knowledge of the spell, an intellect devourer to help them control Rupert's mind, and a final ritual and spell to place Voldemort's soul inside the child's body. If they succeed, the Wizarding World will fall under the tyranny of Voldemort once again.

STORY OUTCOME: If the Death Eaters succeed in their plan, the Wizarding World will fall into darkness and tyranny under the rule of Voldemort. However, if they fail, they will face imprisonment or worse, and the Wizarding World will be safe once again.

CRIME MEANS: The Death Eaters will use the "Soul Jar" spell to store Voldemort's soul inside the body of a young boy named Rupert Ham, who they plan to hypnotize using an intellect devourer. They will then use a final ritual and spell to place Voldemort's soul inside the child's body, completing the transfer of power.

CRIME MOTIVE: The Death Eaters want to restore Voldemort to power and impose their twisted beliefs on the Wizarding World.

CRIME OPPORTUNITY: The opportunity to carry out the plan presents itself when the young wizard Rupert Ham is discovered and targeted by the Death Eaters. They will use their influence and resources to carry out the spell and hypnotize Rupert to ensure their success.

STEPS NEEDED TO BE PERFORMED BY THE CRIMINALS TO COMMIT THE CRIME:

Make contact with Aldus Norwitch and bribe him into performing the Soul Jar spell
Collect and prepare the ingredients required to complete the Soul Jar Spell
Kidnap Rupert Ham and bring him to the secret temple beneath the black lake.
Use an intellect devourer to hypnotize Rupert and control his mind.
Perform the final ritual and spell to place Voldemort's soul inside the child's body.
Ensure that Rupert is kept safe and hidden until Voldemort's power is fully restored.
:::

Display the contents of the NEW STORY OUTLINE excluding the delimiters.

# P6 And the corresponding NEW STORY PROPERTIES LIST

*Replace this with any list you choose.  Be sure to call it the "**NEW** STORY PROPERTIES LIST".*

Here is the NEW STORY PROPERTIES LIST that provides data to be used when analyzing the STORY OUTLINE:

STORY_TYPE = A Lovecraftian Horror

AUTHOR = H.P. Lovecraft

INVESTIGATORS = the students at Hogwarts

CRIMINAL = The Death Eaters

CRIME: A conspiracy by the Death Eaters to use the Soul Jar spell to restore Voldemort to human form.

START_NODE = Hogwarts School of Wizardry

START_PERSON = A hypnotized student at Hogwarts named Rupert Ham

NODE1 = The Black Lake

NODE2 = The Shrieking Shack

NODE3 = Dead spiders in the Forbidden Forest

END_NODE = The Altar in the Chamber of Secrets

CLUE_TYPE = Any items in this list: spell books, magic history books, a book in the library, an item in Hagrid's hut, an item in the Room of Requirement, the statues at Hogwarts, a trophy in the trophy case at Hogwarts, a secret passage, the Marauder's Map, the paintings at Hogwarts, tools, trash, rubbish, blood stain, broken window, broken door, broken mirror, broken branches, arcane residue, footprints, psychic residue, receipt, clothing, weapons, weapon parts, witnesses, questioning, official records, a home address, background check, body, body part

Display the contents of the NEW STORY PROPERTIES LIST.

# P7 Repeat the same prompt to regenerate the outline

Analyze the NEW STORY OUTLINE and apply the NEW STORY PROPERTIES LIST to the contents of the CLUE TEMPLATE above to generate a CLUE OUTLINE. Generate the CLUE OUTLINE using the CLUE TEMPLATE for a {STORY_TYPE} story in the style of {AUTHOR} involving the player character investigators beginning their investigation of {CRIMINAL} committing the crime of {CRIME} at {START_NODE} or {START_PERSON} and finding clues that lead to {NODE1}, {NODE2}, {NODE3} and {END_NODE}.

## P8 Optional: replace one of the clues.

*NOTE: This will show all the clues under a node but will only replace the clue specified*

Regenerate CLUE TO NODE2 under NODE3 with new details.

## P9 Optional: Merging new clues.

*You can merge the new clues with the last template as so:*

Display the generated CLUE OUTLINE again replacing NODE3 with the new details.

## P10 Optional: Removing the labels.

*You can remove the labels and clean up the details:*

Display the template again but remove the NODE and CLUE labels.