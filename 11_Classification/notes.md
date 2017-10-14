# Classification

## Lesson Preview

* Equivalence classes and hierarchies

* Kinds of Concepts

* Bottom-up and top-down processes

## Concept Learning Revisited

Classifying Birds given pictures.  Accept or Reject pictures if they do or do not meet certain criteria and conditions for being a bird.

## Classifying Birds

Questions asked for classification:
 has wings? has feathers? has talons? has a beak?
 flies? runs?
 lays eggs?
 carivorous? vegarian?
 blue? red?
 swims?
 builds nests?

These are known as percepts.

## The Challenger of Classification

The previous percepts are input into our Cognitive System and it provides an output.

2^n percepts -> 2^m actions possilbe for output

Very, very large amount of percepts and outputs possible which makes the challenge of classification extremely difficult.

10 percepts = 1024 combiniations
100 percepts = 1.2 * 10^30 combinations

Personal observation, NP type of problem.

## Equivalence Classes

One way to solve the ineffeciency presented from the previous section is with Equivalence Classes.

New formula:
  2^n percepts -> k concepts -> 2^m actions possilbe for output

Example, go to the doctor for being sick.  He prescribes a red or blue pill to address some symptoms but does not address all possible combinations of symptoms.

Schools extensively study Classification.

If Equivalence classes were not used, 2^n percepts would be rows and 2^m actions would be columns in a huge table.

## Excercise Equivalence Classes

After providing answers to certain bird criteria such as Eagles lay eggs, they have wings, they do not have fur, etc.  We use this incremental learning approach to build an equivalence class for different types of birds.

## Concept Hierachies

Concept Hierachies relate to incremental learning and background knowledge.

Organization provides power.  Establish a node, refine it.

## Types of Concepts

Types of concepts spectrum:

More formal
|  - Axiomatic concepts
|
|  - Prototype concepts
|
|  - Exemplar Concepts
|
|
|
Less Formal

These concepts are the most common.

Axiomatic like mathemtical.  Easy for computers and humans.

Prototype concepts are hard for humans but we can understand them.  Harder to teach computer these.

Exemplar concepts like beauty of freedom.  Harder to talk about these types.  Extremely difficult to teach computers these.

## Axiomatic Concepts

Axiomatic concepts:  Concepts defined by a formal set of ncesslary and sufficient conditions

Example:  A circle.

Circle:  All points in a plane that are equidistance from a single point.

Easy to identify circles based on the former definition.

## Prototype Concepts

Prototype Concepts:  Base concepts defined by a typical example iwth overridable propertiers

Example:  A chair.

example, a prototypical chair has four legs.  Chair can be represented in the language of frames such as,

Chair
 # of legs: 4
 material: metal
 has-back: true
 has-arms: false
 is-cushioned : false
 etc.

Recall that Frames represent stereotypes

Not all chairs need to satisfy these properties.  That is why there is no necessary or sufficient conditions here.  For jexample, we may run across a wood chair even though our frame definition does not fit it.  In this case, this property may be overridden.

## Exemplar Concepts

Example Concepts:  Concepts defined by implicit abstractions of instances, or exemplars, of the concept.

Example:  beauty

Exemplars concepts dont have typical dconditions or ncessary and sufficient conditions.

Can give examples to illustrate.  Implicit abstraction of some examples but that is far as it can go.

Examples of beauty, a famous painting, a sunset, a flower, dancing, etc.

Extremely hard to define and produce conditions for 'beauty.'

## Order of Concepts

Review:

More formal
|  - Axiomatic concepts
|
|  - Prototype concepts
|
|  - Exemplar Concepts
|
|
|
Less Formal

Philosophers often about concepts called 'qualia'.  Raw sensations that we may get from our sensors.  An example is bitterness.  A bitter fruit can produce a memory that can similuate a bitter taste in one's mouth based on an experience from the past.  Very difficult to communicate what a qualia is to anyone else like what your definition of what bitterness is.

## Exercise:  Order of Concepts

More Formal
 | 4) Right Triangle
 | 2) Reptile
 | 5) Holiday
 | 3) Foo
 | 1) Saltiness
 | 6) Inspirational 
Less Formal

Similiar to the chemical periodic table, in this course we are building a periodic table of elements of the mind.  Instead of elements and valances and atoms, we talk about methods and represnetations.  We are discovering the fundamental knowledge for presentations and organizaations and reasoning methods that go with it.  Case-based reasoning was one reasoining method that went with certain concepts that are hard to abstract into conditions, like typical conditions, are ncessaryily logical conditions.

## Bottom-Up Search

Recall, top-down starts from the top and refines.  For example,

Vertebrate
|
Bird
|
Blue Bird

Bottom up goes in reverse

How could an AI predict hte future of the Dow Jones Industrial average to make us a lot of money?  One way it could do is look at hte GDP, Inflation, Employment.  How could it determine GDP for example?  It could look at overtime hours, consumer sentiment index, new orders index.

Short illustration of bottom-up:


Future of Dow Jones Industrial Average
|
GDP
|----------------------------------------------------------
|                             |                         |
Overtime hours      Consumer sentiment index      New orders index

If we know the values and features that go into the concepts like Overtime hours or New orders index, we can abstract them then find the value of the say the GDP and repeat going up.  Identify and abstract.

We have identified two elements of our periodic table thus far:  Top-down and Bottom-Up

## Assignment: Classification

* How would you use classification to design an agent that could answer Raven's Progressive Matrices?

Will you develolop the classification scheme yourself, or are you going to have agent learn it as it encounters new problems?

What would that classification scheme look like?

What percepts will the agent use to classify new problems int othat classific ation scheme?

Once it classifies them, how would they use to solve hte problem?

What will it be able to do this way tthat iw wouldnt have been able to do otherwise?

## Wrap Up

Classification is one of the biggest problems in AI.

Recap:

* Concept Learning - take examples and abstract away a concept.
* Equivalence Classes j- Group sets of percepts into equivalnce classes to establish a particuular instance of aconcept.
* Concept Hierarchies - Example is the animal kingdom where the animals make up vertebrae, birds, etc.
* Axiomatic, prototypical, and examplar concepts.
* Bottom-up Search - look at lower variables and abstract up from them.

Next is logic, which is a bit unrelated to Classification.

Further topics on Classification are Diagnosis and Configuration which heavily leverage Classification.

## Cognitive Connection

There is a lot to be said about the conncection between classification and cognition.  Classification is ubiquitous in cognition.

Examples are, you see a car and you classify it as a Pourche. Another example is that you run a faulty program and you find the bug and name it.  Doctor names a disease categoryh based on symptoms.  These are ideas of classification.

The reason classification is ubiquitous is that it allows us to select actions.

Example, once the doctor knows the disease category, she can prescribe or suggest a therapy.