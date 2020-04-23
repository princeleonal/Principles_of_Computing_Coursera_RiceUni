# Question 1: 
  Enter the type of the Python expression 3.14159.
  
### Answer: 
    Float
  
----
# Question 2:
  An if statement can have at most how many else parts?
  
### Answer:
    1

----
# Question 3: 
  Consider the following Python code snippet.Enter the value returned by Python after evaluating the expression clock_helper(90).
        
    def clock_helper(total_seconds):
     """
     Helper function for a clock
     """
     seconds_in_minute = total_seconds % 60
        
### Answer:
    None

----
# Question 4:
  In Python, what character always appears at the end of the line before the start of an indented block of code?
  
### Answer:
    ":"
  
----
# Question 5:
  Which of the following expressions returns the last character in the non-empty string my_string?
  
### Answer:
    my_string[-1]
  
----
# Question 6:
  What is the primary difference between a list and a tuple?
  
### Answer:
    Lists are mutable.Tuples are immutable.
  
----
# Question 7:
  Consider the following snippet of Python code. What is the value of val2[1] after executing this code?
  
    val1 = [1, 2, 3]
    val2 = val1[1:]
    val1[2] = 4
    
### Answer:
    3
  
----
# Question 8:
  Which of the following Python expressions is a valid key in a Python dictionary?
  
### Answer:
    False,""
  
----
# Question 9:
  Write a function in Python that takes a list as input and repeatedly appends the sum of the last three elements of the list to the end of the list. Your function should loop for 25 times.

### Code:
    def appendsums(lst):
    sum = 0
    for i in range(25):
        sum = lst[len(lst) -1] + lst[len(lst) -2] + lst[len(lst) -3]
        #print sum
        lst.append(sum)
    return lst

    sum_three = [0, 1, 2]
    appendsums(sum_three)
    print sum_three[10],print sum_three[20]
    
    OUTPUT: 230 101902
    
### Answer:
    101902
  
----
# Question 10:
  Complete the following class definition.
  
    class BankAccount:
    """ Class definition modeling the behavior of a simple bank account """

    def __init__(self, initial_balance):
        """Creates an account with the given balance."""
        …
    def deposit(self, amount):
        """Deposits the amount into the account."""
        …
    def withdraw(self, amount):
        """
        Withdraws the amount from the account. Each withdrawal resulting 
        in a negative balance also deducts a penalty fee of 5 dollars
        from the balance.
        """
        …
    def get_balance(self):
        """Returns the current balance in the account."""
        …
    def get_fees(self):
        """Returns the total fees ever deducted from the account."""
        …
        
  The deposit and withdraw methods each change the account balance. The withdraw method also deducts a fee of 5 dollars from the balance if the withdrawal (before any fees) results in a negative balance. Since we also have the method get_fees, you will need to have a variable to keep track of the fees paid.The Test case given below should print the values 10 and 5, respectively, since the withdrawal incurs a fee of 5 dollars.

    my_account = BankAccount(10)
    my_account.withdraw(15)
    my_account.deposit(20)
    print my_account.get_balance(), my_account.get_fees()
  
  Copy-and-paste the following much longer test. What two numbers are printed at the end? Enter the two numbers, separated only by spaces.
  
    my_account = BankAccount(10)
    my_account.withdraw(5)
    my_account.deposit(10)
    my_account.withdraw(5)
    my_account.withdraw(15)
    my_account.deposit(20)
    my_account.withdraw(5)
    my_account.deposit(10)
    my_account.deposit(20)
    my_account.withdraw(15)
    my_account.deposit(30)
    my_account.withdraw(10)
    my_account.withdraw(15)
    my_account.deposit(10)
    my_account.withdraw(50)
    my_account.deposit(30)
    my_account.withdraw(15)
    my_account.deposit(10)
    my_account.withdraw(5)
    my_account.deposit(20)
    my_account.withdraw(15)
    my_account.deposit(10)
    my_account.deposit(30)
    my_account.withdraw(25)
    my_account.withdraw(5)
    my_account.deposit(10)
    my_account.withdraw(15)
    my_account.deposit(10)
    my_account.withdraw(10)
    my_account.withdraw(15)
    my_account.deposit(10)
    my_account.deposit(30)
    my_account.withdraw(25)
    my_account.withdraw(10)
    my_account.deposit(20)
    my_account.deposit(10)
    my_account.withdraw(5)
    my_account.withdraw(15)
    my_account.deposit(10)
    my_account.withdraw(5)
    my_account.withdraw(15)
    my_account.deposit(10)
    my_account.withdraw(5)
    print my_account.get_balance(), my_account.get_fees()
  
### Code:
    class BankAccount:
    balance = 0
    fee = 0
    def __init__(self, initial_balance):
        """Creates an account with the given balance."""
        self.balance = initial_balance
    def deposit(self, amount):
        """Deposits the amount into the account."""
        self.balance = self.balance + amount
    def withdraw(self, amount):
        """
        Withdraws the amount from the account.  Each withdrawal resulting in a
        negative balance also deducts a penalty fee of 5 dollars from the balance.
        """
        if self.balance - amount < 0:
            self.balance = self.balance - amount -5
            self.fee = self.fee + 5
        else:
            self.balance = self.balance - amount
    def get_balance(self):
        """Returns the current balance in the account."""
        return self.balance
    def get_fees(self):
        """Returns the total fees ever deducted from the account."""
        return self.fee
        
    my_account = BankAccount(10)
    my_account.withdraw(5)
    my_account.deposit(10)
    my_account.withdraw(5)
    my_account.withdraw(15)
    my_account.deposit(20)
    my_account.withdraw(5) 
    my_account.deposit(10)
    my_account.deposit(20)
    my_account.withdraw(15)
    my_account.deposit(30)
    my_account.withdraw(10)
    my_account.withdraw(15)
    my_account.deposit(10)
    my_account.withdraw(50) 
    my_account.deposit(30)
    my_account.withdraw(15)
    my_account.deposit(10)
    my_account.withdraw(5) 
    my_account.deposit(20)
    my_account.withdraw(15)
    my_account.deposit(10)
    my_account.deposit(30)
    my_account.withdraw(25) 
    my_account.withdraw(5)
    my_account.deposit(10)
    my_account.withdraw(15)
    my_account.deposit(10)
    my_account.withdraw(10) 
    my_account.withdraw(15)
    my_account.deposit(10)
    my_account.deposit(30)
    my_account.withdraw(25) 
    my_account.withdraw(10)
    my_account.deposit(20)
    my_account.deposit(10)
    my_account.withdraw(5) 
    my_account.withdraw(15)
    my_account.deposit(10)
    my_account.withdraw(5) 
    my_account.withdraw(15)
    my_account.deposit(10)
    my_account.withdraw(5) 
    print my_account.get_balance(), my_account.get_fees()
    
    OUTPUT : -60, 75
    
  ### Answer:
      -60 75
