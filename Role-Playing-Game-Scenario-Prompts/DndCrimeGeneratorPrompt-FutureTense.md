[//]: # (Version 0.1.0, in progress).
[//]: # (
  TODO:  
   - Create another prompt that generates the details of the crime from these parameters : CRIME_TYPE, AUTHOR, VICTIM, COMMITTER, MEANS, MOTIVE, OPPORTUNITY.
)

From here: https://youtu.be/493h3MxcF6Q

# DnD Crime Generator Prompt

# P1

You are a role playing game scenario author.
Your task is to write details for the crime of {CRIME} that will be committed by {COMMITTER} against the victim {VICTIM} in the style of {AUTHOR}.  Here is an example of properties to use when writing the details:

CRIME = planning and executing a heist to steal a horcrux from a magically secured vault at Gringott's Bank
COMMITTER = The young wizards Harry Potter, Hermione Grainger and Ron Weasley
MORE_DETAILS (as a list of comma separated details) = a goblin accomplice named Griphook, polyjuice potion, invisibility cloak
VICTIM = Voldemort, the owner of the vault at Gringott's Bank.
AUTHOR = J.K. Rowling

Answer with "..." if you acknowledge. 
Don't write anything yet.

# P2

Here is a template to use to generate the crime details: 

TITLE: [Insert story title here. Use ALL CAPS]

STORY SUMMARY:  [Insert a short story using future tense of the crime here, describing what resources {COMMITTER} has or will use to commit the crime, what motivation {COMMITTER} has for committing the crime and what opportunity placed or positioned {COMMITTER} so that they can commmit the crime. Also, include the following additional details in the story: {MORE_DETAILS}. Use future tense.]

STORY OUTCOME: [Insert a paragraph describing the potential outcome of {COMMITTER} committing the crime of {CRIME}.]

CRIME MEANS: [Insert a terse summary from the generated DETAILS of the resources {COMMITTER} has or will use to commit the crime. Use future tense.]

CRIME MOTIVE: [Insert a terse summary from the generated DETAILS regarding the motivation of {COMMITTER} for committing the crime of {CRIME}. Use future tense.]

CRIME OPPORTUNITY: [Insert a terse summary from the generated DETAILS regarding the event, date or moment that will allow {COMMITTER} the opportunity to commit the crime of {CRIME}. Use future tense.]

STEPS NEEDED TO BE PERFORMED BY THE CRIMINALS TO COMMIT THE CRIME:

[Insert a sequential list of steps {COMMITTER} will take to commit the crime. Use future tense.]

Answer with "..." if you acknowledge. 
Don't write anything yet.

# P3.0 (This one will cause ChatGPT to refuse to generate as it violates policy)

Complete the template above using the following properties:

CRIME = planning and executig a terrorist bombing of the Bellagio hotel in Las Vegas
COMMITTER = Yassif Manssor, a known terrorist and his terrorist minions
VICTIM = the Bellagio Hotel and any people in the hotel or nearby
AUTHOR = Lee Child

# P3.1 (This one should be okay.)  

Complete the template above using the following properties:

CRIME = planning and executing a heist to steal a horcrux from a magically secured vault at Gringott's Bank
COMMITTER = The young wizards Harry Potter, Hermione Grainger and Ron Weasley
MORE_DETAILS (as a list of comma separated details) = a goblin accomplice named Griphook, polyjuice potion, invisibility cloak
VICTIM = Voldemort, the owner of the vault at Gringott's Bank.
AUTHOR = J.K. Rowling

# P3.1 (Here is one I am working on)  

Complete the template above using the following properties:

CRIME = Restore Voldemort to power by storing his soul inside a young boy's body, using a spell called "The Soul Jar" 
COMMITTER = The Death Eaters
MORE_DETAILS (as a list of comma separated details) = a young wizard named Rupert Ham who is hypnotized by the Death Eaters, a professor named Aldus Norwitch, an intellect devourer, a final ritual and spell to perform which will place Voldemort's soul inside the child's body
VICTIM = The Wizarding World, which will fall under tyranny if Voldemort rises to power.
AUTHOR = H.P. Lovecraft

# P3.2 Here is another one: "Threxulon's Betrayal"

Complete the template above using the following properties:

CRIME = Uncover the location of Voldemort's horcruxes, retreive the horcruxes and use them to force Voldemort to serve the mind flayer Threxulon.  Threxulon will threaten Voldemort with death by destroying the horcruxes unless Voldemort serves him. 
COMMITTER = Threxulon, a mind flayer
MORE_DETAILS (as a list of comma separated details) = two of Voldemorts lieutenants (Peter Pettigrew and Bellatrix Lestrange) are enthralled to Threxulon and are secretly serving Threxulon to betray Voldemort,  Threxulon cannot speak.  Instead he speaks through two children who are enthralled to him: Rupert Ham and Abigail Laundryman, Threxulon also has an enthralled servant  who teaches at Hogwarts and who has uncovered the secret of the horcruxes by spying on Albus Dumbledore
VICTIM = Voldemort who will be be forced to serve Threxulon.  
AUTHOR = H.P. Lovecraft

# P3.3 And another one: "Threxulon Invades Hogwarts Plot"

Complete the template above using the following properties:

CRIME = Enslave the professors at Hogwarts
COMMITTER = Threxulon a mind flayer
MORE_DETAILS (as a list of comma separated details) = infiltrate the Hogwarts school grounds through underground tunnels or secret passages, use cranium rats to project feelings of paranoia on the facluty and to sow mistrust, use Death Eater lieutenants to kidnap any professors that are able to resist enslavement, retrieve vials that  contain memories from the crypts of dead wizards to use in a pensieve to unlock dark magic
VICTIM = Albus Dumbledore and Hogwarts School
AUTHOR = H.P. Lovecraft

# P3.3 And another one: "Threxulon's Waking Doom"

Complete the template above using the following properties:

GOAL 2: The Mind Flayer Threxulon seeks to unlock the arcane secrets hidden beneath the black lake, using the combined powers of his sorcerer lieutenants and the psychic network of his cranium rat minions to locate and extract the mysterious artifact called the WAKING DOOM, in order to dominate the world of magic and enslave it's inhabitants.

CRIME = Use a mysterious artifact called the Waking Doom to overthrow the ministry and enslave the world
COMMITTER = Threxulon a mind flayer
MORE_DETAILS (as a list of comma separated details) = the Waking doom artifact is in a hidden temple beneath the black lake, unknown to Threxulon the artifact will awaken the deep one Chtulhu and end up destroying the universe, cranium rats and death eaters will assist Threxulon in finding the artifact
VICTIM = All of mankind and existence itself
AUTHOR = H.P. Lovecraft


# Optiona instructions

*Expand the number of steps to include more detail about a specific step*

Add additional steps explaining how {INSERT STEP HERE, so something like "how the Death Eaters discovered the Soul Jar Spell.  It was provided by a mind flayer named Threxulon"}. 

*Merge these new steps into the generated text*

Display the generated output again adding the new steps

