# Semantic Networks

## Lesson Preview

* Knowledge Representations
* Semantic Networks
* Problem-Solving with Semantic Networks
* Represent & Reason

## Representations

Knowledge and Repesentation has two things:  Language and Content.  Affordances and constraints.

## Intro to Semantic Networks

Represent Objects as x, y, and z.
Represent relationships between objects by Links which describe the relationship.

Want to capture the knowledge of the transformation from A -> B so that it can be applied to C -> D.

First part deals with objects in A and the objects in B.
Second part deals with relationships between the objects in A and the objects in B.
The third part deals with the relationships between the objects in A and the objects in B.

Capture relationship between A and B in a Raven Matrice.  What has changed?  What has not changed?

## Structure of Semantic Networks

Lexically: nodes
Structurally: directional links
Semantically: application specific labels

A knowledge presentaiton, will have a lexicon.  That tells us something about the vocabulary of the presentation language.
A structure which tells us about how the words of that vocabulary can be composed together into complex represetnations
The semantics which tells us how the representation allows us to draw inferences so that we can in fact reason.

Further Explanations of Lexicon, Structure, and Semantics.
Basic lexicon consists of nodes that capture objects.  So x, y ,z.
Structural specification consists of links which have directions.  These links capture relationships and allows us to compose these notes together into complex representations.
Semantics places labels on links to allow us to draw inferences and do reasoning over these representations.

## Characterstics of Good Representations

Make relationships explicit
Expose natural constraints
Bring objects and relationships together
Exclude extraneous details
Transparent, concise, complete, fast, computable.

## Guards and Prisoners

Appeared in 1200-year-old-text "Propositiones ad Acuendos Juvenes."
Used by through AI for problem representation.

## Semantic Networks for Guards

Each node is a state that captures how many prisoners/guards are on one side of the boat.
A link goes between node to capture a transition to another state.

## Solving the Guards and Prisoners Problem

Generate all possible moves.  Some are illegal.  Some not productive.

## Represent & Reason for Analogy Problems

Forming representations of the Figures A -> B and C -> 5, can we decide whether 5 is the correct answer?

If two representations of transformations are closely matched, an answer can be reasonably assumed.

This leads to a problem when two representations are identical and one answer is not apparent.

## Choosing Matches by Weights

If two Transformations are the same, as in different actions achieve same state, decide with similiarity weights.

Example:

5 pts Unchanged
4 pts Reflected
3 pts Rotated
2 pts Scaled
1 pts Deleted
0 pts Shape Changed

More points means greater similiarity and less difficulty.  Less points holds the opposite.

## Connections

Memory is integral to part of the cognitive systems architecture.

Example:  A and B are stored in memory.  Then C and 1, C and 2, C and 3, and so forth are probes into memory.

The question is, which one of these probes is most similar to what's stored in memory?

One answer may be based on similiarity metric.

Another connection is reasoning.  When deciding between an enclosed Circle(Two Circles in total), do we make a connection between the outer circle here and Figure B or the inner circle and Figure B?  This is called a correspondence problem.

Correspondance problems will be brought up in analogical reason.

Third Connection has to do with cognition, of knowledge based AI as a whole.  Instead of talking about properties of objects, like this is a circle and the size of the circle, our emphasis has been on the relationships between the objects.  Example, inside the outer circle; circle remains the same; inner circle dissappears.

In KBAI, in general, focus is always on relationships.  Not just on the objects and the features of those objects.

## Assignment:  Semantic Nets

Write a representation scheme.
Talked about how that representation enables problem solving.

Good qualities of a good knowledge representation is that it's complete, it captures information at the right level of abstraction, and enables problem solving.

Semantic network does not capture the solution but the representation of the problem.

## Wrap Up

Knowledge Representations
Semantic Networks - What do they help us do and help us avoid.
Represent and Reason - An abstract class of problem solving that lies at the heart of KBAI.  Simply put, represents knowledge then reasons over it.
Weights with Represent and Reason - Allows us to come to more nuanced and specific conclusions.

## The Cognitive Connection

Semantic Networks are knowledge representations.
The human brain represents problems.
Human uses its knowledge to address problems.
Representation becomes key.
Second, semantic networks are related to spreading activation networks which is a very popular theory of human memory.

Example:  Story consisting of two sentences.

John wanted to get Rich.  He got a gun.

Draw inferences without complete information.

Start point is that John wanted to get Rich and it gets activated and spreaded among nodes
End point is that He got a gun which activated and spreaded among nodes.
Both sets of nodes merge to form a path or story.