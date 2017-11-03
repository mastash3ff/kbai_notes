# Logic

## Preview
Logic is a formal language that allows us to make assertions about the world in a precise way.

Logic -> Planning

Logic is important topic and because it forms the basis for Planning.

Formal Notation
Conjunctions, disjunctions, negations, implications
Truth Tables
Rules of Inference like modus ponens and modus tollens
Resolution theorem proving. - method for proving theories by repetition

## Why do we need formal logic?


Why do we need to use formal logic to design an AI agent.

Two parts to the AI agent:  Knowledge base and inference engine.

Knowledge base is the agent’s knowledge about the world.
Inference engine applies rules of inference to the knowledge that the agent has.

In certain situations we may want the AI agent to be able to show or to be able to prove that the answers that it derives to any problem in fact are provably correct.

We may want the AI agent ot generate only provably correct solutions.  How can we guarantee this?  Complete and correct knowledge base and rules of inference that guarantee correctness of the answer.

Inferencing has two properties.  

Soundness:  Only valid conclusions can be proven
Completeness: All valid conclusions can be proven.

If an agent can use logical rules of inference on its knowledge base and provide guaranteed soundness and completeness then it’s a very useful thing for an AI agent to have.

Logic will be discussed in limited detail in this course for a number of reasons.  Instead of talking about knowledgein the form of logical sentences, we are much more intrested in conceptual, experiential, and heuristic k,nowledge.  Second, logic based agent has two parts to it:  knowledge base and inference engine.  This presents the problem of how we present a complete knowledge base.  If the knowledge base of an AI agent is not correct and complete then it may not provide useful answers using inference even when roots of inference are sound and complete.

Logic in this course will be used in this course when it’s useful for speicifying other methods that use conceptual knowledge, experiential knowledge or heuristic knowledge.

## Inferences about Birds

If an animal has feathers, then it is a bird.  If an animal lays eggs and it flies, then it is a bird.  

Sentences like this we will put into the language of logic.

## Predicates

Predicate:  a function that maps object arguments to true or false values.

How can we construct a knowledge base in the language of logic?

Example 1  

Feathers(bluebird).  Bluebird is an object and Feathers is the predicate on this object.  Feathers is a function that maps to true or false.  So the function output is true for this example.

Example 2

If an animal has feathers, then it is a bird.

If Feathers(animal): Then Bird(animal)

This example has two predicates, feathers and bird but only one object which is animal.  Sentence captures relationship between both predicates.  Sentences like this are known as having ‘implications’  The example is an implicative relationship.

## Conjunctions and Disjunctions

“And” and “OR” logical operators for conditions

Example, if an animal lays eggs or it flies, then it is a bird.

 lays-eggs(animal) OR flies(animal)


## Implies

A == B

## Notation Equivalency

AND a&b
OR a|b
NOT !a
IMPLIES A = B

## Excercise: Practicing Formal Logic

If an animal lays eggs and does not have feathers, it is a reptile
lays-eggs(animal) ^  !feathers(animal)  => Reptile(animal)

If an animal has feathers or has talons, it is a bird
feathers(animal) OR talons(animal) => bird(animal)

If an animal lays eggs, has a beak, and flies, it is a duck
lays-eggs(animal) & beak(animal) & flies(animal) => duck(animal)

If an animal lays eggs, has a beak, and does not fly, it is a platypus
lays-eggs(animal) & beak(animal) & !flies(animal) => platypus(animal)

## Truth Tables

Skipped

## Truth of Implications

T => T = T
T => F = F
F => T = T
F => F = T

## Implication Elimination

Given: a => b

Rewrite as
!a OR b

## Rules of Inference

Rules of Inference: Instantiate general rules to prove specific claims

Modus Ponens
p => q
p
Therefore q

Feathers => Bird
Feathers
Therefore Bird

Modus Tollens
p => q
!q
Therefore !p


Modus Tollens aka contrapositive

