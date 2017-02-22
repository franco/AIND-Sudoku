# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: For the sudoku problem constraint propagation is used to reduce the 
search space of the algorithm by applying different strategies to eliminate
possible values from boxes. One such strategy is the naked twins strategy,
which looks for two boxes in the same unit (same row, same column or 
same 3x3 square) that both have the same two possible digits. If found,
it is unclear which of the two possible digits goes in which of the two boxes,
but the two digits are locked in and therefore every occurrence of one or both
of those digits in any other box within the same unit can be eliminated.
This elimination of possible values reduces the search space. 

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: With a diagonal sudoko there is an additional rule that each digit 1-9 can only 
appear once along its two diagonals. This additional rule helps many strategies
like elimination strategy or 'only choice' strategy to find potentially additional digits
to eliminate as those strategies can be applied also for the diagonals. And this in
turn helps to eliminate the search space quicker. So the applied strategies stay
the same, but in a diagonal sudoko the constraint propagation strategies might
be more efficient. 

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Data

The data consists of a text file of diagonal sudokus for you to solve.