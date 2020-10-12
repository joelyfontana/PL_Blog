# Blog Entry #4
## Haskell vs C++

Overall, switching from an Imperiative programming language like C++ to Haskell (a functional programming language) was initially very difficult and confusing. Now instead of simply declaring a function and being able to write both in and outside of it, we are limited to only working with in functions. At first I struggled with both syntax and concepts within Haskell. Instead of declaring a function once in C++, I now had to begin each line within the function with the function name so the compiler understood that it was all one function. Further, Haskell is much more math based than other languages. At first I thought this was going to be a major issue as math is not my strongsuit, but so far is has turned out to be an advantage. While C++ code can become long-winded and confusing, I can quickly write out the steps for the math problem I need to compute and convert it to a  Haskell function. An example of when I did this is when I had to write the function in fractions.hs to add two fractions together. My first approach to solving this problem was to write out the mathimatical steps for adding fractions together.

1. multiply the numerators with the opposite denominator
2. multiply denominators together
3. rewrite fractions
4. add fractions together
5. simplify if needed

I took these steps and converted them step by step into Haskell to give me a starting point. From there, I filled in the missing syntax needed for Haskell and tested my function. The resulting function is below:
```
-- add fractions
-- recall from school how to add fractions
addF :: Frac -> Frac -> Frac
--3/2 + 1/4
addF (nn, nd) (mn, md) = 
 --multiply the two denominators together (already a positive num)
    let comD = (multP nd md)
        -- multiply the numerators by the opposite denominator
        numer1 = (mult nn (p2n md))
        numer2 = (mult mn (p2n nd))
        --add the numerators together
        numerator = (add numer1 numer2)
        -- get the greatest common denominator to divde by to simplify the fraction
        gDom = (gcdN numerator (p2n comD))
            --(gcdN (p2n nd) (p2n md))
        -- simplify using the greatest common divisor
        in (divide numerator gDom, n2p(divide (p2n comD) gDom))
```        
However, 

