### This is my personal note when learning dynamic programming.
### (The reference is the *Introduction to Algorithms*)
Dynamic programming: It's a method that could through combining subproblems(optimal substructure) to sovle optimization problem.

We can recursively solve some optimal substructures (usually top-down) or make state transition directly from bottom to top.

But the former is very inefficient,both time and space.Because it solves many subproblems repeatedly.

So we'd like to solve such problem by dynamic programming.We save computing time by spending extra space.This is a typical time-memory trade-off example.

The first method is top-down with memoization,we will save all the solution of all the subproblem.

And the second method is bottom-up method,this method requires us to define the scale of subproblem properly.

We focus on the second method:

1. For a problem, we define it as P,and P(i) is the optimal solution when the scale of the problem is i.

2. And we know that the solution of P(i) is depends on smaller P's solutions,such as P(k)(k<i).Only when we get all the solutions that P(i) depends,we could get the P(i)'s soultion.We might as well write this process as P(i)=max(fun(p(k))(k<i,and the answer might be some satisfied k through some kind of operation (that is, some kind of function)).

And now we will discuss how to find the properly way to plan the substructure and find the appropriate transfer equation. 

1: You should choose a op
