# Blog Entry 2
## Abstract Syntax in Haskell

### Writing an Abstract Calculator
At first, the idea of creating an abstract calculator was very confusing to me. Of course I understood the calculator aspect of adding together two numbers, but I was very confused when we could not add actual numbers together. Instead, to get the program to work, I had to use (S O) - the successor of zero - to represent 1. This concept of using letters to represent numbers and having to start from 0 was much harder for me to understand and was not solidified until the fractions.hs assignment. In this assignment, we had to use both abstract numbers and recursion to make a calculator. I expected this to be extremely difficult as I did not really understand either but it turned out to be easier than expected. We started with the addition function which was very different then the functions we had previously made. Instead of declaring the function with an integer type, we had to make a function that worked with natural numbers. We also had to take in two inputs. Using the steps that I learned from the previous functions, I made a base case after declaring the function and then worked on the main case (see below).
```
add :: NN -> NN -> NN
add O n = n
add (S n) m = S (add n m)
```
Since this function only has one base case, I did not realize that the order of the variables in the base case does matter. I discovered this in the divide function. In the base cases for the divide function I accidentlly switched the variables in the third case. Instead of the correct code below, my third case read: divide (S(O)) n = n. This did not throw any errors and worked initially, but caused many problems later on. This is because my code was saying 1 divided by n is equal to n, which is incorrect. Instead, I had to change it to read n divided by 1 is still n, which is the correct base case. However, because I had this issue, I was much more careful about how I wrote my base cases for future functions and made sure that my variables were in the correct order.
```
divide :: NN -> NN -> NN
divide O n= O
divide n O = O --can not divide a number by 0
divide n (S (O)) = n -- make a case for 1?
```
### General issues
Overall, the fractions.hs assignment really helped me to understand both Haskell syntax and abstract syntax. However, before this happened, I ran into many (many) issues. For me, the easiest way to figure out the steps to write the function was to physically write out the steps needed (with concrete numbers) to solve the function. Unfortunately, this did not help me figure out how to write these steps in Haskell. As mentioned above, I figured out the functions type for the declaration and started with the base cases. For the recursive case however, I quickly had to learn how to do if statements properly in Haskell. Unlike c++, when writing an If statement in Haskell, there are no parenthesis and there has to be a then statement following. This then statement is in addition to an else statement and is not a substitute! Further, I struggled with the minor syntax differences. I always wrote 0 instead of O so the compiler did not understand what I was doing. Additionally, when writing the abstract syntax, especially when testing, my parenthesis were in the wrong positions so I would get the error saying that I did not have as many variables as I should. I quickly learned that this error meant to check my testing syntax and not my actual function. However, when we got to the functions dealing with both positive and natural numbers, I was very confused at first. Instead of starting at zero, now we had to start at 1. Surprisingly, this shift to using both positive and natural numbers somehow helped my fully understand the abstract syntax. By the time we worked our way to the fraction functions that used both, I was comfortable switching between the two. I still struggled with testing the functions, but I was now able to identify if my errors were a code problem or a syntax problem.



 
 
