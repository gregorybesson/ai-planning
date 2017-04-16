# A brief history of AI planning and search

## Introduction
The planning problem in AI is about the decision making performed by a robot, a machine, a software or a human to achieve some goal.
It involves choosing a sequence of actions that will transform the state of the world, step by step, so that it will satisfy the goal\[1\].
It has been an area of research in AI for over 4 decades and planning techniques have been applied in robotics, process planning, autonomous agents, spacecraft mission control and games.\[2\] \[3\]

## 1971 - STRIPS
STRIPS (Fikes and Nilsson, 1971) is the first major planning system and a language that is based on state variables. Each possible state of the world is an assignment of values to the state variables, and actions determine how the values of the state variables change when that action is taken \[4\].
STRIPS (Stanford Research Institute Problem Solver) was initially an automated planner and this name was later used to refer to the seminal formal language of the inputs of this planner.
We call it an "action language".
With STRIPS, you first describe the world. You do this by providing objects, actions, preconditions, and effects. You then can construct a graph that contains all available states and the actions that bring you to each states: The planning graph \[5\].

The Problem Domain Description Language (PDDL) \[5\] was introduced as a computer-parsable, standardized syntax for representing STRIPS.

The limitation of STRIPS is that you need a finite set of actions, preconditions and effects.

## 1975 - Partial-order planning
The ideas behind Partial-order planning include the detection of conflicts and the protection of achieved conditions from interference \[7\]. NOAH planner and NONLIN were pionners in this field \[8\].
In contrast with a total-order plan which produces an exact ordering of actions, a partial-order plan specifies all actions that need to be taken, but specifies an ordering of the actions only where necessary.
Partial-order planning dominated the next 20 years of research. SNLP being an implementation widely used by many researchers. \[9\]

## 1995 - GRAPHPLAN
The GRAPHPLAN algorithm processes the planning graph, using a backward search to extract a plan. It allows for some partial ordering among actions. It is orders of magnitude faster than the previous partial-order planners of the time: Planning graphs have polynomial size and can be built in polynomial time \[10\]. A closely related approach to planning is the Planning as Satisfiability (Satplan).

## Next steps
recent researches lead to stochastic/probalistic planning with binary decision diagrams \[11\] and Markov Decision Processes (MDP) \[12\] which are popular for modeling sequential decision-making scenarii in environments where an intelligent agent could produce actions with uncertain outcomes (not deterministic actions but stochastic).

## References
- \[1\]: https://users.ics.aalto.fi/rintanen/planning.html
- \[2\]: https://github.com/primaryobjects/strips#starcraft
- \[3\]: https://stripsfiddle.herokuapp.com/
- \[4\]: Richard E. Fikes, Nils J. Nilsson (Winter 1971). "STRIPS: A New Approach to the Application of Theorem Proving to Problem Solving" (PDF). Artificial Intelligence. 2 (3–4): 189–208. doi:10.1016/0004-3702(71)90010-5.
- \[5\]: http://www.primaryobjects.com/2015/11/06/artificial-intelligence-planning-with-strips-a-gentle-introduction/
- \[6\]: McDermott, Drew; Ghallab, Malik; Howe, Adele; Knoblock, Craig; Ram, Ashwin; Veloso, Manuela; Weld, Daniel; Wilkins, David (1998). "PDDL---The Planning Domain Definition Language" (PDF). Technical Report CVC TR98003/DCS TR1165. New Haven, CT: Yale Center for Computational Vision and Control. CiteSeerX 10.1.1.51.9941
- \[7\]: Barrett, A., and Weld, D. (1993). Partial-Order Planning: Evaluating Possible Efficiency Gains. University of Washington: Department of Computer Science and Engineering. Notes
- \[8\]: Sacerdoti, E., 1975, “The Nonlinear Nature of Plans”, International Joint Conference on Artificial Intelligence, pp. 206-214.
- \[9\]: http://homes.cs.washington.edu/~weld/papers/weld-snlp-commentary.pdf
- \[10\]: MIT OpenCourseWare lecture on GraphPlan and making planning graphs
- \[11\]: http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.121.1953&rep=rep1&type=pdf
- \[12\]: http://www.morganclaypool.com/doi/abs/10.2200/S00426ED1V01Y201206AIM017?journalCode=aim
