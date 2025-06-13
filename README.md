# AI-Based Pathfinding and Parkinson's Disease Detection

This repository contains two key phases of an AI project:

1. **Pathfinding Algorithm Performance Analysis** using classical and metaheuristic search strategies.
2. **Q-Learning Implementation** for autonomous navigation in a grid environment.

---

## Phase I: Search Algorithms Performance Analysis

### Objective
To evaluate and compare the performance of various search algorithms in a grid-based delivery task involving path planning through obstacles.

### Problem Setup
- **Grid:** 30x30 with random obstacles and 3 delivery goals.
- **State Representation:** Includes robot position and delivery status.
- **Actions:** Move in four directions and deliver at goal positions.
- **Goal:** Visit all delivery points.

### Algorithms Implemented
- Breadth-First Search (BFS)
- Depth-First Search (DFS)
- Uniform Cost Search (UCS)
- Iterative Deepening Search (IDS)
- A* Search
- Greedy Best-First Search
- Hill Climbing
- Simulated Annealing
- Genetic Algorithm

### Performance Metrics
- Execution Time
- Memory Usage
- Path Length
- Success Rate

### Key Insights
- **A\*** offered the best balance of performance and optimality.
- **BFS and UCS** reliably found optimal paths but were resource-intensive.
- **DFS and IDS** were fast but often produced suboptimal or long paths.
- **Greedy, Hill Climbing, Genetic, and Simulated Annealing** struggled with either inefficiency or inconsistency due to the random nature of the environment.

---

## Phase II: Reinforcement Learning with Q-Learning

### Objective
Train an agent using Q-Learning to navigate an 8x8 grid with static obstacles and reach randomly placed goals.

### Environment
- Start Position: Top-left corner.
- Obstacles: Randomly placed, impassable.
- Goals: Randomly placed in valid positions.

### Q-Learning Setup
- **Actions:** Move North, South, East, West
- **Rewards:**
  - +ve for reaching the goal
  - -ve for hitting obstacles or invalid moves
- **Hyperparameters:**
  - Alpha (Learning Rate): 0.1
  - Gamma (Discount Factor): 0.99
  - Epsilon (Exploration): Decayed over time
  - Episodes: 500

### Results Summary
- **Average Reward/Episode:** 201.70
- **Max Reward:** 285.55
- **Min Reward:** -258.80
- **Final Path Length:** 15
- **Q-Value Evolution:** Steady improvement, final average ≈ 16.38

### Final Learned Path:
```python
['E', 'S', 'S', 'S', 'E', 'S', 'S', 'S', 'E', 'E', 'E', 'E', 'E', 'E', 'S']



 References

    AI textbook resources on classical search and reinforcement learning.

    Open-source implementations of heuristic and genetic algorithms.

    Research on Q-Learning and path planning.

 Conclusion

This project demonstrates how classical AI search algorithms and modern reinforcement learning approaches can be applied to navigate complex environments. The two phases collectively showcase the strengths and limitations of each method under different problem settings.
