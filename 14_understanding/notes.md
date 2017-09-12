# Understanding

## Preview

Frames -> Understanding -> Common Sense Reasoning -> Scripts

* Thematic role systems - A more structured type of frame representation.
* Ambiguity - Discuss how thematic roles can be used to solve ambiguity.
* Constraints - how grammar and constrains can be used to guide our interpretation of the world.

## Earthquake Report

First story talks about earth quakes.
Second story talks about a president that kills proposals.
Both deal with killing but completely different meanings.

Two different frames.  No simple way to disambiguate between the two previously w/ frames.

We'll examine how to construct a different interpretation of the fist story or 2nd story based on the interpretation of hte word killing in both stories.

To simplify and illustrate thje point.  Focus on one sentence from each story.

Sentence 1:  A serious earthquake killed 25 people in Lower Slabovia.
Sentence 2:  The President of Lower Slabovia killed 25 proposals for earthquake prediction.

An AI program will have to use a lot of background knowledge in order to disambiguate between both sentences and generate hypotheses about how humans might be using that background knowledge to similiarly disambiguate between different senses of the word killed.

## Thematic Role Systems

Example sentence:  Ashok made pancakes for David with a griddle.

Can do different kinds of analysis on this sentence such as lexical analysis which will categorize each of these words into different lexical categories.  For example, "Ashok" is a noun, "made" is a verb, "pancakes" is a noun, etc.

Can do synatical analysis.  Structure of this particular sentence.  "Ashok" is a noun phrase.  "Made pancakes for David with a griddle" is a verb phrase.  This particular verb phrase itself has subphrases in it.

Could do semantic analysis on this and say that Ashok was the agent.  Made was the action.  Pancakes was the object that got made.  David was the beneficiary.  Griddle was the instrument.

Semantic Analysis is at the forefront utilizing Lexical Analysis and synatical analysis.

Ashok made pancakes for David with a griddle.
Ashok - agent
made - verb
pancakes - thematic object
David - beneficiary
griddle - instrument.

A frame representing this sentence would look like

Thematic Role
  verb: make
  agent: Ashok
  beneficiary: David
  thematic object: pancakes
  instrument : griddle

Frame represents the "meaning of meaning."  This is what the agent underdstands when it udnerstands the meaning of this sentence.  This could also be what we understand when we understand the meaning of this sentence.

Q. How do we know that you understood the meaning of this sentence?
A. Questions can be asked and the right kind of inferences can be drawn from it.

Example:  who ate the pancakes?
We might say David ate the pancakes b/c Ashok made them for him.

Information about who ate the pancakes was not present in this particular sentence.  We drew an inference.

Similiar to "Ashok ate a frog" example
We asked questions such as, was Ashok happy at the end?
Frame had default values such as happy.

In short, we do not understand the meaning if we can't draw inferences from sentences or can only draw the wrong inferences.

The frame representation of the meaning of this particular sentence allows you to draw the right inferences.

Example of a thematic-role frame:  "throw"

If we know that a throw action ahs taken place, a few things can be expected.  Someone doing the throwing.  Expect a target specific by the word 'at' or a destination specified by the word 'to'

In no way was there reference to a specific instance of throwing, we are still able to generate expectations with the general action of "throw."

A thematic case frame is able to generate expecations

## Exercise: Thematic Role Systems

"David went ot the meeting with Ashok by car."

Thematic Role Frame:
  verb: go
  agent: David
  coagent:Ashok
  destination:meeting
  conveyance:car

Start with the verb "went."  Notice it's past tense of the action "go."

How did we know David was the agent?  How did we know that the destination was the meeting? etc.

## Constraints

We know that car was a conveyance because of the role that this preposition, "by", plays here.  An intelligence agent might make use of the structure of the sentence ot make sense of the story.

Human language has been design with structure in mind.  For example prepositions:

*Prepositional Constraints*
---------------------------
Preposition | Thematic Roles
by          | agent, conveyance, location 
for         | beneficiary, duration
from        | source
to          | destination
with        | coagent, instrument

Whatever comes after the word "by" can be an 'agent', 'conveyance', 'location'.

The categories we are using here, 'agent', 'conveyance', and 'location', are semantic categories.  We are not saying noun,verb, etc.  These words are semantic categories that let us draw inferences.

How do we know that car was a conveyance and not an agent or location?

In general, while the structure of hte language does provide constraints, these constraints do not always definately determine the meaning of that particular word.  We need to use additional knowledge to figure out teh exact meaning of "car".

## Resolving Ambiguity in Prepositions

Look at three different examples in which "by" points to

1. That was written by Ashok - by points to an agent
2. David went to New York by train. - by points to a conveyance
3. David stood by the statue. - by points to a location

"By" contstrained itself in that it was either agent, conveyance, or location.  It doesn't by itself tell us whether Ashok is either of the categories.  Need additional knowledge.

Assume agent has an ontology of the world.  Term ontology initially comes from philosphy where it means the nature of reality.

AI determine ontology often reference to the conceptualization of the world.  The categories and terms of which I specify the world.  These categories become the vocabulry of the knowledge representation.

