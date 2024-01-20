# Parallel Heuristic Sudoku Solver

This Python script provides a CLI Sudoku puzzle generator and solver with an improved backtracking algorithm. It introduces parallelism and heuristics to enhance the solving process, making it faster and more efficient.

The initial version of this solver is available in a separate repository, [Sudoku Solver with Backtracking](https://github.com/AswinPKumar01/Sudoku-Solver).

An updated Sudoku Solver with GUI can be accessed [here](https://github.com/AswinPKumar01/Sudoku-Solver-with-GUI).

## Performance Improvement

- **Parallel Execution:**
  - Utilizing ThreadPoolExecutor, the optimized solver concurrently explores possible solutions, significantly reducing solving time.
  - Effectively leverages multi-core systems, distributing the computational load and accelerating the solving process.

- **Heuristic Strategies:**
  - The incorporation of heuristics intelligently guides the search for a solution, prioritizing empty cells with fewer valid moves.
  - Strategically reduces the overall search space, enhancing efficiency and expediting the Sudoku-solving experience.

- **Noticeable Reduction in Solving Time:**
  - Particularly evident when solving larger puzzles or those with higher difficulty levels.
  - Users will experience a remarkable improvement in solving times compared to the original non-optimized implementation.

## Parallelism and Heuristics

### Parallelism

Parallelism, on the other hand, involves the simultaneous execution of multiple processes or threads to improve computational efficiency. It harnesses the power of multiple cores or processors to execute tasks concurrently, enabling faster completion of complex computations. In Sudoku solving, parallelism can be leveraged to explore different possibilities simultaneously, significantly accelerating the search for a valid solution. This parallel approach is particularly advantageous on modern, multi-core systems, where it can distribute the computational load across multiple processors for quicker results.

![image](https://github.com/AswinPKumar01/Sudoku-Optimized/assets/118362715/9f9445bb-956c-418e-a5a8-42b5d6644d52)

_(Paralellism demo from Princeton Research)_


The improved algorithm introduces parallelism using Python's ThreadPoolExecutor. The `DynamicParallelSudokuSolver` function concurrently explores possible solutions, significantly speeding up the solving process. This enhances the solver's performance, particularly on multi-core systems.

### Heuristics

Heuristics is a problem-solving approach that employs practical and intuitive techniques to quickly find approximate solutions, especially when dealing with complex and computationally demanding tasks. Unlike rigorous algorithms, heuristics prioritize speed and efficiency, often sacrificing optimality. In the context of Sudoku solving, heuristics can be applied to intelligently guide the search for a solution, such as prioritizing empty cells with fewer valid moves, thereby reducing the overall computational burden.

![](https://miro.medium.com/v2/resize:fit:1280/1*5O_0y-3B7n_1eEI833H8MA.gif)

_(Simple heuristics for TSP by Robert Kübler)_


In this program, heuristics play a crucial role in identifying promising moves, reducing the search space and enhancing the efficiency of the algorithm. The `heuristic_find_empty_cell` function prioritizes empty cells based on the number of valid moves, improving the solver's decision-making process.

## Acknowledgments
- Sincere appreciation to the authors of research papers and documentations on Algorithm Optimization, Parallelism, and Heuristics for their valuable insights. 
