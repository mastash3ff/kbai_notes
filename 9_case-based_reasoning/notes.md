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
Reminder:  Evalutation - Evaluating how well the adapted solution addresses the current problem.

One method of using evaluation is simulation.  If a path from start to goal is known, one can do a simulation.  Might found out the solution works and might accept hte solution.

Instead, reverse from goal to start.  We decide to flip all the turns.  But as the solution is executed, we find that some of the turns are only one way streets so this particular solution fails.

In this example, the cost of executing a solution may be low so there is little cost but in other domains the cost of execution may be high.  Therefore, we can first simulate it before we decide to execute it.

In design, we can simulate a design or we can actually prototype a design.

Another method of evaluating a design could be to share it with other designers and let them critique it.

## Case Storage

Reminder:  Storage - Storing the new problem and solution as a case.

After we have evaluated how well teh adapted solution addresses the current problem, we can encapsulate them as a case and store them in a case memory.

Saw this earlier when we saw that we could go from Home to Restaraunt.  We stored that case in memory so that when we wanted to go back from restaraunt to home, we could retrieve that case and try to adapt it.

Constantly accumating and assimiliating new cases.

Will talk about two kinds of storage mechanisms:  Indexing and discrimation tree.

## Case Storage by Index

For routes, we can produce index schemes such as xy coordinates.  Ideally want a more complex one like start and goal coordinates.  We could also have indexes whether the route is scenic or not scenic or whether the route if fast or not fast.

Want an effecient index structure because we want to store and retrieve them at a later time.

In design, people hjave developed indexical structures that have to do with functions, with operating environment, with performance criteria,etc.

## Exercise Case Storage by Index II

Storing indexes by departure and destination is useful but as we get a lot of different cases it is going to get very large and very quickly.  With a lot of variables, it could be troublesome to search.

If the storage mechanism is such that it does not allow for effecient retrieval, then its not a very good storage mechanism.

As entries in the table increase and the number of dimensions increases as well, retrieval will eventually be ineffecient.

## Case Storage by Discrimination Tree

Discrimination Tree I suppose is the same as a decision tree.

Example:  is the origin north of x location, yes/no?  iterate.

How will we add to this knowledge structure as new cases are encountered?

How will we incrementally learn this knowledge structure as new cases are put into the case library?

What happens when A and X both answer No in our Discrimination Tree?  We need a way to discriminate between A and X.  Perhaps we add a new question, is the origin East of 3E?  In the case of X, the answer is yes and the case of A is no.

The original Discrimation tree has been modified as a result of finding a new case.  Therefore the organization of the case of memory changes.  Example of incremental learning.

Three Discrimination Tree's branches do not have to binary (yes/no) they can have multiple answers.  Example:  What color is it?

## Exercise Storage by Discrimination

Previously in Storage by Index, we used a table for storing.  If it became very large it would be difficult to search for a specific case in the table.

By a discrimination tree, we can narrow down the search more rapidly.

Both methods try to accomodate and accumulate new cases.  The search in the discrimination tree is more effecient.

Indexing vs Tree:  Indexing is Linear while Tree is Logorithmic.

## Case Retrieval Revisited

Revisit retrieval now.  How can we retrieve the case relevant to a given problem?  Assume that the new problem has the same features in its description as the cases stored in the memory.

Before we navigated the tree trying to find a place to store a new case.  This time we'll use the problem to navigate this tree and find out which case is the most similiar to the problem.

## Exercise: Retrieval by Index

Going back to the map example that had routes with Destination_x and Destination_y coordinates for Indexes, What case should be retrieved and adapted?

## Exercise: Retrieval by Discrimination Tree

What case should be retrieved and adapted using a series of yes/no questions?

## Advanced Case-Based Reasoning

Review:  Retrieval ->  Adaptation -> Evaluation -> Storage

The examples thus far have been linear in the case-based reasoning process.  Case-based reasoning process may not necessarily be linear.

