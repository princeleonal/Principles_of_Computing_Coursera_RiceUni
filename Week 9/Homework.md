# Question 1
  A 4×4 puzzle in its solved configuration is shown below. Which configuration is the result of applying the move string "drdr" to the puzzle?

  ```python
  [0, 1, 2, 3,
   4, 5, 6, 7,
   8, 9, 10,11,
   12,13,14,15]
   ```

### Answer:

```python
[4, 1, 2, 3,
 5, 9, 6, 7,
 8, 10,0, 11,
 12,13,14,15]
```

----
# Question 2
  Which move string updates the puzzle from the configuration shown on the left to the configuration shown on the right?

  ```python
  [1, 2, 3, 7,         [5, 1, 2, 7,
   5, 4, 9, 6,          4, 8, 3, 6,
   8, 0, 10,11,         0, 9, 10,11,
   12,13,14,15]         12,13,14,15]
   ```
  
  Note that on the left, the tiles ten to fifteen are in their correct locations. On the right, tile nine has also been moved to its correct location.

### Answer:
    urullddruld

----
# Question 3
  For the next three problems, we will focus on exploring the behavior of a 2×2 puzzle. The size of the puzzle is passed to the initializer for the Puzzle class as a height and a width. Modify the last line of the template to create a 2×2 puzzle.
  
  Now, from the solved configuration, enter the move string "rdlu" repeatedly. How many times do you need to enter this string to return the puzzle to its solved configuration?

### Answer:
    3

----
# Question 4
  Starting from the configuration shown below, which move string returns the 2×2 puzzle to its solved configuration?
  
  ```python
  [0,2
   3,1]
   ```

### Answer:
    rdlu

----
# Question 5
  For configuration shown below, which of the following move strings return the puzzle to its solved configuration?

  ```python
  [0,3
  1,2]
  ```

### Answer:
    drul

----
# Question 6
  Which of the configurations below satisfy the invariant `lower_row_invariant(2, 1)`?

### Answer:

```python
--> [4, 1, 7, 2
     8, 6, 9, 3,
     5, 0, 10,11,
     12,13,14,15]

--> [8, 1, 2, 3
     4, 5, 11,10,
     8, 0, 9, 7,
     12,13,14,15]
```

----
# Question 7
  Which annotated execution trace captures the relationship between the solution method `solve_col0_tile` and the invariant `lower_row_invariant`? Remember that once the entire ith row is solved, the solution process then proceeds to the rightmost column of the i−1st row. You may assume that the puzzle is m×n.

### Answer:
    ...
    assert my_puzzle.lower_row_invariant(i, 0)
    my_puzzle.solve_col0_tile(i)
    assert my_puzzle.lower_row_invariant(i - 1, n -1)
    ...

----
# Question 8
  Starting from the configurations (given) on the right, which move string completes the solution process for this position and updates the puzzle to a configuration where `lower_row_invariant(3, 0)` is true?


### Answer:
    lddruld

----
# Question 9
  Which move string below updates the puzzle from the left configuration into the right configuration as given in the question?

### Answer:
    ruldrdlurdluurddlur

----
# Question 10
  Which move string below updates the left configuration into the right configuration as given in the question?

### Answer:
    urdlurrdluldrruld

----
