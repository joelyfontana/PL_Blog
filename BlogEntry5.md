# Blog Entry #5 
## Haskell Tips and Tricks

**1. Top tip for Haskell - Get a code editor that you can easily install Haskell extensions to help you write and debug your code. Visual Studio Code is my favorite for this because it is very easy to use, contains multiple extensions for Haskell, and has github integration so you can push straight to your github. In Visual Studio Code, the extensions I found the most helpful are Haskell, Haskell Syntax Highlighting, Haskelly, and Simple GHC (Haskell) Integration. Together, these extensions help my code to be more readable with varying colors, suggest type declarions, and let you know if there is a problem with your code before you compile it.**
2. You can use **undefined** to define a function before it is implemented 
```                                 
add :: Int -> Int -> Int
add = undefined            
```
So after it is implemented, the function can look like this:
```
add :: Int -> Int -> Int
add = \x y -> x + y
```
3. Use pattern matching - this is helpful in developing simple declarative command line applications
4. If you are not using a code editor like Visual Studio, importing Debug.Trace is super helpful in helping you to debug your code
5. Haskell is much more math based than other languages so before you write a function, write out the mathimatical steps first! After you have done that, your code is mostly done and just convert it into Haskell syntax
6. Remember to use a capital letter O instead of 0 when you are representing 0 as a Natural Number so you do not confuse the compiler (examples below).
```
-- Example using O -- O is a natural number
subtr :: NN -> NN -> NN
subtr O n = O
subtr n O = n
subtr (S n) (S m) = subtr n m

--Example using both O and 0. 0 is needed in this example because it is of type Int not NN
nn2int :: NN -> Int
nn2int O = 0
nn2int (S(n)) = 1 + (nn2int n)
```
7. Unless you are using an if statement or another type of statement in your function, every line in your function must begin with the name of the function so the compiler knows what function your code belongs in
```
--Every line in this function begins with the function name addP so the compiler can tell it is all one function
addP :: PN -> PN -> PN
addP I n = (T n)
addP (T n) m = T (addP n m)

--However, when you have a statement and your code is indented, you do not need to begin the line with the function name because the compiler knows it is all the same function.
gcdN :: NN -> NN -> NN
gcdN O O = O
gcdN n m = if less n m then gcdN m n
    else if modN n m == O then m
    else gcdN m (modN n m)
```
**List is subject to change and increase as I continue to learn and understand Haskell Better**


