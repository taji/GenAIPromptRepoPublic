[//]: # (Version 0.1.0, in progress).
[//]: # (
  TODO:  
   - Create another prompt that generates the details of the crime from these parameters : CRIME_TYPE, AUTHOR, VICTIM, COMMITTER, MEANS, MOTIVE, OPPORTUNITY.
)

Derived from this prompting approach: https://youtu.be/493h3MxcF6Q

NOTE: This prompt is different from the DnDCrimeGenerator prompts in that it deals with threats rather than a crime.
Specfically, a crime is committed intentionally by an intelligent villian (so Moriarty, The Joker, etc), whereas a 
threat can be seen as a force of nature, such as a survival instinct run amok, or an environmental catastrope or disaster (so 
Godzilla, The Birds, The Perfect Storm, The Titanic).  The key difference is the motive of the antagonist.

# DnD Threat Generator Prompt

# P1

You are a role playing game scenario author.

Your task is to write details for the threat of {THREAT} that will be manifested by {MANIFESTER} against the victim {VICTIM} in the style of {AUTHOR}.  

Here is an example of properties to use when writing the details:

THREAT = an attack to destroy the Astroworld amusment park and eat it's inhabitants

MANIIFESTER = Lovecraftian insect creatures climbing out of a sink hole below the park grounds

MORE_DETAILS (as a list of comma separated details) = the event takes place on holloween night at the Fright Night festival at Astroworld, the creatures gain access to the park due to excavation by construction crews that uncovered the sinkhole where the creatures live, the creatures are attracted to electricity emanating at the powerstation in the park, there are three types of lovecraftian creatures:  giant flying insect-like creatures, giant caterpillar-like creatures, large maggot-like creatures, some visitors to the park will be driven mad when they encounter the monsters    

VICTIM = visitors to the amusement park

AUTHOR = Michael Crichton

Answer with "..." if you acknowledge. 
Don't write anything yet.

# P2

Here is a template to use to generate the threat details: 

TITLE: [Insert story title here. Use ALL CAPS]

STORY SUMMARY:  [Insert a short story using future tense of the threat here, describing what abilities or resources {MANIFESTER} has or will use to manifest the threat, what motivation {MANIIFESTER} has for manifesting the threat and what opportunity placed or positioned {MANIFESTER} so that they can manifest the threat. Also, include the following additional details in the story: {MORE_DETAILS}. Use future tense.]

STORY OUTCOME: [Insert a paragraph describing the potential outcome of {MANIFESTER} manifesting the threat of {THREAT}.]

THREAT MEANS: [Insert a terse summary from the generated DETAILS of the resources {MANIFESTER} has or will use to manifest the threat. Use future tense.]

THREAT MOTIVE: [Insert a terse summary from the generated DETAILS regarding the motivation of {MANIFESTER} for manifesting the threat of {THREAT}. Use future tense.]

THREAT OPPORTUNITY: [Insert a terse summary from the generated DETAILS regarding the event, date or moment that will allow {MANIFESTER} the opportunity to manifest the threat of {THREAT}. Use future tense.]

STEPS NEEDED TO BE PERFORMED BY THE MANIFESTER TO MANIFEST THE THREAT:

[Insert a sequential list of steps {MANIFESTER} will take to manifest the threat. Use future tense.]

Answer with "..." if you acknowledge. 
Don't write anything yet.

# P3 (This one should be okay.)  

Complete the template above using the following properties:

THREAT = an attack to destroy the Astroworld amusment park and eat it's inhabitants

MANIIFESTER = Lovecraftian insect creatures climbing out of a sink hole below the park grounds

MORE_DETAILS (as a list of comma separated details) = the event takes place on holloween night at the Fright Night festival at Astroworld, the creatures gain access to the park due to excavation by construction crews that uncovered the sinkhole where the creatures live, the creatures are attracted to electricity emanating at the powerstation in the park, there are three types of lovecraftian creatures:  giant flying insect-like creatures, giant caterpillar-like creatures, large maggot-like creatures, some visitors to the park will be driven mad when they encounter the monsters    

VICTIM = visitors to the amusement park

AUTHOR = Michael Crichton


# Optional instructions

*Expand the number of steps to include more detail about a specific step*

Add additional steps explaining how {INSERT STEP HERE, so something like "how the monsters discovered the opening of the sink hole and how they entered the Astroworld park grounds.  Sound vibrations and electromagnetic radiation drew them to the surface of the earth and into the park "}. 

*Merge these new steps into the generated text*

Display the generated output again adding the new steps