## Prove Harry is a bird

Prove that Harry is a Bird

Feathers(animal) => Bird(animal)
Feathers(Harry)
By Modus Ponens Therefore Bird(Harry)

Prove Buzz does not have feathers
Feathers(animal) => Bird(animal)
!Bird(Buzz)
Therefore !Feathers(Buzz)

Downsides of using logic, like Truth tables, is based on the complexity of sentences trying to prove.  A truth table will be come very complex thus computationally it will be very expensive for large sentences.  

Even if Modus Tollens and Ponens were applied to a very large number of sentences to find truth values.  But if the knowledge base consisted of a large number of sentences, instead of just one or two sentences then the number of inferences become very large.  The problem space can become very large for following the truth tables for sentences as well.
These methods are not computationally feasible for complex tasks and agents that have limited computational resources.

## Universal Quantifiers

Thus far only propositional logic have been used and specific values have been referenced like a specific animal.  Example,
Lays-eggs(animal) & Flies(animal) => Bird(animal)

Values, or animals, can be talked about in general.  Any animal, all animals.  Variables are introduced.

Audilogic, aka predicate calculus, example:

For all animals:
For all x[Lays-eggs(x) & Flies(x) => Bird(x)]

In reference to Predicate logic, Instead of animal, a variable is used.

For all X is a universal quantifier

For one animal:
Lays-eggs(animal) & Flies(animal) => Bird(animal)

For at least one animal:
There exists y[Lays-eggs(y) & Flies(y) => Bird(y)]

## A Simple Proof

AI has developed more efficient methods called Resolution Theorem Proving.

Example, a robot’s job is to lift something off the assembly line and place it somewhere.  Every now and then a human plays a joke on the robot.  They glue a widget to the assembly line belt.  When the robot cannot move it, it uses logical reasoning to figure out that the widget is not liftable and moves onto the next widget.

!can-move => !liftable

We find:  
!can-move

How do we prove that the box is not liftable besides something trivial like Modus Ponens?

By implication elimination:
!can-move => !liftable 
BECOMES 
Can-move || !liftable

Which is conjunctive normal form of the original sentence.  Implication is removed.

Resolution Theorem Proving is like proof by refutation (Proof by Contradiction).  We take the negation of what we want to prove.

Sentences thus far:
Can-move || !liftable
!can-move
Liftable

Look for a sentence that is the negation,!liftable, of what we want to prove, liftable.  The first sentence contains it, Can-move || !liftable

So liftable and !liftable can not both be True so we can eliminate them which is called resolution.

What is left over after resolution:
Can-move || !liftable
!can-move
Liftable

Now can-move and !can-move contradict each other, so we eliminate them too so nothing is left:
Can-move || !liftable
!can-move
Liftable

This leaves the null condition proving that liftable cannot be true therefore !liftable is true.

In this example, resolution theorem proving appears to of made the problem more complex.  In general it is not.  The example used fulfilled the form of Modus Ponens directly.  In general, deciding on which sentence to apply the modest ponens on, and how to combine those groups of inferences make it computationally harder than deciding how to apply the resolution theorem proving

## A More Complex Proof

Example that cannot be easily provided with Modus Ponens:

We know:
 !can-move & battery-full => !liftable

We find:
!can-move 
battery-full

How do we prove the box is not liftable?

Implication Elimination:
!( !can-move & battery-full ) | !liftable
This is still not conjunctive normal form because there is a disjunction of a conjunctions:
 ….  | !liftable

So we apply Demorgan’s Law to get
Can-move | !battery-full | !liftable

Sentences thus far:
S1: Can-move | !battery-full | !liftable
S2: !can-move
S3: Battery-full
S4: Liftable

Original problem was to show that not liftable.  Therefore, we will use proof by contradiction to further simplify the problem.  We find that S4 and S1’s !liftable contradict each other to get:

S1: Can-move | !battery-full | !liftable
S2: !can-move
S3: Battery-full
S4: Liftable

