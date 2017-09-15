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

## Specialization to Exclude Features