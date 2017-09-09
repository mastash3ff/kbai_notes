# Production Systems

## Preview

First time talking about learning.
Production systems are kind of a cognitive architecture, in which knowledge is represented in the form of rules.
Last topic under the fundamental topics of the course:  Semantic Networks, Generate and Test, Production Systems, Means-End Analysis, and Problem Reduction

Will talk about cognitive architecture, in general, and focus on production systems then talk about a mechanism of learning called chunking

## Exercise: A Pitcher

How might intelligent agents make complex decisions about the world?
Given that David has a lot of knowledge about baseball, he can use that knowledge to make a decision.
How is her using his knowledge to make a decision?  What is the architecture?  What is the reasoning that leads him to make that specific decision?

## Function of a Cognitive Architecture

Percepts -> Action.  Maps a particular history into an action.  What should we do next?

## Levels of Cognitive Architectures

Task / Knowledge Level (e.g. selecting a pitch, playing baseball)

Algorithm / Symbol Level (e.g. means-ends analysis, semantic networks)

Hardware / Implmentation Level (e.g. a brain, a transistor)

David Mark talked about 3 levels which he called computational theory. the level of algorithms and the level of implementation.

The three levels are transitive for architectures:  Hardware/Impl Level is an architecture for Algorithm/Symbol Level.  Algorith/Symbol Level is an architecture for Task/Knowledge Level.

In reverse, the three levels are content for another:  Task/Knowledge Level is content for Algorithm/Symbol Level.  Algorithm/Symbol Level is content for Hardware/Impl Level.

Semantic network is represented by Knowledge Level.  What is the content of the knowledge in order to do a particular task.

Want to build theories at all three of these different levels of abstractions.

Most of AI work is done at the top two levels.

## What are the layers of Watson?

Physical Computer(Hardware layer), Searching & Decision-Making(Algorithm Layer), and answering the inputted clue(Knowledge Layer).

## Assumptions of Cognitive Architectures

* Goal-oriented
* Rich,complex environment
* Significant knowledge
* Symbols and abstractions
* Flexible and function of the environment

## Architecture + Content = Behavior

Function for cognitive architectures:  Percepts -> Action

Similiar to computer architecture, stored memory is operated on to get an action.

What is a good architecture?

## A Cognitive Architecture for Production Systems

Deliberation:  Reasoning <-> Learning <-> Memory

SOAR:  Procedural Semantic Episodic
             \       |      /
             Working Memory

SOAR has been worked on for the last 30 years by Neville, Lear and Rosenbloom.

Episodic knowledge has to do with events.
Semantic knowledge has to do with generalizations in the forms of concepts and models of the world.
Procedural has to do with how to do certain things.

## Return to the Pitcher

How do baseball Percepts get mapped into action?
Pitcher has certain knowledge.  Can perceive from the world.  For example, can perceive the bases, batter, current state of game, specific batter, positions of own team mates.  Picture has goals.

## Action Selection

State 0.  Feature1 : value1.  Piicture wants to get to goal state.  Path from current state to goal state.  Illustrated in abstract state space.

## Putting Content in the Architecture

Inning : 7th
portion : top
runners : 2nd and 3rd
outs : 2
batter : prado
average : .256
bats: right-handed
score: 3-2
goal: escape inning (don't let batter hit the ball)

## Bringing in Memory

Using the previous knowledge, present production rules.

i.e. If goal is to Escape, I perceive 2 outs, I perceive a runner on 2nd and I perceive no runner on 1st. THEN suggest goal intenionlaly walk batter (Intentional Walk)

another example, If goal is Intentional Walk THEN suggest intentional-walk operator

Capturing these rules in SOAR's long term memory.

Knowledge is very detailed in these examples.

## Chunking

A technique used to dismiss an operator to use when there is a conflict between multiple operator choices.

## Assignment

How would a production system be used to design an agent that can solve RPMS?
* Address incoming problems.  Knows what to look for in a new problem and it knows how to reply when it finds those things.

OR

* Production rules that are specific to a given problem.  When the agent receives a new problem, it induces some production rules that govern the transformation between certain figures and then transfers that to other rows and columns.  Learns from the problem it receives.

How is the learning going to take place?
How is it actually going to write these production rules, based on a new problem?
What do we get out of actually having these production rules, that are written based on individual problems?

## Wrap Up

Cognitive Architecture.

Fundamental units of learning.

SOAR framework implements production systems.

Production systems enable action selection.

Map percepts -> action.

When a production hits an impass, it can use chunking to learn a new rule to overcome the impass.

## Cognitive Connection

Working memory correlates to short-term memory in humans.

Similiary between SOAR and human behavior when faced with problems of arithmetic algebra.

AI can be good in closed world problems but cannot perform as well as humans in open world problems.

How can human knowledge be captured at large so that it can be used for problems in the open?

