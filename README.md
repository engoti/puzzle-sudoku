# Sudoku Solver in Go

## Overview
This is a Go-based Sudoku solver that takes a partially completed 9x9 Sudoku puzzle as input and attempts to solve it using a backtracking algorithm. If the puzzle is solvable, it prints the solution; otherwise, it returns an error message.

## Features
- Parses input from the command line
- Validates Sudoku constraints
- Uses backtracking to find a valid solution
- Prints the solved Sudoku board

## Installation
To use this Sudoku solver, you must have Go installed on your system. You can download and install Go from [here](https://go.dev/dl/).

## Usage
### Compiling the Program
```sh
go build -o puzzle-sudoku
```

### Running the Solver
```sh
./puzzle-sudoku "53..7...." "6..195..." ".98....6." "8...6...3" "4..8.3..1" "7...2...6" ".6....28." "...419..5" "....8..79"
```
Each string represents a row in the Sudoku puzzle, with '.' indicating an empty cell.

### Example Input
```
53..7....
6..195...
.98....6.
8...6...3
4..8.3..1
7...2...6
.6....28.
...419..5
....8..79
```

### Example Output (Solved Sudoku)
```
5 3 4 6 7 8 9 1 2
6 7 2 1 9 5 3 4 8
1 9 8 3 4 2 5 6 7
8 5 9 7 6 1 4 2 3
4 2 6 8 5 3 7 9 1
7 1 3 9 2 4 8 5 6
9 6 1 5 3 7 2 8 4
2 8 7 4 1 9 6 3 5
3 4 5 2 8 6 1 7 9
```

## Code Explanation
- `checkErrors(arr []string) bool`: Ensures the input follows the correct format.
- `optimizeSudoku(arr []string) [][]int`: Converts the input strings into a 2D integer slice.
- `solveSudoku(arr *[][]int, length int) bool`: Implements the backtracking algorithm to solve the puzzle.
- `printSudoku(arr [][]int)`: Prints the Sudoku board.
- `isCorrect(arr [][]int, row int, column int, num int) bool`: Checks if a number can be placed in a specific position.
- `checkRow`, `checkColumn`, `checkSubSudoku`: Helper functions for Sudoku validation.
- `runeToInt(number rune) int`: Converts rune characters to integers.

## License
This project is open-source and free to use under the MIT License.

## Contributions
Contributions and improvements are welcome! Feel free to submit a pull request.

## Author
Developed by Engel Samuel Otieno

