[//]: # (Version 1.0.0, rough, but ready for use).

[//]: # (

Thoughts on the design of this prompt:
  - You may need to refine prompt 1 to suit your needs.  I iterated over this prompt, fine tuning it until it was close.
}

# Generating the Mystery Story

**NOTE: This prompt sequence requires GPT-4! (See below for details)**

## P1 Example of one of my own scenarios:  Voldemort returns via the Soul Jar Spell

*Here is an example backstory I'm working on:*

Imagine you are a mystery roleplaying game scenario author, and you're developing a {STYLE} backstory titled {BACKSTORY_TITLE}. Write a detailed outline of the crime means, crime motive, crime opportunity, and the steps needed to be performed by the criminals to commit the crime in the style of {AUTHOR}. Your focus should be on how {CRIMINAL} plan to {CRIME}. Consider the use of {MEANS_LIST} used by {CRIMINAL}. Consider other details such as {OTHER_DETAILS}. Provide a step-by-step account of the {CRIME_TYPE}, highlighting key challenges, suspenseful moments and describe the final outcome of {FLAW}.

BACKSTORY_TITLE = "The Soul Jar Spell: Resurrecting Voldemort"

CRIMINAL = the Death Eaters

CRIME_TYPE = forbiddien ritual and spell involving dark magic

CRIME = restore Voldemort to power by placing his soul in the body of Barty Crouch Jr (a devoted follower) using the corpse of a giant spider as an egg

MEANS_LIST = forbidden spells, secret passages, arcane elditch knowledge, suicidal commitment 

OTHER_DETAILS = the ritual will be performed in the Chamber of Secrets, using the spider corpse as an egg, and the date of the ritual must be Hogsmeade day so that students and faculty are away from Hogwarts at the village of Hogsmeade.

FLAW = Eric Eldric (a brave student at Hogwarts) enters the Chamber of Secrets and interferes with the Soul Jar Spell causing it to backfire and transforming Voldemort into a horrific giant spider

AUTHOR = H.P. Lovecraft

STYLE = Horror

## P3 Revisions

*Based on the output for my own scenario above, I made the following changes*

Add more details of Voldemort's transformation into a giant spider and describe the battle between Eric Eldric and Voldemort's spider persona.
Change the outcome so that the Death Eaters are forced to serve Voldemort in his new form.
Change the outcome so that Eric Eldric transforms into a lovecraftian creature and battles Voldemort in an epic battle before Voldemort and his followers escape the chamber and go into hiding, leaving the story unresolved to be continued in a later chapter.

*Once I revised with these prompts, I had an extremely solid story.*

# Generating a graph to model the investigation and render the graph diagram.

## P4 Create a graph to model the points of interest and clues in the investigation and how they are connected. 

*Create a directed graph of the clues and points of interest for the investigation.*
   *- For directed graphs, see here: https://en.wikipedia.org/wiki/Directed_graph*
   *- For node based mystery design see here: https://thealexandrian.net/wordpress/7949/roleplaying-games/node-based-scenario-design-part-1-the-plotted-approach*
*We use graphviz to: 1) help ChatGPT understand the structure of the clues and points of interest, and 2) create a visualization of the scenario clues*

*The graph connects each point of interest to a clue that leads to the next point of interest.  All clues should ultimately lead to the end node which is where the final battle/confrontation will occur*

*Start with a simple graph that we will fill in with details later.*

Here is a graphviz code block: 

digraph investigation {
    node [shape=ellipse, style=filled, fillcolor=lightgray];

    "START"  [fillcolor="#ddb9f7", pos="7,9!", xlabel="START"];
    "A"  [fillcolor="#f8ef10", pos="3,6!", xlabel="A" ];
    "C"  [fillcolor="#f8ef10", pos="11,6!", xlabel="C"];
    "END"  [fillcolor="#e54a11", pos="7,3!", xlabel="D"];
    
    "START" -> "A" [label="(Clue StartToA)"];
    "START" -> "C" [label="(Clue StartToC)"];

    "A" -> "END"  [label="(Clue AToEnd)"];
    "C" -> "END"  [label="(Clue CToEnd)"];
}
*NOTE: Add these lines to the above code block if you need a more complex graph:*

```
"B"  [fillcolor="#f8ef10", pos="7,6!", xlabel="B" ];
"START" -> "B" [label="(Clue StartToB)"];
"B" -> "END"  [label="(Clue BToD)"];

```

The graphviz code block is for a directed graph.
The vertices of the graphviz code block are the points of interest in an investigation of a crime. 
The arcs of the graphviz code block are the clues that lead from each point of interest to the connecting point of interest.
The START vertex is the point of interest where the investigators will begin their investigation.  
The END vertex is the point of interest where the investigators will end their investigation.

Display a list of the vertices.
Display a list of the edges.

## P5

*Add labels for the locations, people, etc your PCs will investigate.*

Your next task is to add a label property to each of the vertices in the graphviz code block, using this list of labels: {VERTICES}, like this: '"S"  [fillcolor="#ddb9f7", pos="6,7!", label="Quidditch Match at Hogwarts"]'
The list contains each of the points of interest the investigators will visit during their investigation.
The first item in the list is the START vertex in the graph.
The second item in the list is the A vertex in the graph.
The third item in the list is the C vertex in the graph.
The last item in the list is the END vertex in the graph.
 
VERTICES = [Quidditch Match at Hogwarts, The Black Lake, Dead Spiders in the Forbidden Forest, The Village Of Hogsmeade]

Display the graphviz code block.

*AS NEEDED: Ensure you add an item line above for additional points of interest and then add those points to the VERTICES list*

## P6

