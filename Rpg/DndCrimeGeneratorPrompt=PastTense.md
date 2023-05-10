[//]: # (Version 0.1.0, in progress).
[//]: # (
  TODO:  
   - Create another prompt that generates the details of the crime from these parameters : CRIME_TYPE, AUTHOR, VICTIM, COMMITTER, MEANS, MOTIVE, OPPORTUNITY.
)

From here: https://youtu.be/493h3MxcF6Q

# DnD Crime Generator Prompt

# P1

You are a role playing game scenario author.
Your task is to write details for the crime of {CRIME} committed by {COMMITTER} against the victim {VICTIM} in the style of {AUTHOR}. 

CRIME = planning and executing a heist to steal a horcrux from a magically secured vault at Gringott's Bank
COMMITTER = The young wizards Harry Potter, Hermione Grainger and Ron Weasley
MORE_DETAILS = a goblin accomplice named Griphook, polyjuice potion, invisibility cloak
VICTIM = Voldemort, the owner of the vault at Gringott's Bank.
AUTHOR = J.K. Rowling

Answer with "..." if you acknowledge. 
Don't write anything yet.

# P2

Here is a template to use to generate the the crime details: 

TITLE: [Insert story title here. Use ALL CAPS]

DETAILS:  [Insert a short story of the crime here, describing what resources {COMMITTER} had or used to commit the crime, what motivation {COMMITTER} had for committing the crime and what opportunity placed or positioned {COMMITTER} so that they could commmit the crime. Also, include the following additional details in the story: {MORE_DETAILS}]

OUTCOME: [Insert a paragraph describing the outcome of {COMMITTER} committing the crime of {CRIME}.

MEANS: [Insert a terse summary from the generated DETAILS of the resources {COMMITTER} had or used to commit the crime]

MOTIVE: [Insert a terse summary from the generated DETAILS regarding the motivation of {COMMITTER} for committing the crime of {CRIME} ]

OPPORTUNITY: [Insert a terse summary from the generated DETAILS regarding the opportunity {COMMITTER} used to commit the crime of {CRIME} ]

STEPS: [Insert a sequential list of steps {COMMITTER} took to commit the crime]

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
MORE_DETAILS = a goblin accomplice named Griphook, polyjuice potion, invisibility cloak
VICTIM = Voldemort, the owner of the vault at Gringott's Bank.
AUTHOR = J.K. Rowling

# P3.1 (Here is one I am working on)  

Complete the template above using the following properties:

CRIME = Restore Voldemort to power by storing his soul inside a young boy's body, using a spell called "The Soul Jar" 
COMMITTER = The Death Eaters
MORE_DETAILS = a young wizard named Rupert Ham who is hypnotized by the Death Eaters, a professor named Aldus Norwitch, a intellect devourer
VICTIM = The Wizarding World, which will fall under tyranny if Voldemort rises to power.
AUTHOR = J.K. Rowling

# Optiona instruction

The template has instructions to follow (enclosed in square brackets) to generate details for each element in the template.  The instructions should be replaced with the details.

