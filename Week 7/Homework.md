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
  If n is non-negative integer, enter a math expression in n for the value returned by `add_up(n)`.

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
# Question 5
  The number of recursive calls to `fib` in the Q4 grows quite quickly. The issue is that `fib` fails to "remember" the values computed during previous recursive calls. One technique for avoiding this issue is memoization, a technique in which the values computed by calls to `fib` are stored in an auxiliary dictionary for later use.
  
  The Python function below uses memoization to compute the Fibonacci numbers efficiently.
  ```python
  def memoized_fib(num, memo_dict):
    if num in memo_dict:
        return memo_dict[num]
    else:
        sum1 = memoized_fib(num - 1, memo_dict)
        sum2 = memoized_fib(num - 2, memo_dict)
        memo_dict[num] = sum1 + sum2
        return sum1 + sum2
  ```
  If n > 0, how many call to `memoized_fib` are computed during the evaluation of the expression `memoized_fib(n, {0 : 0, 1 : 1})`? Enter the answer as a math expression in n below. You may want to add a global counter to the body of `memoized_fib` keeps track of the number of calls.

### Answer:
    2*n - 1

----
# Question 6
  In a previous homework, we implemented an iterative method for generating permutations of a set of outcomes. Permutations can also be generated recursively.
  
  Given a list `outcomes` of length n, we can perform the following recursive computation to generate the set of all permutations of length n:
  * Compute the set of permutations `rest_permutations` for the list `outcomes[1 :]` of length n−1,
  * For each permutation `perm` in `rest_permutations`, insert `outcome[0]` at each possible position of `perm` to create permutations of length n,
  * Collect all of these permutations of length n into a set and return that set.

If p(n) is the number of permutations returned by this method, what recurrence below captures the behavior of p(n)?

### Answer:
    p(0) = 1
    p(n) = n p(n-1)

----
# Question 7
  Using the math notes for recurrences, look up the solution to the recurrence from Q6. Enter the solution to this recurrence (as given in the notes) as a math expression in n below.

### Answer:
    n!

----
# Question 8
  As part of this week's mini-project, you will implement a function `merge(list1, list2)` that takes two ordered lists and merges the lists into a single ordered list that contains all of the elements in either `list1` and `list2`.
  
  The body of `merge` consists of a `while` loop that iterates until one of the lists `list1` and `list2` is empty. Each iteration of the loop compares the first element in each list, pops the smaller element from its containing list and appends this element to the answer. Once one list is exhausted, the entries in the remaining list are appended to the answer.
  
  If `list1` and `list2` are both of length n, which expression below grows at the same rate as the running time (i.e; the number of Python statements executed) of `merge`?

### Answer:
    n

----
# Question 9
  Another part of this week's mini-project will be implementing a recursive sorting algorithm known as `merge_sort`. The basic idea behind `merge_sort` is to split the unordered input list of size n into two unordered sub-lists of approximately size n/2, recursively call `merge_sort` to sort each of these sublists and, finally, use `merge` to merge these two sorted sublists.
  
  If t(n) corresponds to the running time of `merge_sort` as a function of the input list size n, which recurrence below captures the behavior of t(n) most accurately?

### Answer:
    t(1) = 1
    t(n) = 2t(n/2) + n

----
# Question 10
  Use the math notes for recurrences and look up the approximate solution to the recurrence for `merge_sort` from Q9. Select the solution to this recurrence as an expression in nn below.

### Answer:
    n log(n)

----