*This is the meat of the work to create clues and connect the clues to the points of interest in the graph.*

END_VERTEX = The Village of Hogsmeade

Your next task is to generate clues based on the graphviz directed graph structure.
The vertex labels in the directed graph structure are the points of interest in an investigation of the crime.

The player characters in the role-playing game scenario will visit each of the points of interest looking for clues that will eventually lead them to {END_VERTEX}

Analyze the detailed backstory outline and generate a numerically sequenced list of clues, one clue for each arc in the directed graph structure.
The list of clues should be in text format.
Each clue should describe the current point of interest (as defined by the label property of the tail vertex of the arc) and the the next point of interest (as defined by the label property of the head vertex of the arc) and how the clue connects the two points.

The clues should be written as {STYLE} in the style of {AUTHOR}.

STYLE = Lovecraftian Horror

AUTHOR = H.P. Lovecraft

Ensure that each clue connects the correct points of interest based on the graph structure and it's relationships.

Don't display the graphviz code block.
Please provide the list of clues as text, appending each clue to the corresponding clue label in the graphviz code block.

[//]: # (
  - The prompt above took a lot of finessing. Specifically in how to correlate the clues and points of interests back to the tail vertex, the head vertex and the arc of the graph's structure.  Carefully wording the prompt did the trick.
  - This proves out that most of the time, the problem is in the prompt, not in ChatGPT.
}
    
## P7 More refinement

*Go over each of the clues and replace/refine as needed.*

Generate a new clue replacing clue number X using these details: --NEW CLUE DETAILS HERE--. 

## P8 Optional: Add an escape clue

Add a new vertex and arc to the graphviz codeblock as so:

    "ESCAPE" [fillcolor="#00FF00", pos="3,3.5!"];
    "ESCAPE" -> "END"  [taillabel="(Clue EscapeToEnd)"];

Display the current graphviz code block

For the arc labeled "Clue EscapeToEnd" in the graph, generate a clue that leads to Vertex END that could be placed at any point of interest in the investigation. 
Add this clue to the clue list.
Display the clue list.

## P9 Optional: Add a twist or revelation

### P9.0 Add the TWIST vertex and arc to the graph

Add a new vertex and arc to the graphviz codeblock as so:

  "TWIST"  [fillcolor="#e54a11", pos="7,1!", xlabel="TWIST"];
  "END" -> "TWIST" [label="(EndToTwist)"];

CONFRONTATION=Battle in the Chamber of Secrets

For the TWIST vertex, replace the xlabel property with {CONFRONTATION}.

Display the current graphviz code block

### P9.1 Generate the revelation text that connects the END vertex to the TWIST vertex. 

Generate an obvious and dramatic revelation that propels the investigators from {END_VERTEX} to {CONFRONTATION} using these details: {TWIST_DETAILS}.

TWIST_DETAILS: In The Village of Hogsmeade, the investigators stumble upon a park. In the park is a historical shrine called "The Veil of Redemption", there is a plaque near the shrine that describes the history of the shrine and mentions the shrine's evil counterpart: The Veil of Woe. The Veil of Woe has been associated with dark magic and its mention suggests the possibility of a dark act to be performed soon. Harry Potter recognizes the description of the Veil of Woe as something he had seen in the Chamber of Secrets.

Call the revelation text the "Twist Text".
Display the Twist text 

### P9.2 Reduce the twist text to a terse phrase for the graph to display.

Distill the Twist Text down to a single terse phrase. Call the phase the "Shortened Twist Text".
In the directed graph, replace the label property for the EndToTwist arc with the Shortened Twist Text.

Display the Shortened Twist Text.
Display the current graphviz code block.

## P10 Once you have a complete list of GOOD clues, distill the clues down to small phrases for the diagram (next step)

Using the current list of clues, create a new list of clues called "shortened clues" that reduces the details of each clue to as terse a statement as possible and removing the points of interest from each clue description.

Display the shortned clues.

## P11 Insert the shortened labels into the GraphViz diagram as labels.

In the directed graph, replace the label property value in each arc with the corresponding shortened clue.

## P12 Get the code to generate the diagram.

Display the graphviz code block

*This generated the digraph code and I plugged it into GraphUI (installed in linux). Note: you have to save the graph document to see it rendered*

# Other examples

## P1 Example from the Gringott's Heist in Book 7 of Harry Potter

Imagine you are a mystery roleplaying game scenario author, and you're developing a {STYLE} backstory titled {BACKSTORY_TITLE}. Write a detailed outline of the crime means, crime motive, crime opportunity, and the steps needed to be performed by the criminals to commit the crime in the style of {AUTHOR}. Your focus should be on how {CRIMINAL} plan to {CRIME}. Consider the use of {MEANS_LIST} used by {CRIMINAL}. Consider other details such as {OTHER_DETAILS}. Provide a step-by-step account of the {CRIME_TYPE}, highlighting key challenges, suspenseful moments and describe the final outcome of {FLAW}.

BACKSTORY_TITLE = "The Gringott's Heist"

CRIMINAL = Harry Potter, Hermione Grainger and Ron Weasley

CRIME_TYPE = heist

CRIME = steal a horcrux that belongs to Voldemort and is stored in a magically secured vault at Gringott's Bank

MEANS_LIST = disguises, magical items, and the involvement of a goblin accomplice named Griphook

OTHER_DETAILS = harry uses his invsibility cloak to enter gringott's vaults, Hermione disguises herself at Bellatrix Lestrange

FLAW = there are countless duplicate cups in the vault making it difficult to find the correct cup, and there is a dragon in the tunnels below gringotts guarding the vaults.

AUTHOR = J.K. Rowling

STYLE = Harry Potter type

