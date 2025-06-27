# Rubik's Cube Solver

A C++ implementation of a Rubik's Cube solver using Korf's IDA* (Iterative Deepening A*) algorithm combined with a heuristic-based approach. The project utilizes a graph-based data structure to represent cube states and efficiently search for the optimal solution.

---

## Features

- Solves a standard 3x3x3 Rubik's Cube.
- Implements Korf's IDA* algorithm for optimal solving.
- Uses heuristic functions to guide the search.
- Models cube states using a graph data structure.
- Efficient state exploration and pruning.
- Modular and clean C++ code structure.

---

## Algorithm Explanation

### Korf's IDA* Algorithm
- A variant of A* search optimized for memory efficiency.
- Performs iterative depth-first searches with increasing cost thresholds.
- Combines the benefits of DFS (low memory) and A* (optimality).

### Heuristic Used
- The heuristic estimates the minimum number of moves required to reach the solved state.
- The heuristic is admissible (never overestimates), making IDA* optimal.
- Examples of heuristic techniques:
  - Pattern Databases
  - Manhattan Distance on Facelets
  - Corner & Edge orientation & permutation checks

### Graph Structure
- Each node represents a unique Rubik's Cube state.
- Edges represent valid moves (rotations of cube faces).
- Efficient hashing for cube states to avoid revisits.