# Blog Entry #9

## Most Useful Extensions of Lambda Calculus

### Introduction
Overall, Lambda Calculus is a very flexible and versile language. It allows us to "extend" the langauge, or add features to the language that help us create a binding mechanism for variables so we do not have to redefine them my hand each time. This is also known as **Higher Order Abstract Syntax** (HOAS for short). 

___________________________________________________________________________________________________________________________________________________________________________________
**Definition**

Higher Order Abstract Syntax is a technique for the representation of abstract syntax trees with languages that have variable binders. HOAS can be used in math where a graphs edges are binding sites associted with variables. It can also be used with de Burjin indeces and logical frameworks. 
___________________________________________________________________________________________________________________________________________________________________________________

### Syntax of Lambda Calculus 
Given the function below, we need to be able to turn it into a more readable function. We can do this by rearranging the function and using Let.

_________________________________________________________________________________________________________________________________________________________________________________
**Let Definition** - 
Let is a easier and cleaner way of defining whenever we have a program.
So if we have 
```
let x = element1 in element2
```
it means the same thing as 
```
(\x . element2) element1
```
_________________________________________________________________________________________________________________________________________________________________________________

```
(\plus . \two . \one . plus two one) 
(\m.\n.\f.\x. m f (n f x)) 
(\f.\x. f (f x)) 
(\f.\x.f x)
```
First, we need to divide this function up into our three parts: the plus, two, and one. We can see that the plus is the second line - because it is a combination of the bottom two lines - while one and two are the third and forth lines. Further, we need to divide up the first line into two programs by splitting it at the plus after the lambda arguments. This can be moved to the end of the function.
```
plus = (\m.\n.\f.\x. m f (n f x))
two = (\f.\x. f (f x)) 
one = (\f.\x.f x)
plus two one
```
From here, we need to start each program with let. However, the last line, plus two one, does not start with let because it is not a program.
```
let plus = (\m.\n.\f.\x. m f (n f x))
let two = (\f.\x. f (f x)) 
let one = (\f.\x.f x)
plus two one
```
Finally, we also need to add *in* between programs to make it more readable and grammatically correct.
```
let plus = (\m.\n.\f.\x. m f (n f x))
in
let two = (\f.\x. f (f x)) 
in
let one = (\f.\x.f x)
in 
plus two one
```
This use of *let* and *in* help to bind the function together to make it more readable and more abstract.
## Recursion 
If we have a function that is recurvsive, the syntax is slightly different. Instead of using *let* before the program, you would use *let rec* in front of the program that you want to use recursion in. This is shown in the example below.
```
let rec minus_check = \w.\x. 
if w = 0 then S 0 
else if w = x then 0 
else minus_check (minus_one w) (x)
```
In this function, it is comparing two inputs, w and x. If w is equal to 0 it returns 1 but if w is equal to x it returns 0. However, if neither of these conditions are met, it calls the outside function minus one to subtract w from x. After it has done this, it uses recursion to call minus_check again to see if the new w and x now meet the conditions. This recursion is when the program needs to begin with let rec and not just with let. 


