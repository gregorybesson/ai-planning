# A brief history of AI planning and search

## Introduction
The planning problem in AI is about the decision making performed by a robot, a machine, a software or a human to achieve some goal.
It involves choosing a sequence of actions that will transform the state of the world, step by step, so that it will satisfy the goal[1].
It has been an area of research in AI for over 4 decades and planning techniques have been applied in robotics, process planning, autonomous agents and spacecraft mission control.
This language has been widely used in many fields including robotics and games [4].

## STRIPS: The first step
STRIPS (Fikes and Nilsson, 1971) is the first major planning system. This language is based on state variables. Each possible state of the world is an assignment of values to the state variables, and actions determine how the values of the state variables change when that action is taken [2].
STRIPS (Stanford Research Institute Problem Solver) was initially an automated planner and this name was later used to refer to the seminal formal language of the inputs of this planner.
We call it an "action language".
With STRIPS, you first describe the world. You do this by providing objects, actions, preconditions, and effects. You then can construct a graph that contains all available states and the actions that bring you to each states: The planning graph.

The limitation of STRIPS is that you need a fin
ite set of actions, preconditions and effects
## SNLP: A second step

## GRAPHPLAN: Third step

## Conclusion

## References
- [1]: https://users.ics.aalto.fi/rintanen/planning.html
- [2]: Richard E. Fikes, Nils J. Nilsson (Winter 1971). "STRIPS: A New Approach to the Application of Theorem Proving to Problem Solving" (PDF). Artificial Intelligence. 2 (3–4): 189–208. doi:10.1016/0004-3702(71)90010-5.
- [3]: http://www.primaryobjects.com/2015/11/06/artificial-intelligence-planning-with-strips-a-gentle-introduction/
- [4]: https://github.com/primaryobjects/strips#starcraft
