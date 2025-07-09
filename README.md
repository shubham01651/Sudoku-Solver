# 🧩 Sudoku Solver using Dancing Links (DLX) in C++

A high-performance, console-based Sudoku solver implemented in C++ using **Donald Knuth's Dancing Links (DLX)** algorithm to solve the Sudoku puzzle as an **Exact Cover Problem**.

## 🔧 Tech Stack
- **Language**: C++
- **Algorithm**: DLX (Dancing Links)
- **Approach**: Backtracking + Exact Cover Mapping
- **Memory Model**: Pointer-based linked list (no STL used)

## 📌 Features
- Transforms any standard 9×9 Sudoku puzzle into an **Exact Cover Problem** using principles of **Combinatorics** and **Boolean Algebra**.
- Implements **DLX** using a custom **toroidal doubly linked list** structure for fast column/row operations.
- Efficiently solves Sudoku puzzles of varying difficulty levels.
- Completely STL-free — low-level implementation with manual memory management and optimization.
- Clean console output of the solved Sudoku grid.

## 🧠 Algorithm Overview

The DLX algorithm is used to solve Exact Cover problems efficiently. In this project:

- The 9x9 Sudoku puzzle is transformed into a **Boolean constraint matrix** with 729 rows (9×9×9) and 324 columns (constraints for rows, columns, boxes, and cells).
- Each row in the matrix represents a possible assignment of a number to a cell.
- The matrix is converted into a **toroidal doubly linked list** for constant-time removal/restoration of rows and columns during backtracking.
- The recursive search algorithm explores possible placements and backtracks efficiently using the DLX technique.

## 🖥️ How to Run

1. **Compile the code:**
   ````bash
   g++ -o sudoku_solver sudoku_solver.cpp

2. **Run the executable:**
   ```bash
   ./sudoku_solver

3. **Input:**

   * Enter a 9×9 Sudoku grid in row-wise order, with `0` representing empty cells.

4. **Output:**

   * Prints the completed Sudoku solution if solvable.
   * Otherwise, displays `"No Solution Exists"`.
```markdown
## 📂 Sample Input
0 0 0 2 6 0 7 0 1
6 8 0 0 7 0 0 9 0
1 9 0 0 0 4 5 0 0
8 2 0 1 0 0 0 4 0
0 0 4 6 0 2 9 0 0
0 5 0 0 0 3 0 2 8
0 0 9 3 0 0 0 7 4
0 4 0 0 5 0 0 3 6
7 0 3 0 1 8 0 0 0

## ✅ Sample Output

4 3 5 2 6 9 7 8 1
6 8 2 5 7 1 4 9 3
1 9 7 8 3 4 5 6 2
8 2 6 1 9 5 3 4 7
3 7 4 6 8 2 9 1 5
9 5 1 7 4 3 6 2 8
5 1 9 3 2 6 8 7 4
2 4 8 9 5 7 1 3 6
7 6 3 4 1 8 2 5 9

## 🏗️ Project Structure
sudoku_solver.cpp      // Main source file
README.md              // Project documentation

## 📘 References

* [Donald Knuth - Dancing Links (DLX)](https://arxiv.org/pdf/cs/0011047.pdf)
* [Exact Cover Problem – Wikipedia](https://en.wikipedia.org/wiki/Exact_cover)

## 🙋‍♂️ Author

**Shubham Garg**
Passionate about algorithms, data structures, and problem-solving.
