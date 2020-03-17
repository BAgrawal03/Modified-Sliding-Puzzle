# Modified-Sliding-Puzzle
Finds the optimal path to variations of the traditional sliding puzzle


## The Luddy puzzle 

Initial State - The state provided as an input

Goal State - A grid where the numbers are arranged sequentially with 0(blank tile) at the end.

State Space - A list of all the configurations the state can take up.

Successors - The configurations that can follow a current state with the valid possible moves. It would vary depending on the variations - original, circular and luddy.

Cost Function - Initially, the code worked on Manhattan distance as a cost function only. But, this cost function did not prove to be very effective for luddy so we used the number of mispaced tiles and that worked far better for luddy but was slower on original and circular variations. So, we decided to use Manhattan distance for the latter versions.

Search Algorithm - We have implemented the search algorithm #3 discussed in the class to solve this problem. We need to find out the solution to a 15 puzzle problem with slightly modified rules. The first case, however works on the typical rules of the game. Out first step was to check whether the puzzle is solvable or not. The function isSolvable() in the program is for the same. For the second case, we introduced the extra moves which are allowed for the circular moves. If the circular moves are allowed, all the blocks in the puzzle get 4 possible moves - unlike in the original one. The third case is similar to how a knight moves on a chess board. We defined the moves of the puzzle

Potential Issues - The Luddy version does not always give the solution within the time limits.

Code Fix - A better solution would be to use heuristic to be a combination of Manhattan distance and linear inversions for Luddy.