Likewise battery-full a contradict to get:

S1: Can-move | !battery-full | !liftable
S2: !can-move
S3: Battery-full
S4: Liftable

And likewise for can-move elimination:

S1: Can-move | !battery-full | !liftable
S2: !can-move
S3: Battery-full
S4: Liftable
Resulting in a null that proves that the robot cannot lift.

When the problem space is very large, it’s difficult for the AI agent to focus on.  Because the problem is in conjunctive normal form and resolution theorem proving is making use of resolution(problem reduction?).  As a result, at anytime the AI agent as a result knows exactly what to focus on.  For example,
Always start with S4’s literal.  
Find a sentence which contains this literals negation.  Resolve those found.
Proceed forward with sentences that have not been resolved.

This computational efficiency of resolution theorem proving is arising because of Horne Clauses.

Horne Clauses is a disjunction that contains at most one positive literal.

Referring to the previous example, this is happening in S1 which is a disjunction that contains the positive literal, can-move.

## Exercise: Proof I Quiz

If an animal has wings and does not have fur, it is a bird.

How would this be written in formal logic to prove this is a bird?

wings(animal) & !fur(animal) => bird(animal)
Wings & !fur => bird

Convert to conjunctive normal form for resolution theorem proving.
Eliminate implication using the property: A=>B with !A | B

!(Wings & !fur) | bird    (This is not conjunctive normal form yet.  Use DeMorgan’s Law)
!Wings | fur | bird

Resulting sentences thus far:
S1: !wings | fur | bird
S2: wings
S3: !fur
S4:  What sentence should be assumed to facilitate the proof?

S4: !bird  (Opposite of what we want to provide aka contradiction)

Bird is eliminated first so that:
S1: !wings | fur | bird
S2: wings
S3: !fur
S4:  !bird

Then resolve wings and fur:
S1: !wings | fur | bird
S2: wings
S3: !fur
S4:  !bird

Therefore a null which is a contradiction proving by the resolution theorem that it is a bird.

Logic has been mechanized to where large truth tables and complex chains of inferences are not needed.  The recipe in summary:

Take all the sentences in the knowledge base and convert to conjunctive normal form.
Use Proof by Contradiction to assume what you want to prove
Eliminate all the contradictions to result in a proof.

If a null condition is not found based upon not finding enough contradictions, then what was started with cannot be proved.

## Assignment: Logic

How would formal logic be used to solve RPMs?

Like production systems, these problems can be faced at two different levels:
Use formal logic to represent the overall algorithm the agent uses to solve any new problem.
OR
Use formal logic to develop its understanding of a new problem that just came in.  Use those formal rules to transfer those transformation into a new answer.

Alternatively, formal logic could use used to allow the agent to prove why it’s answer to a particular problem is correct.  If the answer is incorrect, then the agent may have the information necessary to go back repair it’s reasoning and do better next time.

## Wrap Up

Formal Notation (Conjunctions and Disjunctions)
Properties of truth values
Rules of inference
Proof by Refutation
Planning leverages formal logic to reason about start and goal states.  Originally agents would prove that a particular plan would work first before planning.

## The Cognitive Connection

Logic is important to AI because of these reasons:
Logic provides a very formal and precise way of reasoning.
Logic provides a formal notation for intelligent agents to reason whether or not they are using logical reasoning.

Does this mean logic is at the basis of human cognition?

Humans use logic some of the time by making assumptions via Modus Ponens.  This does not mean that humans use logic to solve new problems.  An analogy to a previously encountered problem could of been used.  Although logic was not used, it appears to exhibit logic.

Deductive logic has been used thus far.  A lot of human reasoning is inductive or abductive.

Deduction uses reasonings from causes to effects.

Abduction uses reasonings from effects to causes.  Like a doctor diagnosing.

Induction given some relationship between cause and effect, how do we generalize it between a cause and effect relationship for a population.

