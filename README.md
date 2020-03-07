# WQU-Miniprojects
Solutions to WQU Unit 1 Miniprojects

# IN Miniproject

Problem 1

Compute the five smallest positive even numbers. Provide these in a list. In this case, the answer is a fixed value, so you may compute (or hard-code) the answer and submit it. Note that we have provided a "dummy solution" below. This dummy solution illustrates the correct format of the solution (i.e. a list of 5 numbers). If you are encountering an error when you try to submit a solution to the grader, double check that your answer has the same structure as the dummy solution.

even_numbers = [2,4,6,8,10] * 5
even_numbers = [2,4,6,8,10]
en = [x for x in range(2,11,2)]

Problem 2

Define a function that accepts a list (called numbers below) as input and return a list where each element is multiplied by 10. The grader will supply the argument numbers to the function when you run the grader.score.in__problem2 method below. In this case, you need to write a function that will work for arbitrary input. Before submitting your function to the grader, you may want to check that it returns the output that you expect by evaluating code similar to the following:

test_numbers = [1, 2, 3]
mult(test_numbers)

def mult(numbers):
    return [n*10 for n in numbers] 
    print(mult((1,2,3)))
    [10, 20, 30]

Exercise 1: mersenne_numbers

A Mersenne number is any number that can be written as 2𝑝−1 for some 𝑝. For example, 3 is a Mersenne number (22−1) as is 31 (25−1). We will see later on that it is easy to test if Mersenne numbers are prime. Write a function that accepts an exponent 𝑝 and returns the corresponding Mersenne number.

def mersenne_number(p):
    return 2**p-1
    
Mersenne numbers can only be prime if their exponent, 𝑝, is prime. Make a list of the Mersenne numbers for all primes 𝑝 between 3 and 65 (there should be 17 of them). Hint: It may be useful to modify the is_prime and get_primes functions from the Program Flow notebook for use in this problem.

# we can make a list like this
my_list = [0, 1, 2]
print(my_list)
[0, 1, 2]

# we can also make an empty list and add items to it
another_list = []
print(another_list)
for item in my_list:
    another_list.append(item)
print(another_list)
[]
[0, 1, 2]

def is_prime(number):
    """Accepts an integer and checks if it's prime or NOT. 
    Returns True if it is or False if it is NOT"""
    if number < 2:
        return False

    for factore in range(2, number):
        if number % factore == 0:
            return False

    return True 

def get_primes(n_start, n_end):
    return (n for n in range(n_start, n_end) if is_prime(n))

The next cell shows a dummy solution, a list of 17 sevens. Alter the next cell to make use of the functions you've defined above to create the appropriate list of Mersenne numbers

mersennes = [mersenne_number(p) for p in get_primes(3,65)]
