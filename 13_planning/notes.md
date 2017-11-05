# Planning

## Preview

An intelligent agent maps perceptual histories into actions.  Planning is a power method for action selection.

Logic -> Planning

Lesson Preview:

States, goals, and operators
Conflicts in planning
Partial-order Planning
Hierarchical Task Networks

## Block Problem Revisited

Remember that the block world problem moves a block in it’s current state to progress towards it’s end goal state.  Only one block at a time.  Can’t move a block that has a block on top of it.

A weak method was used earlier such as Means-End Analysis.  The question was presented, “how do we find which goal to select among the various goals presented?”  We assumed the agent might select a goal.

Now we look at how the agent can do goal composition and pick the correct goal to pursue.

## Painting a Ceiling

Assume a robot is needed to paint the ceiling and the ladder.

Goals:  The ceiling is painted and the ladder is painted.

These goals are in conflict b/c if the robot paints the ladder first, then the ladder will become wet and the robot cannot climb on it to paint the ceiling.  The robot must paint the ceiling first before the ladder.

Propositional Logic Form:
Painted(Ceiling)

## Exercise: Goals

Goal State in Propositional Logic Form:
Painted(Ceiling)
Painted(Ladder)

Goal State in Conjunctive Normal Form:
Painted(Ceiling) & Painted(Ladder)

## States

Initial State:
On(Robot, Floor) & Dry(Ladder) & Dry(Ceiling)

Goal State:
Painted(Ceiling) & Painted(Ladder)

How can a robot come up with a plan with this information?

## Exercise: States

How would we represent a state where the robot is on the ladder and the ceiling is painted?

Given Initial State:
On(Robot, Floor) & Dry(Ladder) & Dry(Ceiling)

State: 
Painted(Ceiling) & on (Robot, Ladder)

Note, there is no operators between states.

## Operators

Operator: Climb ladder

In propositional logic,
Climb-ladder:
  Precondition:
    on(robot,floor) & dry(ladder)
  Postcondition: On(Robot, Ladder)

In the precondition, there are not any negative literals.  All the literals in the precondition are positive.  Postconditions of operators may have negative literals.

The meaning of this precondition and post-condition is that these assertions are true in the world before this operator can be applied.

## Exercise: Operators

Fill in missing preconditions and postconditions for Descend-ladder, paint-ceiling, and paint-ladder.

Climb-ladder:
  Precondition:
    on(robot,floor) & dry(ladder)
  Postcondition: On(Robot, Ladder)

Descend-ladder:
  Precondition: on(robot,ladder) & dry(ladder)
  Postcondition: on(robot, floor)

Paint-Ceiling:
  Precondition: on(robot, ladder)
  Postcondition: painted(ceiling) & !dry(ceiling)

Paint-ladder:
  Precondition: on(robot,floor)
  Postcondition: painted(ladder) & !dry(ladder)

Convention is to often not use conditions that are negated like !painted(ladder) instead of dry(ladder)for a precondition because of it’s history.  In the 60s at Stanford Research Institute a early robot planner that ran under the robot called Shakey.  Strips, the planner, used theorem proving to form plans and it turned out that the use of only positive literals in the preconditions made the theorem proving processes more efficient.

## Planning and State Spaces

Goals provide us with the control knowledge on deciding how to select between different operators.  An example of this is driving from start to goal.  Means-Ends analysis uses goals as control knowledge. Planning provides more systematic methods for selecting between operators.

A plan may look like the following:

On(Robot, Floor) & Dry(Ladder) & Dry(Ceiling)
         |
CLIMB-LADDER
         |
on(robot,ladder) & dry(ladder) & dry(ceiling)
       |
PAINT-CEILING----------------------------------------Paint-Ceiling:
    Precondition: on(robot, ladder)
    Postcondition: painted(ceiling) & !dry(ceiling)
       |
On(robot,ladder) & dry(ladder) & !dry(ceiling)
Painted(Ceiling) 
       |
Descend-ladder
       |
 On(robot,floor) & dry(ladder) & !dry(ceiling)
Painted(Ceiling)


## Planning

Means-End Analysis can run across conflicts that may waste time waiting for events to complete.

How can an AI agent resolve conflict between these goals?  How can planning systemitcally find out how to organize these various operators so conflicts do not occur.

Simple planners are sometimes called linear planners.

## Partial Order Planning

An example of partial-order planning, a preassembled couch won’t fit through a bed room door.  It needs to be disassembled and rebuilt once inside.  The plan for assembling the couch clobbered the goal of getting the couch into the apartment.

