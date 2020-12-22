# Blog Entry #9

## Extensions of Lambda Calculus

### Introduction
Overall, Lambda Calculus is a very flexible and versile language. It allows us to "extend" the langauge, or add features to the language that help us create a binding mechanism for variables so we do not have to redefine them my hand each time. This is also known as **Higher Order Abstract Syntax** (HOAS for short). 

___________________________________________________________________________________________________________________________________________________________________________________
**Definition**

Higher Order Abstract Syntax is a technique for the representation of abstract syntax trees with languages that have variable binders. HOAS can be used in math where a graphs edges are binding sites associted with variables. It can also be used with de Burjin indeces and logical frameworks. 
___________________________________________________________________________________________________________________________________________________________________________________

### Syntax of Lambda Calculus 
Given the function below, we need to be able to turn it into a more readable function. We can do this by rearranging the function and using Let.

___________________________________________________________________________________________________________________________________________________________________________________
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
___________________________________________________________________________________________________________________________________________________________________________________
```
(\plus . \two . \one . plus two one) 
(\m.\n.\f.\x. m f (n f x)) 
(\f.\x. f (f x)) 
(\f.\x.f x)
```
