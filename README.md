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
