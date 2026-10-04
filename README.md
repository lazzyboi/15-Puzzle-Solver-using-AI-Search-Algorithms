# 15-Puzzle Solver using AI Search Algorithms

A Python-based Artificial Intelligence project that solves the **15-Puzzle problem** using multiple uninformed and informed search algorithms.

The project represents the puzzle as a state-space search problem and compares different search strategies based on solution depth, processed nodes, memory usage, and execution time.

## Project Overview

The 15-Puzzle consists of a 4×4 grid containing numbered tiles from `1` to `15` and one empty space represented by `0`.

The objective is to transform a scrambled puzzle into the goal state:

```text
1   2   3   4
5   6   7   8
9  10  11  12
13  14  15   0
```

The program explores possible states until it reaches the goal configuration.

## Search Algorithms Implemented

The project implements the following search algorithms:

- Breadth-First Search
- Depth-First Search
- Uniform Cost Search
- Depth-Limited Search
- Iterative Deepening Search
- Greedy Best-First Search
- A* Search

## Heuristic

For informed search algorithms, the project uses the **Manhattan Distance** heuristic.

The Manhattan distance measures how far each tile is from its target position based on horizontal and vertical movement.

A* uses:

```text
f(n) = g(n) + h(n)
```

where:

- `g(n)` = cost from the initial state
- `h(n)` = Manhattan distance heuristic
- `f(n)` = estimated total cost

## Features

- 15-Puzzle state representation using NumPy arrays
- Automatic solvability checking
- Random solvable puzzle generation
- State expansion
- Parent-child state relationships
- Solution path reconstruction
- Multiple AI search strategies
- Manhattan distance heuristic
- Node processing statistics
- Maximum frontier size tracking
- Execution-time measurement

## Project Structure

```text
15-Puzzle-Solver/
│
├── AI.py
├── README.md
├── Batch_file.xlsx
└── Report.pdf
```

### `AI.py`

Contains the complete implementation of:

- Puzzle states
- Search tree nodes
- State expansion
- Search algorithms
- Heuristic functions
- Solvability checking
- Solution reconstruction
- Performance statistics

### `Batch_file.xlsx`

Contains project-related data/results used during development and evaluation.

### `Report.pdf`

Contains the project's academic documentation and analysis.

## Requirements

- Python 3.x
- NumPy

Install NumPy using:

```bash
pip install numpy
```

## Running the Project

Run:

```bash
python AI.py
```

The program will ask you to choose a search algorithm:

```text
Choose an algorithm [Breadth first, Depth first, Uniform cost,
Depth limited, Iterative deepening, Greedy, A*]
```

Example:

```text
A*
```

For Depth-Limited Search, the program additionally asks for a search depth limit.

## Output

After execution, the program reports:

```text
Time taken
G-value
Processed nodes
Max stored nodes
Whether a solution was found
Solution sequence
Solution state
```

Example output format:

```text
---------- Output Information ----------
Time taken: ...
G-value (level solution found in goal tree): ...
Processed nodes: ...
Max stored nodes: ...
Do we find solution: True
Solution: [...]
Solution state:
[...]
```

## Puzzle Solvability

Not every 15-Puzzle configuration can be solved.

The program calculates the number of inversions and the blank-tile position to determine whether a generated or supplied configuration is solvable.

Random puzzle generation therefore produces only solvable states.

## Custom Puzzle

The program currently contains a predefined 4×4 puzzle:

```python
initial = [
    [14, 15, 3, 4],
    [10, 6, 7, 13],
    [9, 0, 5, 11],
    [12, 8, 2, 1]
]
```

This state can be modified inside `AI.py` to test different configurations.

## Technologies Used

- Python
- NumPy
- Artificial Intelligence
- State-Space Search
- Heuristic Search
- Graph Search
- A* Search

## Learning Objectives

This project demonstrates practical implementation of:

- State-space representation
- Search trees
- Uninformed search
- Informed search
- Heuristic functions
- A* algorithm
- Puzzle solvability
- Solution-path reconstruction
- Search algorithm performance comparison

## Limitations

The current implementation is primarily designed as an academic demonstration of AI search algorithms. Very difficult 15-Puzzle states can require significant processing time and memory, especially for uninformed search strategies.

The puzzle configuration and selected algorithm are currently controlled through the Python source and command-line interaction rather than a graphical interface.

## Academic Project

This project was developed as an Artificial Intelligence project to study and compare classical search algorithms through the 15-Puzzle problem.
