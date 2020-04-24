# Question 1
  Given the set of outcomes corresponding to a coin flip,{Heads,Tails}, how many sequences of outcomes of length five (repetition allowed) are possible?

### Answer:
    32  (2^5 = 32)
    
----
# Question 2
  Consider a sequence of trials in which a fair four-sided die (with faces numbered 1-4) is rolled twice. What is the expected value of the product of the two die rolls? Enter the answer as a floating point number below.
  
### Answer:
    6.25
    
----
# Question 3
  Given a trial in which a decimal digit is selected from the list ["0","1","2","3","4","5","6","7","8","9"] with equal probability 0.1, consider a five-digit string created by a sequence of such trials (leading zeros and repeated digits are allowed). What is the probability that this five-digit string consists of five consecutive digits in either ascending or descending order (eg."34567" or "43210")?

  Enter your answer as a floating point number with at least four significant digits of precision.
  
### Answer:
    0.0001200
    (Each outcome has probability 0.00001. There are six strings with consecutive ascending digits and six string 
     with consecutive descending digits. Therefore, the probability of this event is 0.00012.)
     
----
# Question 4
  Consider a trial in which five digit strings are formed as permutations of the digits ["0","1","2","3","4","5","6","7","8","9"]. (In this case, repetition of digits is not allowed.) If the probability of each permutation is the same, what is the probability that this five digits string consists of consecutive digits in either ascending or descending order (eg."34567" or "43210") ?

  Enter your answer as a floating point number with at least four significant digits of precision.

### Answer:
    0.0003968
    There are 12 possible permutations out of 10!/5! permutations that are either ascending or descending.
    
----
# Question 5
  In this week's lectures, we discussed an iterative approach to generating all sequences of outcomes where repeated outcomes were allowed. Implement a function `gen_permutations(outcomes,num_trials)` that takes a list of outcomes and a number of trials and returns a set of all possible permutations of length `num_trials` (encoded as tuples) from the set of `outcomes`.
  
### Answer:
    ('b','e','c','d')

### Code:
    
    def gen_permutations(outcomes, length):
        """
        Iterative function that generates set of permutations of
        outcomes of length num_trials
        No repeated outcomes allowed
        """
        answer_set = set([()])
        for dummy_idx in range(length):
            temp_set = set()
            for partial_sequence in answer_set:
                for item in outcomes:
                    new_sequence = list(partial_sequence)
                    new_sequence.append(item)
                    if dummy_idx == 1 and new_sequence[0] == new_sequence[1]:
                        continue
                    elif dummy_idx == 2 and (new_sequence[1] == new_sequence[2] 
                                             or new_sequence[0] == new_sequence[2]):
                        continue
                    elif dummy_idx == 3 and (new_sequence[0] == new_sequence[3] 
                                             or new_sequence[1] == new_sequence[3]
                                             or new_sequence[2] == new_sequence[3]):
                        continue    
                    temp_set.add(tuple(new_sequence))
            answer_set = temp_set
        return answer_set

    outcome = set(["a", "b", "c", "d", "e", "f"])

    permutations = gen_permutations(outcome, 4)
    permutation_list = list(permutations)
    permutation_list.sort()
    print
    print "Answer is", permutation_list[100]

----
# Question 6
  Which of the following sets are subsets of the set {1,2}?

### Answer:
    {}
    {1,2}
    {1}
    
----
# Question 7
  If the set T has n members, how many distinct sets S are subsets of T?
  
### Answer:
    2^n
    
----
# Question 8
  Given a standard 52 card deck of playing cards, what is the probability of being dealt a five card hand where all five cards are of the same suit?
  
### Answer:
    0.0019807923
    There are 13!/5!8! possible hands with 5 cards in a single suit. Multiply this value by the number of suits (4)
    and divide by the 52!/5!47! possible hands.
    
----
# Question 9
  Enter a math expression in `m` and `n` using factorial (!) that represents the value of the nth entry of the mth row of Pascal's triangle. (Both the row numbers and entry numbers are indexed starting at zero.)

### Answer:
    m! / n!(m-n)!
    
----
# Question 10
  To complete this problem, visit the link given (OwlTest page) and follow the directions for creating and submitting a list of test cases. Once OwlTest has successfully assessed your test cases, you will see the message TEST CASES successfully assessed.. Following this message is a seven-digit number that you should enter in the form below.
  
### Answer:
    
