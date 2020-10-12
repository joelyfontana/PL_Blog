# Blog Entry #4
## Haskell vs C++

Overall, switching from an Imperiative programming language like C++ to Haskell (a functional programming language) was initially very difficult and confusing. Now instead of simply declaring a function and being able to write both in and outside of it, we are limited to only working with in functions. At first I struggled with both syntax and concepts within Haskell. Instead of declaring a function once in C++, I now had to begin each line within the function with the function name so the compiler understood that it was all one function. Further, Haskell is much more math based than other languages. At first I thought this was going to be a major issue as math is not my strongsuit, but so far is has turned out to be an advantage. While C++ code can become long-winded and confusing, I can quickly write out the steps for the math problem I need to compute and convert it to a  Haskell function. An example of when I did this is when I had to write the function in fractions.hs to multiply two numberss together. My first approach to solving this problem was to write out the mathimatical steps for multiplying two numbers together as listed below.

1. multiply n-1 and m
2. add m to the multiplied value

I took these steps and converted them step by step into Haskell to give me a starting point. From there, I filled in the missing syntax needed for Haskell and tested my function. The resulting function is below:
```
-- multiplication
mult :: NN -> NN -> NN
mult O n = O
mult (S O) n = n
mult (S n) m = add m (mult n m)
```        
However, in C++, writing this function would be much more confusing for me as the steps would not be the same as the mathimatical steps. First, I had to define Natural numbers in a class and make a constructor for the successor value. Next, I had to make an add function to be called later in the multiply function. Lastly, I had to call the multiply function in the main in order to run in with values. In Haskell, it is much easier to define a natural number as it is done in 1 line: data NN = O | S NN. Further, Haskell looks much cleaner than C++ and it is much easier to see what is happening.
```
Pseudo code for Multiplying Natural numbers
//definition for a natural number
class NN
{
    char zero = 'O';
    NN* next;

//constructor
    NN(NN* _next)
    {
        next = _next;
    }
};

NN* Add(NN* num1, NN* num2)
{
    //insert code to add natural numbers
};
NN* Multiply(NN* num1, NN* num2)
{
    //insert code to multiply two natural numbers using the add function above
};

int main()
    {
        Multiply(2,4);
        return 0;
    }
```

