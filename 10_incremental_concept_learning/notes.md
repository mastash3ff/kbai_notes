# Incremental Concept Learning

## Preview

Learning by Recording Case
         |
Incremental Concept Learning
    |                  |
Classification   Version Spaces

Case Based Learning stores new examples in memory.
Extract Concepts from Examples stored in Memory

* Purpose of incremental concept learning
* Variabilization
* Specialization
* Generalization
* Heuristics for specialization and generalization

## Quiz identifying A Foo

Background knowledge about previous figures to identify a "foo" is important.

Learning is incremental.  One example at a time.
Examples we get are labeled.  Positive/Negative examples.
Examples can come into a particular order.
Different from case based reasoning.  We stored in raw form.  In this case, extracting concepts from them.
Extracting from the number of examples is small.
When abstracting concepts from examples, what to abstract?  What to learn?  What exactly to generalize is a very hard problem?
A tendency to often overgeneralize or overspecialize becomes a problem.
How does an intelligent agent find out what is the right generalization?

## Incremental Concept Learning

                    Given new example:
              Is this an example of the concept?
           /                                     \
        Yes                                       No
         |                                        |         
Does it fit the current                 Does it fit the current 
definition of the concept?               definition of the concept?
  |                   |                      |            |
 Yes                  No                    Yes           No
  |                   |                      |            |
Do Nothing       Generalize             Specialize     Do nothing

Examples using tree:
* Child has been introduced to a black cat.  Knows all cats to be black.  Sees an orange cat so has to generalize color of cats.
* Child has been introduced to a black cat that has 4 legs and it's furry.  See a dog and it matches traits but it's not a cat so has to specialize.

## Variablization

First example is an Arch made of bricks

           Brick
             |     (supports)
           Brick
(supports) /    \  (supports)
Brick (left-of) ->  Brick


AI knows that bricks support each other.  All objects are bricks.  Some can be in horizontal position of one another.  Builds vertically.

Further examples will learn on positive and negative examples.

## Generalization to Ignore Features

Current Concept of Arch

           Brick
             |     (supports)
           Brick
(supports) /    \  (supports)
Brick (left-of) ->  Brick

Encounter an Arch which is a positive example

           Brick
(supports) /    \  (supports)
Brick (left-of) ->  Brick


New Concept of Arch by Generalization
           Brick
(supports) /    \  (supports)
Brick (left-of) ->  Brick

## Specialization to Require Features

Require-link heuristic is when a current concept encounters a concept that does not fit the current concept.  So, the concept encountered must 'require' the current concept's features.

In other words...
Require-Link Heuristic - if the structure of the representation of the concept and the representation of the negative example have some things in common but there are also some differences.  Revised the current definition in such a way that those things that are not in common MUST be required.

Example:

Current Concept
           Brick
(supports) /    \  (supports)
Brick (left-of) ->  Brick

Encountered Concept
Not an Arch
           Brick
          /     \
Brick (left-of) ->  Brick

New Concept
           Brick
MUST support /    \  MUST supports
Brick (left-of) ->  Brick


## Specialization to Exclude Features

Forbid-link Heuristic is where the current concept run across a negative example and it creates a new concept that "forbids" structures in the negative example by negating relationships.

## Generalization to Abstract Features

Enlarge-set heuristic is where the current concept runs across a positive example and the new concept is "enlarged" by adding new elements to the structure so the new example is added to the new concept.

## Generaliation with Background Knowledge

Climb-tree Heuristic assumes that the AI has background knowledge so that it knows, for example, that a 'brick' is a kind of 'block' using is-a relationships.  If the AI has a current concept such that something is a brick or wedge, it can reduce it to being a block based on the background knowledge.

Background knowledge provides a powerful mechanism for generalizing.  "The more we know, the more we learn."

## An Alternative Visualization

Assume an AI was provided a positive example, and the AI can come up with a concept definition that covers that positive example.  Now suppose the AI has been given a negative example that is covered by the current concept definition.

The current concept definition must be refined in such a way that the negative example is excluded while still including the positive example.  The current concept learns to exclude this negative example from it's current definition.

Likewise, if a new positive example is introduced, the current concept definition must be revised to fit both encountered poositive examples into it's current concept definition.

How do we constrain learning in this complex learning space?  That is where heuristics and background knowledge come in.  Heuristics guide hte algorithm so that it revised the conccept definition in an effecient manner and the background konwledge helps in that process.

## Heuristics for Concept Learning

Review of heuristics encountered so far for specializing and generalizing.

* Require-Link:  link must be present to be a positive example of the concept.

* Enlarge-set: mulitple objects or links may fit one role in the concept

* Forbid-Link: link must be absent to be a positive example of the concept

Climb-Tree: generalize over multiple objects in the same role based on knowledge

* Drop-Link: link is not ncessary to be apositive example of the concept

* Close-interval: expand range of values to be a positive example of the concept.

## Quiz Excersises

Given four bricks, the first step is to variablize the concepts.  We know the concept is a "foo".  So all four bricks are labeled simply as...bricks!

We then write connections for the concepts such as "supports" for the bricks.  Note that we write "supports" instead of "must supports" since we have not encountered an example that these links are required.

The AI will now run across positive and negative examples to refine it's current concept definition.

AI runs across a negative example so it now refines based on the example to show concepts of that the bricks "should not touch each other".

A positive example now such that bricks are now cylinders or bricks in the middle.

Next example, suppose the AI has background knowledge such that it knows a brick or cylinder is a block.  Modify the concept on the right to generalize based on this knowledge.  Uses Climb-Tree heuristic to apply background knowledge.  This particular method of incremental concept ispart of analogous AI class because we are looking at the critical role that knowlede plays in guide the learning process.  What we learn in the end depends on the knowledge we begin with.

Sometimes we don't have to change our concept given a negative example such as when a triangle is on top of our bricks.  So if a current concept already excludes a new negative example, nothing has to be done since the current concept has already learned to exclude it...

## Final Concept of a Foo

The final concept through the excercies is finally defined for a "foo".  Machine learning uses large number of samples to learn concepts.  Small numbers of samples make it hard to apply background knowledge to new examples.

## Assignment:  Incremental Concept

How would you use incremental concept learning to design an agent that could answer RPMs?

* What are the concepts that your trying to learn in this case?
* What are you incrementing over?

This might depend on the scope of the problem.  Are you doing concept learning at the level of hte individual problem or between problems?

What concepts are you learning and how are you tweaking them?

What would a specific concept look like?  What would a general concept look like?  Once you establish these concepts, how would it help you solve new problems?

## Wrap Up

* Purpose of incremental concept learning.

* Variablization

* Speciailization 

* Generalization

* Heuristics for speciailziaiton and generlaization.

Next up is classification where it leverages concepts using what we have develolped through  incremental concept learning.

Incremental concept learning will be revised in future lessons such as version spaces, explanation based learning, and learning by correcting mistakes.

## The Cognitive Connection

Incremental concept learning is intimately connceted with human cognition.

In one view of learning, an intelligent agent is given a large number of examples.  The agent's task is then to detect patterns of regularity in those examples and learn those patterns of regularity.

In the other view, the agent is given one example at a time such that it gradually learns one example at a time.

Humans easily learn by one example at a time rather than many examples at once.