Example:  If the evaluation of a candidate solution fails, we might want to adapt that particular case in a different way instead of abandoning it.  Alternatively, if we try to adapt the same case several times but just cannot adapt it we might want to abandon it and find a different case from memory.

Another example:  If we retrieve a case from memory and try to adapt it to meet the requirements of the new problem and it fails.  In this case, we might want to abandon the case and try to do a new one.

Even another example:  Suppose we retrieve a case from memory perfectly matches current problem; no adaptation needed so we can jump down to evaluation.

In conclusion, the process need not be linear

Q. What if evaluation shows that the new solution is not good?  Should we store this new solution?

A. Sometimes studying failed cases is also very useful.  Failed cases help us anticipate new problems.

Failures are great opportunities for learning.  When failures occur we can try to repair the failure by going back from the evaluation step to the adaptation step.

Or try to recover from the failure by going from the evaluation step all the wayh to the retrieval step.

In addition we can store these failures in the case memory, these failures can help us anticipate failures that might occur with new problems.

On the flipside, although it is useful to store failed cases it is not useful to store EVERY successful case.  Retrieval will become less effecient over time.

This is sometimes called the utility problem.  We want to store only those successful cases that in fact help us cover a larger span of problems.  Only want to store something that is interesting and noteworth about that case.

## Assignment:  Case-Based Reasoning

How would you use case-based reasoning to design an agent that oculd answer RPMs?

How is this different by Recording by Cases alone?

Where is the adapation phase?  How are you adapting past solution to the new problem?

What is evaluation in this context?  How are you evaluating the strength of your answer?

Are you goign to record the cases that your agent counteres as they're solving the test?  Perhaps instead, are you going to equip them with past cases beforehand for them to solve new problems?

## Wrap Up

* Case Adaptation
* Case Evaluation
* Case Storage
* Case Retrieval Revisited
* Advanced case-based reasoning

Discussed broad process of case-based reasoning.  Learning by recording cases gave us a method for case retrieval called nearest neighbor method.  So went ahead and jhumped into the adaptation phase.  Given aan old solution to a new problem, how do we adapt that old solution to a new problem?

Three ways:  Model of the world, rules, recursion.  Then once we have adapted that old case, how do we then evaluate how good it was for our problem?

Then after we evaluated how good it is,we looked at storing it back in our memory.  Want to build up a case library of past solutions, so if we've solved a new problem we will sort that back into our case library.

Based on how our case library is organized, how do we retrieve a prior case that's most similar to our new problem?

Now there a lot of open issues here.  Should we store failed cases?  Should we store failed adaptations?  Do we want to store them so we can avoid failing in the future?  Should we ever forget cases?  Can our case library ever get so big that it's intractable, and can't use it effeciently.  Should be develop a abstract understanding of a concept,  or should we stick the individual cases and adapt them from there?

These questions will be revisted through the course.

Next up is incremental learnign which takes cases and abstract over them to learn higher level concepts.

## Cognitive Connection

Strong tie to human cognition.

Analogical reasoning in general is considered to be acore process of cognition.  But analogical reasoinig depends upon a spectrum of similiarity.

At one end of this spectrum are problems which are identical to previosly encoutnered prohblems.  We simply retrieve a previosly known solution and apply it.

At the other end of hte spectrum, are probelsm with semantically very dissimilar from previusly encountered problems.  These problems will be discussed later in the class.

In the middle of the spectrum are problems which are similar but not identical so we retrieeve solutions and adapt them.

Cognitive Architecture review:  Reasoning, Learning, and Memory.

Learning by recording cases shifted the balance from reaosining to learning and memory.

Case-Based Reasoning instead unifies the three of them.  It says learning is important because we need to acquire and store experiences.  Memory is important is important because we need to retrieve them.  Reasoning is important because we need to tweak(adapt) them to ecounter the needs of new problems.