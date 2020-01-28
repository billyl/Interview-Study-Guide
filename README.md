# Interview Study Guide

### Dynamic Programming vs Backtracking

Comparison to Dynamic Programming

Dynamic Programming and Backtracking have multiple similarities and differences and are often confused when first learning about them. Often, the confusion comes simply from the name collision where there is a part of DP that involves 'backtracking' to recreate an optimal solution sequence at the end of the DP. For example, when finding the minimum path through a grid in DP we may want to minimize the number of jumps taken, but to reconstruct that final path we often need to go backwards from our final solution to retrace all of the steps that got us to the optimal point in order to reconstruct the minimal path. This is not the Backtracking algorithm.

In backtracking, we are exhaustively searching through a solution space by applying local transformations and collecting solutions we find as we go. It is named 'backtracking' because we will need to back out of each local transformation we make to our current solution in order to continue searching the rest of the space. Imagine searching a labrynth and you have no information so your only choice is to search all paths out. Of course you leave a trail of crumbs behind you so that once you hit a dead end you can backtrack along the crumbs to return to the first position where you could have made a different decision, i.e., all forks in the road. You can continue to do this until you have explored all possible paths through the labrynth.

It is similar to DP in that we are exhaustively searching a solution space guaranteeing that we will touch all solutions that matter. And it is also similar to DP in that the difference between a highly performant algorithm and not is often how you structure your search. In the case of backtracking, the best solutions often model the problem in some way that allows them to quickly prune state prefixes that cannot lead to solutions.

Unlike DP, backtracking is typically not looking for one **optimal** solution, but is instead looking for all that satisfy some criteria. So the structure of the algorithm is much less about being efficient at throwing previous information that you don't need because it doesn't lead you to the optimal solution and more about learning what parts of the space you don't need to explore as you are collecting all solutions that qualify.

[Source](https://guides.codepath.com/compsci/Backtracking#glossary)