How can partial order planning be used to detect conflicts and avoid them?

## Detecting Conflicts

Partial order planning is sometimes called non-linear planning.

Goal: Painted(ladder)
On(robot,floor) & dry(ladder) & dry(ceiling)j
|
Paint ladder
|
On(robot, floor) & !dry(ladder) & dry(ceiling) & painted(ladder)

A couple things to point out.  First, paint-ladder’s post condition is apart of the bottom state.  Second, Initial state propagates some of it’s properties to bottom state.

## Exercise Partial Planning

What operator would be selected and what states would reuslt in order to accomplish the goal Painted(Ceiling)?

Goal: Painted(ladder)
On(robot,floor) & dry(ladder) & dry(ceiling)j
|
Paint ladder
|
On(robot, floor) & !dry(ladder) & dry(ceiling) & painted(ladder)

Goal: Painted(ceiling)
On(robot,floor) & dry(ladder) & dry(ceiling)
|
?
|
?
|
?
|
?

Becomes…
Goal: Painted(ceiling)
On(robot,floor) & dry(ladder) & dry(ceiling)
|
Climb-Ladder
|
On(robot,ladder) & dry(ladder) & dry(ceiling)
|
Paint-Ceiling
|
On(robot,ladder) & dry(ladder) !dry(paint-ceiling) & painted(ceiling)

How would an AI come up with this plan?

If AI knows the goal, which operator has post condition paint-ceiling?  AI then could work backwards and follow the post and preconditions.  Goal is used as control knowledge.  

Problem is broken down into subgoals like Problem Reduction.  Planning provides the “how” as opposed to basic problem reduction.

## Detecting Conflicts

If two goals are independently viewed, a partial plan can be made for each of the two goals.  Thus far, no detected conflicts between them.

Examine relationships between both plans to find conflicts.  How would you find a conflict?

Detecting Conflicts:
For each precondition in current plan:
      If precondition for an operator in the current plan is clobbered by a state in another plan:
           Promote current plan’s goal above other plan’s goal

To resolve conflict, goals in one plan may be given a higher priority. 

Referring to the previous exercise, a planner may promoted Painted(Ceiling) above Painted(Ladder)

Sometimes there is an open condition where if On(Robot,Ladder) must be On(Robot,Floor).

## Open Preconditions

To solve the open precondition, the AI must select an operator that avoids this conflict.  if On(Robot,Ladder) and needto be On(Robot,Floor).  The AI would select descend-ladder between these states to resolve this open precondition.


What does this tell us about Human Cognition?
KNowledge is not just about the world.  Know is also controlled knowledge.  It is often tacit, control knowledge helps us decide between operators.
Goals are control knowledge.  Goals can be used to decide between different operators by selecting an operator that helps us move closer to the goal.
Partial order planning can be viewed as an interaction between several different kinds of agents or abilities.  Each agent represents a micro ability.  There is an agent which is responsible for generating plans for each of the goals independently.  There is an agent responsible for detecting conflicts between them.  A third agent for resolving conflicts.

Minsky has proposed a notion of a society of mind.  A society of intelligent agents that work together to produce complex behavior where each agent itself is very simple.

Humans solve these latter problems almost instantly.  The AI makes the process explicit.  AI must have its program written very explicitly which may provide a hypothesis about how humans might be doing it.

## Hierarchical Task Network Planning

A plan generated can be very large.  Can the operators be abstracted so that they are a higher level type of operator that can be deconstructed to their smaller parts?

## Hierarchical Decomposition

Final Plan:

Move(D,Table)   |
Move(B,Table)   ---   unstack
Move(A,Table)   |
Move(C,D)      }
Move(B,C)      ---  Stack-ascending
Move(A,C)      }

Unstack and stack-ascending have each a precondition, postcondition, and method.

## Hierarchical Planning

Agents approach complex plans with the previously mentioned abstract so it seems smaller and simpler.  

Fundamental:  Agents use knowledge to tackle large complex problems.

## Assignment: Planning

How would you use planning to address RPMs?

What are the states?  What is the initial and final state?  What are the operators for transition between them.  How to select each operator.  How to detect conflicts?  How to avoid conflicts?

First, we can think of agent as having a plan to address any new problem that it encounters.

Second, the agent can discern the underlying plan behind a new problem.


## Wrap Up

Planning in propositional logic
Goal Conflicts
Partial-Order planning for conflict avoidance 
Hierarchical Task Networks

## The Cognitive Connection

Planning is central to human cognition because action selection is central.  How to make decisions?

Cognitive agents have multiple goals.  



