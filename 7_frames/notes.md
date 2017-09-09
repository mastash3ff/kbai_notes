# Frames

## Preview

* Function of Frames
* Properties of Frames
* Relationship between frames and previous topics
* frames for advanced sense-making

Frames are knowledge representations.
Frames are the first unit in common sense reasoning:  Frames - Understanding - Common Sense Reasoning - Scripts

## How we make sense of a sentence?

"Ashok ate a frog"
How to capture meaning?
One word at a time.

"Ate"
  Subject: Ashok
  Object: a frog
  Location:
  Time:
  Utensils:
  Object-Alive: false
  Object-Is: in-subject
  Subject-Mood : happy

Frame is a knowledge structure.  Has slots and fillers.

## Exercise:  Making sense of a sentence

Q: Angela at lasagna with her dad last night at Olive Garden
A:
  Subject:  Angela
  Object: lasagna
  Location: Olive Garden
  Time: Last night
  Utensils: 
  Object-Alive: false(default)
  Object-Is: in-subject(default)
  Subject-Mood: Happy(default)

(default) represents default values using "common sense reasoning."

## Complex Frame Systems

Frames can be connected with another.  A frame can point to another frame.  Can infer information from other frames.  If Angela has a preference for Italian Foods, we can infer that she is happy after eating lasagna.

Complex frames play a strong role in common sense reasoning.

## Properties of Frames

* Represent sterotypes - frames represent stereotypes.  What happens when something is done.  Stereotypes are culture specific.

* Provide default values - Default set values. Can also add exceptions.  If Ashok ate a frog, he become very sad.  Get's really complex having to handle exceptions.

* Exhibit Inheritance - Frame hierarchy.  OOP programming concepts.

Frames and OOP came up in the 1960s at the same time.

## Excercise:  INterperting a Frame System

Q. What sentence is expressed by these frames(in the lecture video)?
A. Haruto ate a pepperoni pizza during noon at Pizza Hut.

## Frames and Semantic Nets

Frames can be used to address RPM.
Semantic nets and frames are closely related.

Rewrite semantic network into frames.  Frame has to be built for each object.

Object1                   Object2
  name: x                 name: z
  shape: triangle         shape: circle
  size: large             size: small
  fill:false              fill: true
  inside:--------         inside:
  above:        |------>  above:

## Exercise:  Frames and Semantic Networks

Object
  name: x
  shape: triangle
  size: large
  fill: false
  inside: 
  above:
Object
  name: y
  shape: circle
  size: large
  fill: false
  inside: 
  above: x
Object
  name: z
  shape: circle
  size: small
  fill: true
  inside: y
  above: x

## Frames and Production Systems

We used frames previusly in production systems as "working memory"

Procedural Semantic Episodic
   |         |       |
    \        |       / 
       Working Memory

## Exercise: Frames and Complex Understanding

Earthquake:
  Subject: Lower Slabovia
  Casualties: 25
  damage: $500 mill
  time: today
  magnitude: 8.5
  location: lower slabovia
  faultline: Sadie Hawkins
  time:
  type:
  duration:

Used bottom up processing by generating slots then filling from story.

Multiple frames will same slots having different contexts and meanings are complicated.

## Assignment

* How would you use frmaes todesign an agent that could answer RPMs?
Receive problem in frames initially or generate frames from reasoning?

With frames in hand, how would they be used to solve the problem based on the frames?

Frames representing individual figures from the problem.  What about representing the problem as a whole?

What about frame representing individual shapes in figure?  How would that level of abstractoin help solve the problem more easily?

What do frames enable us to do that we couldnt do otherwise?

## Wrap Up
* Structure of ramaes - slots and fillers.  similiar to oop
* properties - dfault values, inherit, stereotypes from a oncept
* frmesm with othe represetnations - semantic netsare equivalent representively.  used in production systems.
* story understanding

Jump forward to understanding, commonse senes reasoning and scripts leverage frames heavily.