Example 1: An ontology tree helps us decide that "by Ashok" is an agent.  Ashok is people which is thus an agent from our ontology tree.

Example 2: Examining "by train", train can be a agent, conveyance, or location.  In the ontology tree, a train is a conveyance so now we know train is a conveyance.

Bottom-Up Processing when initially looking at "David went to New York by Train."  David is a noun, went was a verb.  But then we shifted to top-down processing.  Example, we already have this background knowledg and this background knowledge tells us in a top-down manner that "by here" can refer to an agent, a conveyance, or location.  We also have additional background knowledge represented in an ontology tree that tells us that in this particular sentence the train describes frame to a conveyance.

In short, low-level bottom up processing generates queues which access probes into memory.  Memory returns knowledge represented in an ontology tree and the process then becomes top-down.  Top-down tells us how to interpret the various words in the sentence and how to make sense of the story.

## Ambiguity in Verbs

Ambiguity happens in verbs as well as propositions.

Example:  I was wondering why the ball was getting bigger then it hit me.

Hit conveys two different interpretations:  occured or physically striked me.

"Can't explain puns to kleptomaniacs because they always take things literally."

Puns often come from words that have two different roles in a sentence at once and the sentence still makes sense.

Going forward we are only looking for one particular meaning but we could build an agent with a bit of humor.  When one sentence can be made that can fill multiple grammatical simultanously.

## Resolving Ambiguity Verbs

"Take" has 12 different meanings.  How do we know which definition refers to the meaning of "take" in a particular sentence?

Each of the 12 interpretations of "take" can be be represented in frames.  Each frame specifies themantic roles in that particular meaning of take.

Examples:

Take1
  agent:
  object:

Take4:
  agent:
  medicine:

Take10:
  agent:
  coagent:
  destination:

How would an agent know which "take" meaning belongs to the sentence, "I took the candyh from the baby" among the 12?

Although we started with bottom-up processing, we will shift to top-down-processing.  Inside semantic knowledge about "candy" will eliminate several choices.  Can also eliminate choices from other constraints such as the background knowledge of the preposition "from".  "From" references a source so we eliniate all choices that don't have 'source.'  This leaves one frame choice which interprets "take" as "to steal"

## Exercise Resolving Ambiguity in Verbs

Do all languages have enough similiar structure?  Could we then translate sentences from one languaage to another language?

## The Earthquake sentences

Back to disabmiguating the earth quake example with the word "kill"

Kill has two meanings we can represent in a frame:

1. to cause the death of
2. to put an end to

Kill1
  agent:
  victim:

Kill2:
  agent:
  object:

1st sentence refers to Kill1 while 2nd sentence refers to Kill2.

There are limitations in this theory of representing meanings in frames.  Back to example of "I took the candyh from the baby."

One limitation is that when we have a large number of rules to determine the meaning of "take" by making senbse of hte word "candy" and making sense of the word "from"

When we look at increasingly large number of forms of the sentence, the number of rules we need starts exploding.  Different variations of the sentence involves different interpretations of "take."

=
(NOT FROM LECTURE but my observation) *"took" can refer to the frame representing "to steal" or it can refer to the frame "to cheat or swindle".  Both interpretations make sense on the frames provided.

## Assignment - Understanding

How would you use configuration to design an agent that could answer RPMs?

How would you use the notion of understanding the notion of thematical frames, constraint, and ambiguity to address RPMs?

* The idea of multiple possible transformations in earlier problems.  Certain problems could be solved with either rotation or reflection but they would give different answers.

* Might imagine a frame that dictates certain expected values for different transformations and degree of fit to those expectations can dictate the accuracy of that particular answer.

Think about the different phases of the understanding process.

How do you first understand what's happening in the problem?
How do you fit that into a thematically role frame representation?
How would that represetntaiton then help you transfer and solve the problem?

## Wrap Up

* Thematic Role Systems - a more formal type of frame represetnation that capture verbs and tell us what to expect in certain events.
* Resolving ambiguity - single verbs can actually have ambiguous meanings but thematic role frames can help us differentiate which meaning a verb has in a particular sentence
* Leveraging constraints - Certain words or frames can constrain the possible meanings of a sentence and help us figure out those ambiguus meanings.

Understanding is used by agents to understand stories and events happening in the world around them.

We have discussed how single words or phrases can have multiple possible meanings but next time it will be done in phrase.  In reverse we will later discuss how multiple phrases or multiple senseces can actually have the same meaning.  How can we discern that sameness the nreact accordingly.

## Cognitive Connection

We have mostly focused on natural language understanding but that is just one instance of understanding.

Understanding is about making sense of the world.

THe world bombards us with data that comes in acoustic, visual, verbal, numerical.

3 sources of power:
1. Exploit constraints in the world.  The world behaves in certain ways whether its the social world, the gramitcal world, or physical world.
2.  We have structured knowledge representations.  Representations in memory capture not just knowledge and its representations but the organization of that knowledge.
3.  Low level problem bottom up processing helps us activate this knowledge structures from memory.  Once generated, the structures generate expectations that make the processing top-down.