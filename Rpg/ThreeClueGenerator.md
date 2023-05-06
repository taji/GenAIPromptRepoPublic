
[//]: # (Version 1.0.0, ready for use, but could use some enhancements).
[//]: # - Add MEANS, MOTIVE, OPPORTUNITY for the crime to help the AI flesh out the details and the clues.

From here: https://youtu.be/493h3MxcF6Q

And here: https://thealexandrian.net/wordpress/7949/roleplaying-games/node-based-scenario-design-part-1-the-plotted-approach

Using this example: https://thealexandrian.net/wordpress/7999/roleplaying-games/node-based-scenario-design-part-4-sample-scenario

# DnD Three Clue Rule Prompt

## Usage Guide

Each of the clues listed below has a title.  You can prompt ChatGPT to regenerate any of the clues by giving it the title.

NOTE: Use the one of the following lists for the CLUE_TYPE parameter

PRIMITIVE: If the clue is from a PRIMITIVE monster or person in a primitive setting, use this list: 

- CLUE_TYPE = Any items similar to the items in this list:  body, body part, entrails,  trash, rubbish, blood stain, broken window, broken door, broken mirror, broken branches, arcane residue, animal tracks, animal spoor, animal scat, monster victim, monster tracks, psychic residue

INTELLIGENT: If the clue is from an INTELLIGENT person in a modern setting, use this list: 

- CLUE_TYPE = Any items in this list: trash, rubbish, blood stain, broken window, broken door, broken mirror, broken branches, arcane residue, footprints, psychic residue, receipt, clothing, phone call records, weapons, weapon parts, witnesses, questioning, microfilm, official records, computer records, a home address, background check, body, body part



## P1

You are a role playing game senario author. 
Your task is to describe a list of {CLUE_TYPE} clues that lead a group of investigators to three different destinations (called nodes) during an investigation regarding the crime of {CRIME} committed by {CRIMINAL} for a given {STORY_TYPE} story.
An additional task will be to describe a list of clues that lead the investigators from each node to another node, creating a web of connected clues and destinations.
A node can be either a person or a location.
The investigators begin their investigation at {START} with {START_PERSON}

STORY_TYPE = modern police investigation

CRIME: a terror plot involving detonating bombs in Las Vegas

CRIMINAL = Yassif Manssor, a known terrorist

START = storage unit

START_PERSON = the storage unit manager

NODE1 = the Broadstone Indigo apartment complex on Azure Avenue

NODE2 = The Bellagio Hotel And Casino

NODE3 = Frank Nassar, a corrupt police detective

CLUE_TYPE = Any items in this list:  reciept, clothing, phone call records, weapons, weapon parts, witnesses, clothing, questioning, microfilm, official records, an home address, background check.

Answer with "..." if you acknowledge. 
Don't write anything yet.

## P2

TITLE: [Insert story title here. Use ALL CAPS]

START: [Insert {START NODE} and {START_PERSON} values here, in all caps]:
  \- CLUE START_TO_NODE1: [Insert details for a clue that leads the investigators to {NODE1} from {START_NODE} or {START_PERSON}, similar to this: "Checking the storage unit rental records reveals that Yassif Mansoor signed the lease on the storage space. The address given on the lease agreement is the Broadstone Indigo apartment complex on Azure Avenue"]
  \- CLUE START_TO_NODE2: [Insert details for a clue that leads the investigators to {NODE2} from {START_NODE} or {START_PERSON}, similar to this: "The storage space contains an item of clothing: a bellboy uniform belonging to the Bellagio hotel and casino."]
  \- START_TO_NODE3: [Insert details for a clue that leads the investigators to {NODE3} from {START_NODE} or {START_PERSON}, similar to this: "There is also a disposable cell phone in the storage space. Checking the phone record call log reveals several calls being placed to a number that can be traced to Detective Frank Nasser"]
  \- ANCILLARY_CLUE_FOR_START: [Insert details for a clue found at {START_NODE} that reveals or infers the type of {CRIME} crime being committed, similar to this: "Two detonation caps used when making a bomb weapon can be found behind a cabinet in the the storage space. They rolled back behind the cabinet and were lost while Yassif Manssor was building the bombs and planning the attack."]

NODE1: CLUES AT  [Insert {NODE1} here, in all caps]:
  \- CLUE NODE1_TO_NODE2: [Insert details for a clue that leads the investigators to {NODE2} from {NODE1}, similar to this: "A credit card receipt with a credit card number is found at the storage unit.  If the investigators track recent activity on the credit card, they’ll find that it was used to rent a room at the Bellagio"]
  \- CLUE NODE1_TO_NODE3: [Insert details for a clue that leads the investigators to {NODE3} from {NODE1}, similar to this: "One of the men found at Yassif Mansoor's apartment cracks under questioning and reveals that Yassif Mansoor was at the apartment yesterday with a police detective named Frank Nasser"]
  \- ANCILLARY_CLUE_NODE1: [Insert details for a clue found at {NODE1} that reveals or infers the type of {CRIME} crime being committed, similar to this: "There are six suicide-bomb vests stored in the walk-in closet of Yassif Mansoor's apartment." ]

NODE2: CLUES AT [Insert {NODE2} here, in all caps]:
  \- CLUE NODE2_TO_NODE1: [Insert details for a clue that leads the investigators to {NODE1} from {NODE2}, similar to this: "Yassif Mansoor is found at the Ballagio and is brought in for questioning.  The investigator's run a background check on Yassif Mansoor and determine he lives at the Broadstone Indigo apartment complex on Azure Avenue."]
  \- CLUE NODE2_TO_NODE3: [Insert details for a clue that leads the investigators to {NODE3} from {NODE2}, similar to this: "At the Bellagio, Manoor is found with his terrorist accomplices.  Sewn into the lining of Yassif Mansoor’s jacket is a small packet of microfilm. The microfilm contains official records indicating that police detective Frank Nasser of the Las Vegas police department is guilty of embezzling from a fund used for undercover drug buys. Yassif Mansoor was using these records to blackmail Frank Nasser."]

NODE3: CLUES AT [Insert {NODE3} here, in all caps]:
  \- CLUE NODE3_TO_NODE1: [Insert details for a clue that leads the investigators to {NODE1} from {NODE3}, similar to this: "Frank Nasser is more likely to crack under questioning and reveal his accomplice is Yassif Mansoor and the location of Yassif Mansoor's apartment."]
  \- CLUE NODE3_TO_NODE2: [Insert details for a clue that leads the investigators to {NODE2} from {NODE3}, similar to this: "Frank Nasser can also be placed under surveillance. He will visit both the Bellagio hotel and meet with Yassif Mansoor before the bombings occur"]

Answer with "..." if you acknowledge. 
Don't write anything yet.

## P3 (Execution with new input)

Fill out the template above for a {STORY_TYPE} story involving the player character investigators beginning their investigation of {CRIMINAL} commmitting the crime of {CRIME} at {START_NODE} or {START_PERSON} and finding clues that lead to {NODE1}, {NODE2} and {NODE3}.

STORY_TYPE = harry potter type fantasy

CRIMINAL = Threxulon, a mind flayer

CRIME: A conspiracy by the Death Eaters to over throw the Ministry of Magic using a mind flayer named Threxulon

START_NODE = Hogwarts School of Wizardry

START_PERSON = A hypnotized student at Hogwarts named Rupert Ham

NODE1 = The Black Lake

NODE2 = The Forbidden Forest

NODE3 = Threxulon's Lair

CLUE_TYPE = Any items in this list: trash, rubbish, blood stain, broken window, broken door, broken mirror, broken branches, arcane residue, footprints, psychic residue, receipt, clothing, phone call records, weapons, weapon parts, witnesses, questioning, microfilm, official records, computer records, a home address, background check, body, body part

## P4 Optional prompt to replace one the clues

*NOTE: This will show all the clues under a node but will only replace the clue specified*

Regenerate CLUE NODE3_TO_NODE2 under NODE3 with new details

*You can merge the new clues with the last template as so:*

Display the generated template again replacing NODE3 with the new details

*You can remove the labels and clean up the details:*

Display the template again but remove the NODE and CLUE labels

## P4 (Execution prompt with similar input from original for testing and verification)

Fill out the template above for a {STORY_TYPE} story involving the player character investigators beginning their investigation of {CRIMINAL} commmitting the crime of {CRIME} at {START_NODE} or {START_PERSON} and finding clues that lead to {NODE1}, {NODE2} and {NODE3}.

STORY_TYPE = modern police investigation

CRIME: a terror plot involving detonating bombs in Los Angeles

CRIMINAL = Ron White, a known terrorist

START_NODE = storage unit

START_PERSON = Jimmy Yu, the storage unit manager

NODE1 = the Ocean View Condominiums on Sunset Boulevard

NODE2 = The Beverly Hilton Hotel

NODE3 = Joe Castanello, a corrupt district attorney

CLUE_TYPE = Any items in this list: a home address, background check, receipt, clothing, phone call records, weapons, weapon parts, witnesses, questioning, microfilm, official records, computer records, trash, rubbish, blood stain, broken window, broken door, broken mirror, broken branches, footprints, psychic residue, body, body part, arcane residue
