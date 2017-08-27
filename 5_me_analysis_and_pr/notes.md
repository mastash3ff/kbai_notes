# Means-End Analysis and Problem Reduction

## Preview
useful for well-formed problems.

Fundamentals:

              Semantic Networks
              /          \   
              |           |
Generate and Test _      Production Systems
       |           \     
Means-End Analysis  \
                     \
               Problem Reduction

Upcoming discussion topics:

State Spaces
Means-End analysis
Problem Solving with ME analysis
Problem Reduction

## The Block Problem

Move blocks from initial state to hte goal state while obeying these rules:
1. You my only move one block at a time.
2. You may only move blocks that have nothing on top of them.


Initial State      Goal State

                       A
C                      B
A  B                   C

Very famous AI problem in nearly all AI books.

Write a sequence of operators that will move the blocks into the goal state.
Available Operators:

Move(Object, Location)  e.g. Move(C,Table) Moves C onto the Table.  Move(C,B) moves C onto B

**Solution**

1. Move(C,Table)
2. Move(B,C)
3. Move(A,B)

How do we get AI to come up with this solution using ME Analysis?

## State Spaces

Problem solving happens in a state space.
Has an initial State and a Goal State.
Want one path that goes to inital state to goal state.  There may be many paths but we want one.
A sequence of states make up a path.

How does the AI intelligently decide to go from one state to another?

## Differences in State Spaces

Talk in term of differences of current states and Goal States.
Pick an operator that helps reduce the difference between the current state and the goal state.

The reduction between the curent state and the goal state is the END.
The application operator is the MEANS.
Thus, Means-End Analysis.

Application:  Similiar to path finding robotics.

Back to Blocks World Problem...

                      A
C                     B
A  B                  C
_  _  _           _ _ _

A on Table           A on B
B on Table           B on C
C on A               C on Table

delta = 3            delta = 0


Produce 3 possible states from initial state:

                         A
                 C       B
A B C         A  B       C

delta=2       delta=3    delta=2

Choices then become either 1 or 3 by less differences.

Ideal ME Analysis produces a path where each state's difference(delta) is reduced until 0.

## Process of ME Analysis

For each operator that can be applied:
* Apply the operator ot the current state
* Calculate difference betwen new state and goal state

Prefer the state that minimizes distances between new state and goal state

Note:  We used ME method in Blocks World problem and Guards/Prisoners Problem when we threw out states that did not get us closer to goal state.

## Exercices and Problems Faced

Sometimes the next possible states dont reduce the difference.  ME analysis does not always take us closer to the goal b/c we get caught up in a loop.

Like Generate and Test, ME Analysis is a universal AI method.  Few guarantees of success and costly in terms of computational effeciency.  No guaranteed optimal solution.

## Assignment Means-End Analysis

How would you use mean-end analysis to design an agent that could answer Raven's Progressive Matrices?

Goal is to solve the problem

Or transform one frame into another frame.  Then traceback and find out what the transformation was.
How would you measure distance then since it's an important measure for ME analysis since it helps to decide what to do next?

What kind of operators would you define to move to closer to the goal?  How would you weight them to decide to what to do at any time?

## Problem Reduction

Given a hard problem reduce it into simpler subproblems using decomposition.  This is how Problem Reduction(PR) works.

## Problem Reduction in the Block Problem

Curr State   Subgoal     Goal State
                         A
A                        B
B             C          C
C    D        D          D

Problem Reduction does not tell us which subproblem to attack first.

Ignores other states except the ones it is concerned with e.g. C and D from above example.

## Excercies and Problems faced

Problem Reduction is also a universal method like Generate & Test and ME Analaysis.  Faces the same challenges.

## ME Analysis for RPMs

Using ME Analysis on RPMs, we can define an initial state and goal state.  Generate possible next states from transformations to determine deltas to identify which is the best next move, if possible.  Using those transformations previously discovered, transfer it to the new problem set to discover a solution.

Using Problem Reduction on RPMs, we reduce the problem into subgoals.
Three subgoals are shown in the lecture video:
1. Find the transformation between A and B(initial and goal state).  
2. Transfer that transformation to C to find some candidates for D
3. Compare candidate states for D to answer choices provided in problem.

Generate and Test produces solutions to compare against answer choices provided in problem.

Sometimes a combination of methods are used.

Semantic Network's knowledge representation coupled with either Generate and Test, ME analysis, and Problem Reduction have weak coupling and are known as weak methods. We will discover later some knowledge representations that have tight coupling.

## Assignment Problem Reduction

How would you use problem reduction to design an agent that could answer Raven's Progressive Matrices?
Example, how we solve RPMs.  How do you we break it down and combine it as a whole to generate a solution.

How will it recognize to split a problem into subproblems?
How would it combine them as an answer for a whole?

Ask ourself, How does breaking a problem into subproblems help us accomplish our goal of solving the problem as a whole?

## Wrap Up

State Spaces - 
Means-End Analysis - Look at goal and continuously move towards it.
Problem solving with Means-End Analysis 
Problem Reduction - Used with Means-End analysis to help solve a problem faced.

Logic and Planning are good topics to consider next after ME Analysis and Problem Reduction.
Planning provides a more robust way of solving problems faced in ME Analysis

## Cognitive Connection

Weak methods use little knowledge.  Strong methods will demand a lot of knowledge and make use of it but will come up with solutions effeciently.  Though, knowledge is not always readily available.

Humans use a combination of weak and strong methods based on a particular situation given.

