# sudoku
#### Video Demo:  <URL https://youtu.be/ZlBlzesno7U>
#### Description:

This C program is an implementation of a Sudoku solver using a backtracking algorithm. The goal of the program is to solve a partially filled Sudoku grid, where the numbers 1 through 9 must be placed in each row, each column, and each of the 3x3 subgrids without repetition.

Here's a brief explanation of the key functions and the overall flow of the program:

checkrow, checkcolumn, checkgrid functions:

These functions check if a given number num can be placed in the specified row, column, or 3x3 grid without violating the Sudoku rules.
They return 1 if the number can be placed and 0 otherwise.

navigate function:

This function is responsible for moving to the next cell in the Sudoku grid.
It increments the column if the end of the row is not reached, otherwise, it moves to the next row.

show function:

This function prints the solved Sudoku grid.

solvesudoku function:

This is the main recursive backtracking function.
It first checks if the entire grid has been processed (row > 8), in which case it calls the display function to print the solution.
If the current cell is not empty (sudoku[row][column] != 0), it moves to the next cell using the navigate function.
If the current cell is empty, it tries placing numbers 1 through 9 in the cell using a loop.
If placing a number is valid according to the rules, it sets the cell to that number and recursively calls itself for the next cell.
If the recursive call returns, it means the current placement did not lead to a solution, so it backtracks by resetting the cell to 0.

main function:

It takes input for the initial Sudoku grid, where 0 represents an unknown entry.
It then calls the solvesudoku function with the initial cell (0, 0) to start solving the Sudoku.
The backtracking algorithm explores different possibilities for each cell until a solution is found. If a placement violates the Sudoku rules, it backtracks and tries a different number. The process continues until a valid solution is found, or all possibilities are exhausted.

Introduction:

Hello, everyone. Today, I'm excited to walk you through a C program designed to solve Sudoku puzzles using a backtracking algorithm. Sudoku is a number-placement puzzle, and this program demonstrates a method for finding solutions.

The program is organized into several functions.

checkrow, checkcolumn, checkgrid functions determine if a given number can be legally placed in a particular row, column, or 3x3 grid. They return 1 if the placement is valid and 0 otherwise.

navigate function facilitates the movement through the Sudoku grid. It decides whether to move to the next column or the next row, depending on the current position.
Show function prints the solved Sudoku grid. It's called when the entire puzzle has been successfully solved.
solvesudoku function is the heart of the program, implementing a recursive backtracking algorithm.
It checks if the entire grid has been processed. If yes, it calls show to display the solution.
If the current cell is not empty, it navigates to the next cell.
If the cell is empty, it tries placing numbers 1 through 9, and if valid, it recursively calls itself for the next cell. If the recursive call returns, indicating failure, it backtracks by resetting the cell to 0.

The main function takes input for the initial Sudoku grid, where 0 represents unknown entries.
It then calls the solvesudoku function with the initial cell (0, 0) to kickstart the Sudoku-solving process.
Conclusion:

In summary, this program showcases an elegant solution to the Sudoku puzzle using a backtracking algorithm. It explores possibilities, backtracks when necessary, and ultimately arrives at a valid solution. Feel free to experiment with different Sudoku puzzles and observe how the program efficiently navigates through the logical constraints of the game. Thank you for your attention, and I'm happy to answer any questions you may have.
