
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

### Non heuristics

| Search Method                            | Expansions    | Goal tests | New nodes | Plan length | Time spent  |
| -----------------------------------------|:-------------:|:----------:|:---------:|:-----------:| -----------:|
| breadth_first_search                     |  43           | 56         | 180       | **6**       | 0.039       |
| breadth_first_tree_search                |  1458         | 1459       | 596043    | **6**       | 1.152       | 
| depth_first_graph_search                 |  21           | 22         | 84        | 20          | 0.016       |
| depth_limited_search                     |  101          | 271        | 414       | 50          | 0.126       |
| uniform_cost_search                      |  55           | 57         | 224       | **6**       | 0.051       |
| recursive_best_first_search              |  4229         | 4230       | 17023     | **6**       | 3.276       |
| greedy_best_first_graph_search           |  **7**        | **9**      | **28**    | **6**       | **0.005**   |

### Non heuristics

| Search Method                            | Expansions    | Goal tests | New nodes | Plan length | Time spent  |
| -----------------------------------------|:-------------:|:----------:|:---------:|:-----------:| -----------:|
| astar_search with h_1                    |  55           | 57         | 224       | **6**       | 0.054       |
| astar_search with h_ignore_preconditions |  41           | 43         | 170       | **6**       | 0.081       |
| astar_search with h_pg_levelsum          |  11           | 13         | 50        | **6**       | 2.122       |

## Optimal plan


## Analysis

Many heuristics achieve the optimal length under a second of calculation time. This is the greedy best first search which achieve the best result.


# Problem 2

## Introduction

## Initial states and goal
```
Init(At(C1, SFO) ∧ At(C2, JFK) ∧ At(C3, ATL) 
	∧ At(P1, SFO) ∧ At(P2, JFK) ∧ At(P3, ATL) 
	∧ Cargo(C1) ∧ Cargo(C2) ∧ Cargo(C3)
	∧ Plane(P1) ∧ Plane(P2) ∧ Plane(P3)
	∧ Airport(JFK) ∧ Airport(SFO) ∧ Airport(ATL))
Goal(At(C1, JFK) ∧ At(C2, SFO) ∧ At(C3, SFO))
```

## Results

### Non heuristics
| Search Method                            | Expansions    | Goal tests | New nodes | Plan length | Time spent  |
| -----------------------------------------|:-------------:|:----------:|:---------:|:-----------:| -----------:|
| breadth_first_search                     |  3343         | 4609       | 30509     | **9**       | 16.962      |
| breadth_first_tree_search                |  ABORTED      | ABORTED    | ABORTED   | ABORTED     | ABORTED     | 
| depth_first_graph_search                 |  624          | 625        | 5602      | 619         | 4.029       |
| depth_limited_search                     |  ABORTED      | ABORTED    | ABORTED   | ABORTED     | ABORTED     |
| uniform_cost_search                      |  4780         | 4782       | 43381     | **9**       | 52.526      |
| recursive_best_first_search              |  ABORTED      | ABORTED    | ABORTED   | ABORTED     | ABORTED     |
| greedy_best_first_graph_search           |  598          | 600        | 5382      | 17          | **3.982**   |

### Heuristics
| Search Method                            | Expansions    | Goal tests | New nodes | Plan length | Time spent  |
| -----------------------------------------|:-------------:|:----------:|:---------:|:-----------:| -----------:|
| astar_search with h_1                    |  4780         | 4782       | 43381     | **9**       | 52.049      |
| astar_search with h_ignore_preconditions |  1506         | 1508       | 13820     | **9**       | 16.628      |
| astar_search with h_pg_levelsum          |  **86**       | **88**     | **841**   | **9**       | 230.865     |

## Optimal plan

The heuristic a* with ignore preconditions is the one providing the optimal plan
```
Load(C1, P1, SFO)
Fly(P1, SFO, JFK)
Unload(C1, P1, JFK)
Load(C2, P2, JFK)
Fly(P2, JFK, SFO)
Unload(C2, P2, SFO)
Load(C3, P3, ATL)
Fly(P3, ATL, SFO)
Unload(C3, P3, SFO)
```

## Analysis



# Problem 3

## Initial states and goal
```
Init(At(C1, SFO) ∧ At(C2, JFK) ∧ At(C3, ATL) ∧ At(C4, ORD) 
	∧ At(P1, SFO) ∧ At(P2, JFK) 
	∧ Cargo(C1) ∧ Cargo(C2) ∧ Cargo(C3) ∧ Cargo(C4)
	∧ Plane(P1) ∧ Plane(P2)
	∧ Airport(JFK) ∧ Airport(SFO) ∧ Airport(ATL) ∧ Airport(ORD))
Goal(At(C1, JFK) ∧ At(C3, JFK) ∧ At(C2, SFO) ∧ At(C4, SFO))
```

## Results

| Search Method                            | Expansions    | Goal tests | New nodes | Plan length | Time spent  |
| -----------------------------------------|:-------------:|:----------:|:---------:|:-----------:| -----------:|
| breadth_first_search                     |  14663        | 18098      | 12963     | **12**      | 124.733     |
| breadth_first_tree_search                |  ABORTED      | ABORTED    | ABORTED   | ABORTED     | ABORTED     |
| depth_first_graph_search                 |  408          | 409        | 3364      | 392         | 2.035       |
| depth_limited_search                     |  ABORTED      | ABORTED    | ABORTED   | ABORTED     | ABORTED     |
| uniform_cost_search                      |  17882        | 17884      | 156769    | **12**      | 499.634     |
| recursive_best_first_search              |  ABORTED      | ABORTED    | ABORTED   | ABORTED     | ABORTED     |
| greedy_best_first_graph_search           |  4498         | 4500       | 39970     | 26          | 102.867     |
| astar_search with h_1                    |  55           | 57         | 224       | 6           | 0.054       |
| astar_search with h_ignore_preconditions |  41           | 43         | 170       | 6           | 0.081       |
| astar_search with h_pg_levelsum          |  11           | 13         | 50        | 6           | 2.122       |

## Analysis

Many heuristics achieve the optimal length under a second of calculation time. This is the greedy best first search which achieve the best result.
