# Blog Entry #1
## Experience with Haskell Recursion in Functional Programming

### Installing Haskell

Installing Haskell was initially confusing but overall not very challenging. First, I went to the Haskell homepage to download it for windows. However, before I could install Haskell, the steps on Haskells website said to configure chocolatey first. I followed that link and download chocolatey and downloaded it. Then I was able to go back to the Haskell website and download Haskell as well. From there I copied the commands from the webpage into the command prompt and everything installed fairly easily. I did run into the issue where everything installed perfectly excpet for Cabal, which threw an error. I was worried that this would pose an issue in the future so I made a note of it, but so far I have not had any problems.  

### Coding in Haskell
Unfortunately, figuring out how to write code in Haskell and its syntax was not as easy as installing it. While I understood the basic example function we did in class, 
```
len [] = 0
len (x:xs) = 1 + len xs
```
I struggled to apply this example to the homework. To begin, my main issue was I did not know how to declare a function in Haskell. After rereading the notes and googling it, I finally discovered that I needed to put 
```
len :: Num b => [a] -> b
```
before my len function to decalre it. However, my confusion as to what that meant did not clear until I attempted the homework. In my first attempt in making a select_evens function, I did everything incorrect. I tried to copy the function declaration from the len function and creating a new variable within the function (see code below).
```
select_evens :: Num a => [a] -> Integer
select_evens [] = 0
evens_list = []
    if(length(select_evens)) `mod` 2 == 0
        then head(select_evens) : evens_list
```
With this function, I got endless errors and evntually gave up. When we went over the solutions in class, however, Haskell's syntax suddenly made much more sense. I learned that the function declaration consists of the type of your input pointing to the type of your output. Further, I learned that in order for the compiler to know that it is all one function, every line has to start with the function name. Lastly, I understood that when writing my function, I needed to start with the base cases and then use those base cases to help me with my recursion in the final case. Seeing a working example (see code below) that utilized all of these aspects really helped me understand how Haskell works and how I should write my code. 
```
--Credit: Dan's solution from class
-- Integer Input to Interger output
select_evens :: [Int] -> [Int]
--base cases
select_evens [] = []
select_evens [x] = []
--final case using recusion!
select_evens (x : y : ys) = y : select_evens (ys)
```
Once I learned these main componets, I was able to complete the rest of the homework with minimal difficulty and fully understand the rest of the lesson. Saying this, recursion is still a big struggle for me. I continuously put it in the wrong spot and do not fully understand why I am using it yet. However, I'm hoping it will come more naturally the more I continue to use it. 
   
