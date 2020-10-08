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
before my len function to decalre it. 
