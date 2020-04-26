# Question 1
  Use the function `run_simulations` in the greedy boss simulator (given in practice activity) to plot the graph of total salary earned as a function of the number of days for `bribe_cost_increment`= 0,500,1000,2000. Which value for `bribe_cost_increment` generates the fastest growth in total salary earned in the simulation?

### Answer:
    0.

----
# Question 2
  One scenario that the greedy boss simulator does not cover is the situation when you refuse to accept a bribe. Which of the following arithmetic sums evaluates to your total salary earned after d days?
  
### Answer:
    100 + 100 + 100 + . . . + 100 + 100 (with d terms in sum).
    
----
# Question 3
  Reduce the arithmetic sum that you selected in Question 2 to a polynomial expression in the number of days d using the rules for arithmetic sums.
  
### Answer:
    d*100
    
----
# Question 4
  For the next three problems, we will consider the case when `bribe_cost_increment`= 1000. First, convert the output of into Log/Log form by taking the logarithm of both `current_day` and the `total salary` earned using `math.log()` before they appended to the list `days_vs_earnings`.

The plot of the resulting graph approaches a straight line as the number of days increase. This observation signals that the function might be a polynomial function. Compute the slope of this line and round it to the nearest integer to estimate the degree of this polynomial.

### Answer:
    2
    
----
# Question 5
  Examine the output of the simulation `greedy_boss(50,1000)`. Note you accumulate enough savings to pay a bribe once every 10 days.

Which of the arithmetic sums below evaluates to the total salary earned after n bribes?

### Answer:
    1000 + 2000 +3000 + . . . + 1000n
    
----
# Question 6
  Reduce the arithmetic sum that you selected in Question 5 to a closed-form expression in n using the rules for arithmetic sums specified in the class. This expression should relate total salary earned to the number of bribes. Finally, use the fact that each bribe happens once every 10 days to derive a polynomial expression that approximates the total salary earned in terms of the number of days d.
  
### Answer:
    5*d^2+50*d
    
----
# Question 7
  The next two questions will examine the case when the cost of a bribe does not increase, `bribe_cost_increment` = 0. Our first task is to check whether the total salary earned is a polynomial function of the number of days in this case. To this end, create a Log/Log plot of the output of `greedy_bos`s and examine the resulting graph.

Does the graph approach a straight line as the number of days increases?

### Answer:
    No, The graph does not approach a straight line.
    
 ----
 # Question 8
   To conclude our analysis of this case, we will do some manual experimentation to locate an expression in dd that grows at a similar rate to total salary earned when `bribe_cost_increment`= 0.

Compare the growth rates of the expressions below to the growth rate of total salary earned using the plotting technique described in the Math notes. Which expression grows at approximately the same rate as total salary earned?

### Answer:
    e^(0.095*d)
    
----
# Question 9
  Each upgrade in Cookie Clicker costs 15% more than the cost of the previous upgrade.If the first upgrade costs one unit, enter a math expression that models the cost of the nth upgrade.
   
### Answer:
    1.15^(n-1)
    
----
# Question 10
  For the case when`bribe_cost_increment` = 1000, the cost of the nnth bribe was exactly 1000n. Which expression in nn grows faster 1000n or your answer to question 9?
  
### Answer:
    The cost of upgrades grows faster than in the greedy boss scenario. Therefore, the total cookies generated in this
    version grows at rate that is bounded by a quadratic function.

----
# Question 11
  To complete this problem, visit the link given (OwlTest page) and follow the directions for creating and submitting a list of test cases. Once OwlTest has successfully assessed your test case, you will see the message `TEST CASES successfully assessed`.Following this message is a seven-digit number that you should enter in the form below.
  
### Answer:
    3036296
    
### Code:
    TEST_CASES = [[2], [2, 0],
                  [2,2,2,2],[4,4,4,4],[2,4,8,8],
                  [2,16,16,16],[1024,1024,1024,1024],
                  [2,2,4,8],[8,4,2,4],[4,8,32,16]]
