# Learning By Recording Cases

## Preview

* Analogical Reasoning *
Learning by Recording Cases -> Case-Based Reasoning -> Explanation-Based Learning -> Analogical Reasoning

* Learning by Recording cases
* Nearest neighbor method
* k-nearest neighbor
* cases in the real world

## Learning By Recording Cases

1. Given new problem a
2. Retrieve most similiar prior problem, b, from memory
3. Apply b's solution to problem a

Example: Get up to run.  Tye shoe laces.  How do I know how to tie shoe laces?  Retrieve from memory.  Use cases from the past.

Example:  Medical diagnosis.

Case is an encapsulation of a previous experience.

## Case Retrieval by Nearest Neighbor

How to make more explicit instead of generalized?
Using the Block World problem, use a grid to plot the blocks by Width x Height.

Calculate distance between existing case and new problem

Euclidean distance:  d = sqrt(( y_c - y_n)^2 + (x_c - x_n)^2 )

Calculate between all existing cases to find closest.  AKA Nearest Neighbor

## Nearest Neighbor for Complex Problems

Using a map of New York that has higher dimensionality, we plot routes by origin and plot routes by destination.

Routes by origin is the original coordinates of a point A for example
Routes by Destination is where point A finishes it's route.

We calculate with these values euclidean distance.

If we focus on Origin, B caseit seems closest.  But the destination distance is large.
if we focus on Destination, E case seems closest but the origin distance is large.
Neither are good answers b/c euclidean distance does not scale well to the data.
How would an AI decide D is the best route?

## Nearest Neighbor in k-Deimnsional Spaces

New forumula to generalize neighest neighbor:
c is existing case
p is new problem

d = sqrt( sum_i=1 to k (c_i - p_i)^2   )

Route D calculates to where the following values are c_i in the new formula:  4 + 8 + 4 + 1 becomes 4.36

Able to find best fit for finding a route based on previous cases.
Modified distance formula finds D to be the best route.
Suffers from high dimensionality.

## Assignment: Learning by Recording Cases

How would you use recording cases to design an agent that could answer RPMs?

Each figure in a problem could be a case.
Each transformation between figures can be a case.
More generally, each problem in the past can be a case.

How would a simliarity metric be composed for evaluting figures, transformations, or Problem in the past is most similiar now?

## Wrap Up

* Recording and using cases
* Nearest neigbor method
* Cases in real-world probelsm
* Nearest enighbor in k-dimensional problems

Limitations:
Executing from the past doesnt work.
Sometimes have to use qualitative instead of quantitives labels.

There are weaknesses that will be addressed later in lecture videos in case-based reasoning.  

## Cognitive Connection

Strong connection to cognitive.
We use previous cases all the time to solve today problems

reasoning, memory, learning.  Reasoning is not used that much.  Learning and memory are more important.