# Sudoku
A logic-based, combinatorial number-placement puzzle.<br>

<h3>Research Objective<br>
  
To solve Sudoku games using a backtracking algorithm in C language. This is a part of the CLATP 4 component for the subject 18AIC202J-Data Structure And Its Application.
  
<h3>Requirements<br>
<li>Personal Laptop (P.C): A personal computer can be defined as an end-point of connection which will connect with the computer network<br>
<li>Software/Coding Platform: We used GDB, an online compiler to build the sudoku game.<br>
  
<h3>Theory<br>
Sudoku is a logic-based, combinatorial number-placement puzzle. The objective is to fill a 9×9 grid with digits so that each column, each row, and each of the nine 3×3 subgrids that compose the grid contain all of the numbers from 1 to 9.<br>

Backtracking can be defined as a general algorithmic technique that considers searching every possible combination in order to solve a computational problem. It is an algorithmic technique for solving problems recursively by trying to build a solution incrementally, one piece at a time, removing those solutions that fail to satisfy the constraints of the problem at any point in time (by time, here, is referred to the time elapsed till reaching any level of the search tree).  Backtracking can also be said as an improvement to the brute force approach. So basically, the idea behind the backtracking technique is to search for a solution to a problem among all the available options. <br>
  
Like all other Backtracking problems, Sudoku can be solved by assigning numbers one by one to empty cells. Before assigning a number, check whether it is safe to assign. Check that the same number is not present in the current row, current column and current 3X3 subgrid. After checking for safety, assign the number, and recursively check whether this assignment leads to a solution or not. If the assignment doesn’t lead to a solution, then try the next number for the current empty cell. And if none of the numbers (1 to 9) leads to a solution, return false and print no solution exists.<br>
  
<h3>Algorithm<br>
1. We will fill the cells column-wise.<br>
2. For every cell, we will check if it is empty (or has 0) or not.<br>
3. If the cell is empty, we will then check which number from 1 to 9 is valid for the particular cell and update the cell accordingly.<br>
4. If the current cell is not empty, we will move to the next cell of the same column or the first row of the next column if at the last cell of the column.<br>
5. If none of the numbers from 1 to 9 is valid for the current cell, we will go back to the last updated cell and try with another good value (i.e. backtrack). <br>
6. To achieve backtracking, we will return to the last recursive call by returning “FALSE” check with the next value of the iteration of ‘for loop’. We again proceed to the next cell after updating the last cell with another valid value.<br>
  
<h3>Modules Used<br>
<b>State-space tree: <br>
A space tree is a tree that represents all of the possible states of the problem from the root as an initial state to the leaf as a terminal state. Each branch represents a variable and each level represents a solution. This design is able to establish reasoning about the tendencies of the given system, to be able to find relationships and correlations among the different states. This concept can be applied to many different aspects including theory testing, intelligence testing, and games. However, it is important to keep in mind that a space tree is hypothetical to some degree, meaning the results are not necessarily provable.
Implementation<br>

<h3>Conclusion<br>
Time complexity: O(9^(n*n)).  The element that needs to fit in a cell will come earlier as we fill almost filled elements first, which will help in fewer recursive calls. So the time taken will be much less than the naive approaches but the upper bound time complexity remains the same.
Auxiliary Space: O(n*n).  A graph of the remaining positions to be filled for the respected elements is created.
This project can also be solved in other programming languages like Java, C++, etc.  Using other languages increases the speed of execution and eases the programming semantics.
  
<h3>References<br>
<a href="https://www.geeksforgeeks.org/sudoku-backtracking-7/">https://www.geeksforgeeks.org/sudoku-backtracking-7/</a><br>
<a href="https://www.geeksforgeeks.org/introduction-to-backtracking-data-structure-and-algorithm-tutorials/">https://www.geeksforgeeks.org/introduction-to-backtracking-data-structure-and-algorithm-tutorials/<\a><br>
<a href="https://pencilprogrammer.com/algorithms/sudoku-using-backtracking/">https://pencilprogrammer.com/algorithms/sudoku-using-backtracking/<\a><br>
<a href="https://www.simplilearn.com/tutorials/data-structure-tutorial/backtracking-algorithm">https://www.simplilearn.com/tutorials/data-structure-tutorial/backtracking-algorithm<\a><br>
