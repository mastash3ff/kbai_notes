# Common Sense Reasoning

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

## Resolving Ambiguity in Preopositions

## Ambiguity in Verbs

## Resolving Ambiguity Verbs

## The Earthquake sentences

## Assignment - Understanding

## Wrap Up

## Cognitive Connection