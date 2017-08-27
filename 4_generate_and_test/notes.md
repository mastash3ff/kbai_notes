# Generate and Test

## Preview
Generate and test is a solving method
Generate and test method
Smart generators
Smart testers
Generate and test for Raven's Progressive Matrices(RPM)

## Guards and Prisoners

KBAI are a collection of 3 things: knowledge representations, problem solving techinques, and architectures.
Knowledge representation is a semantic network
Problem solving method using Guards & Prisoners.

## Dumb Generators, Dumb Testers

Generate all possible states without discrimination(Dumb Generator)
Has a tester and looks at all states.  ONLY removes some of them that are illegal to problem specification (Dumb Tester).

## Smart Testers

Smart Tester does the following:
Looks at beginning state and looks for that same state and eliminates it.
Prisoners outnumber guards.  Eliminates that state.
If a state has no successor state, it elminates it.
If states are identical, merge them.

Semantic network was useful for knowledge representation but alone not useful for solving.

## Smart Generators

Smart Generator does the following:
Examines if states going forward do not match from history to determine whether the state should be generated.
Determines if a state is illegal and does not generate it.

## Discussion
A balance must be struck between Smart Generators and Smart Testers

## Generate and Test for Raven's Problems

The Prisoner/Guard problem was discrete transformation going from one state to another. Only a certain number of guards/prisoners could be transferred to the other side.  RPMs unlike Prisoner/Guard problem, there is a space of possibilities that are very large.

For Raven Problems, a smart generator and smart tester are CRITICAL.  The number of possibilities are overwhelming without them.

## Semantic Networks for Generate and Test

For the previous issue, semantic networks help with abstraction to where the problem gets represented and analyzed.  Semantic does not care about the fine details of what happened but the high-level abstraction of what did happen.  This abstraction helps us ignore the low-level details therefore the solving method problem does have to worry about them.

## Generate and Test for RPM's

Represent the problem in a semantic network.
David's problem solving methodology:  use the transformation between a and b, transfer that transformation to c.  Use it to generate an answer for d.  look at all possible answers for close matching.  To make the tester and generator even smarter, I would have it meet the generated answer with a certain level of confidence.  And if it doesn't meet that, look back for a different transformation we could have transferred.

Another solution would be to take each answer one by one and match it to C to generate the transformation form C to D.  Then test it against the transformation from A -> B.  Iterate for all 6 choices.  Determine which one is closest aftler all answer choices have been analyzed to figure out which is the single best answer.

## Assignment
How would you use the generate and test method to design an agent that could answer RPMs?

For example, generate multiple answers and testing them against the answer options
OR
Generate one answer and test it intelligently against the different options available.

How do you know which shape in one frame maps up to a different shape in another frame?
How would I then use that information to generate what you think the answer is?

Keep in mind of 3x3 problems where there are more transformation and more figures going on, the problem space can be huge and it can be difficult to figure out what to generate.
Think about how I'm actually going to infer the mapping between different figures in the problem.
How do you know which shape in one frame maps up to a different shape in another frame.
How would I then use that information to generate what you think the answer is.

## Recap

Generate and Test
Smart Testers and Smart Generators - Makes the problem solving easier and more effecient.
Generate and test in an unconstrained domain

Next is up two solving problems that build up on generate and test.  Means-end analysis and problem reduction.

## Cognitive Connection

Humans use generate and test all the time.  We do not have complete or correct knowledge of the world.  We do not have infinite computuation resources.  We do not always have recourse to a method of reasoning that is guaranteed to be correct.  When we don't have these things, we use our own test method.  We come up with particular solutions to a problem and test the solution out.

Genetic algorithms are inspired by the process of biological evolution.  Like crossover and mutation, one can generate solutions that can then be tested against some fitness function. 
