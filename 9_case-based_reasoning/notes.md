# Case-Based Reasoning

## Lesson Preview

Builds upon Learning By Recording Cases in Analogical Reasoning

Analogical Reasoning:
  Learning By Recording Cases -> Case-Based Reasoning -> Explanation-Based Learning -> Analogical Reasoning

* Recording cases revisted
* Need for case-based reasoning
* Phases of case-based reasoning
* Advanced case-based reasoning

## Return to Block World

Q. What color is the block?
A. Orange?

Orange is the longest short horizontal block.  Closest to new problem.  Not identical so there is an issue of matching.

How can you reason about it and adapt it to fit the problem?

## Recording Cases to Case-Based Reasoning

Retrieval -> Adaptation -> Evaluation -> Storage

Retrieval - Retrieving a case from memory similiar to the current problem (like k-nearest neighbor).
Adaptation - Adapting the solution to that case to fit the current problem.
Evaluation - Evaluating how well the adapted solution addresses the current problem.
Storage - Storing the new problem and solution as a case.


## Assumptions of Case-Based Reasoning

* Patterns exist in the world - Like Newton's second law of motion.  Scientists seek to discover these patterns.
* Similiar problems have similiar solutions. - Two similiar problems may have the same solution.

## Case Adaptation

Reminder definition:  Adaptation - Adapting the solution to that case to fit the current problem.

AI face computationally complex problems with limited resources.

Example: Cooking new recipes may involve tweaking previously known favorite recipes.

Popular cliche:  All designers redesign.

Will discuss the 3 most common ways of adapting: Model-based, recursive-based, and rule-based methods

## Case Adaptation by Model of the World

Referring to map example in video.  Want to go from Office to Restarautn.  We know of a doctor's office near Restaraunt from Office.

Take earlier case to adapt to new solution.

## Case Adaptation by Recursive Reasoning

Using map example again, Home to Restaraunt.
Don't know how to go from Home to Restaraunt but know how to go from Home to Office(which is midway between points in this example) and Office to Restaraunt.  Therefore there is a connection going from Home -> Office -> Restaraunt.

Case provided a partial solution.  Take remaining part that is not solved and make it a new problem.  Send it back into the case memory.  Case memory finds me a new case.  Compose it with the previous case to get a full solution.

Use/Find a subgoal and use it to reach a goal

In design, take solutions from multiple cases.

## Case Adaptation by Rules

Uses heuristics expressed in a form of rules.  A heuristic is a rule of thumb.

Example, where is the downtown area in a city?  How could this be done?  A simple heuristic is that you just look around for the tallest buildings.  Tallest builds tend to be in the center of the city in the USA but not in other countries.

If start to goal is already solved and want to reverse goal to start.  Reverse all the terms.  May not always work but its a general rule of thumb.

In design, if you want to make an artifact lighter, use a different material.  A heuristic expressed as a rule.

## Case Evaluation

## Case Storage

## Case Storage by Index

## Case Storage by Discrimination