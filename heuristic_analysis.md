
# Problem 1

## Introduction

We have 

## Initial states and goal
```
Init(At(C1, SFO) ∧ At(C2, JFK) 
	∧ At(P1, SFO) ∧ At(P2, JFK) 
	∧ Cargo(C1) ∧ Cargo(C2) 
	∧ Plane(P1) ∧ Plane(P2)
	∧ Airport(JFK) ∧ Airport(SFO))
Goal(At(C1, JFK) ∧ At(C2, SFO))
```

## Results

| Search Method                            | Expansions    | Goal tests | New nodes | Plan length | Time spent  |
| -----------------------------------------|:-------------:|:----------:|:---------:|:-----------:| -----------:|
| breadth_first_search                     |  43           | 56         | 180       | **6**       | 0.039       |
| breadth_first_tree_search                |  1458         | 1459       | 596043    | **6**       | 1.152       | 
| depth_first_graph_search                 |  21           | 22         | 84        | 20          | 0.016       |
| depth_limited_search                     |  101          | 271        | 414       | 50          | 0.126       |
| uniform_cost_search                      |  55           | 57         | 224       | **6**       | 0.051       |
| recursive_best_first_search              |  4229         | 4230       | 17023     | **6**       | 3.276       |
| greedy_best_first_graph_search           |  **7**        | **9**      | **28**    | **6**       | **0.005**   |
| astar_search with h_1                    |  55           | 57         | 224       | **6**       | 0.054       |
| astar_search with h_ignore_preconditions |  41           | 43         | 170       | **6**       | 0.081       |
| astar_search with h_pg_levelsum          |  11           | 13         | 50        | **6**       | 2.122       |

## Analysis

Many heuristics achieve the optimal length under a second of calculation time. This is the greedy best first search which achieve the best result.


# Problem 2

## Introduction

## Results

| Search Method                            | Expansions    | Goal tests | New nodes | Plan length | Time spent  |
| -----------------------------------------|:-------------:|:----------:|:---------:|:-----------:| -----------:|
| breadth_first_search                     |  3343         | 4609       | 30509     | 9           | 16.962      |
| breadth_first_tree_search                |               |            |           |             | TIMEOUT     | 
| depth_first_graph_search                 |  624          | 625        | 5602      | 619         | 4.029       |
| depth_limited_search                     |  101          | 271        | 414       | 50          | 0.126       |
| uniform_cost_search                      |  55           | 57         | 224       | 6           | 0.051       |
| recursive_best_first_search              |  4229         | 4230       | 17023     | 6           | 3.276       |
| greedy_best_first_graph_search           |  7            | 9          | 28        | 6           | 0.005       |
| astar_search with h_1                    |  55           | 57         | 224       | 6           | 0.054       |
| astar_search with h_ignore_preconditions |  41           | 43         | 170       | 6           | 0.081       |
| astar_search with h_pg_levelsum          |  11           | 13         | 50        | 6           | 2.122       |

## Analysis

Many heuristics achieve the optimal length under a second of calculation time. This is the greedy best first search which achieves the best result. The number of expansions is minimal in this case (7) implying a minimal number of goal tests thus explaining the success of this heuristic.

# Problem 3

## Introduction

## Results

| Search Method                            | Expansions    | Goal tests | New nodes | Plan length | Time spent  |
| -----------------------------------------|:-------------:|:----------:|:---------:|:-----------:| -----------:|
| breadth_first_search                     |  43           | 56         | 180       | 6           | 0.039       |
| breadth_first_tree_search                |               |            |           |             | TIMEOUT     | 
| depth_first_graph_search                 |  624          | 625        | 5602      | 619         | 3.923       |
| depth_limited_search                     |               |            |           |             | TIMEOUT     |
| uniform_cost_search                      |  55           | 57         | 224       | 6           | 0.051       |
| recursive_best_first_search              |  4229         | 4230       | 17023     | 6           | 3.276       |
| greedy_best_first_graph_search           |  7            | 9          | 28        | 6           | 0.005       |
| astar_search with h_1                    |  55           | 57         | 224       | 6           | 0.054       |
| astar_search with h_ignore_preconditions |  41           | 43         | 170       | 6           | 0.081       |
| astar_search with h_pg_levelsum          |  11           | 13         | 50        | 6           | 2.122       |

## Analysis

Many heuristics achieve the optimal length under a second of calculation time. This is the greedy best first search which achieve the best result.
