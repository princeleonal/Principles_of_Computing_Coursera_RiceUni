# Question 1
  Examine the behavior of the recursive program that models the story of the "Cat in the Hat" by Dr. Suess. How many calls to the function `clean_up` are made by the program?

### Answer:
    28.

----
# Question 2
  Consider the following Python function:
  ```python
  def add_up(n):
    if n == 0:
        return 0
    else:
        return n + add_up(n - 1)
  ```
  If nn is non-negative integer, enter a math expression in n for the value returned by `add_up(n)`.

### Answer:
    (n*(n+1))/2

----
# Question 3
  Consider the following Python function:
  ```python
  def multiply_up(n):
    if n == 0:
        return 1
    else:
        return n * multiply_up(n - 1)
  ```

### Answer:
    n!

----
# Question 4
  Consider this recursive Python function that computes the Fibonacci numbers below:
  ```python
  def fib(num):
    if num == 0:
        return 0
    elif num == 1:
        return 1
    else:
        return fib(num - 1) + fib(num - 2)
  ```
  Let f(n) be the total number of calls to the function `fib` that are computed during the recursive evaluation of `fib(n)`. Which recurrence reflects the number of times that `fib` is called during this evaluation of `fib(n)`?
  
  You may want to add a global counter to the body of `fib` that records the number of calls for small values of n.

### Answer:
    f(0) = 1
    f(1) = 1
    f(n) = f(n-1) + f(n-2) + 1

----
