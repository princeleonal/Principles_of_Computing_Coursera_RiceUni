# Question 1
  Review the math notes on the growth of functions. Which of the following functions grow at the same rate as (n^2)/2 - 5n + 20?

### Answer:
    n^2

----
# Question 2
  The fastest algorithms for sorting a list of size n share a bound (specified as a simple expression in n) for the minimal number of comparisons required to sort any list of length n.
  
  Use a web search engine (like Google) to look up this estimate and select the answer below that grows at the same rate as this expression.
  
### Answer:
    n log(n) comparisons

----
# Question 3
  Given a list of n three-letter words, which expression grows as the same rate as the number of statements executed during this sort? (Review practice activity on sorting strings)
  
### Answer:
    n

----
# Question 4
  Consider a stack in which we have performed n pushes followed by n pops. Which of the following are true statements concerning this sequence of operations?

### Answer:
* The last element pushed onto the stack is the first element popped off of the stack.
* The first element pushed onto the stack is the last element popped off of the stack.  

----
# Question 5
  Consider a queue in which we have performed nn enqueues followed by nn dequeues. Which of the following are true statements concerning this sequence of operations?

### Answer:
* The last element enqueued into the queue is the last element dequeued out of the queue.
* The first element enqueued into the queue is the first element dequeued out of the queue.

----
# Question 6
  Upon reviewing the provided code, Which of the following code fragments correctly computes `four_neighbors(row, col)` when the top/bottom rows and left/right columns are treated as being adjacent?
  
### Answer:
    up = (row - 1) % self._grid_height
    down = (row + 1) % self._grid_height
    left = (col - 1) % self._grid_width
    right = (col + 1) % self._grid_width
    return [[up, col], [down, col], [row, left], [row, right]]
    
----
# Question 7
  Consider the wildfire demo from lecture, which line in the implementation of `update_boundary` checks whether the fire can spread to an unburned cell?

### Answer:
    if self.is_empty(neighbor[0], neighbor[1]):
    
----
# Question 8
   Consider the case in which one steps through the entire breadth first search of the grid in the wildfire demonstration. Which of the following expressions grows at the same rate as the number of statements executed during this breadth first search? Assume the grid has size m-by-n.

### Answer:
    mn

----
# Question 9
  Modify the enqueue and dequeue methods in the provided code to behave like the push and pop methods for the Stack class. Then import it to the wildfire demo and run it. Add a single cell in the middle of the canvas to the boundary queue prior to starting the search. Which of the images below correspond to a possible state of the grid during the resulting depth first search?

### Answer:
![Option 1](/Principles_Of_Computing_Coursera_RiceUni/Week 6/Images/1.jpg)

