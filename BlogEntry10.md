# Blog Entry #10

## Introduction to De Brujin Indeces and Notation

### What is the De Brujin Index?
To begin, the De Brujin Index is a tool used to represent terms in lambda calculus without having to name the bound variables. Basically, it is a way to avoid the interaction between free and bound variable names in the substitution operator by picking a representation for the expressions that doesn't have a name.
_________________________________________________________________________________________________________________________________________________________________________________
**Bonus Definition**
Bound variable - a bound variable is just a pointer to the λ that binds it. So if we have the expression 
```
λ x. λ y. y x 
```
y points to the first λ  while x points to the second λ.
_________________________________________________________________________________________________________________________________________________________________________________

### De Brujin Notation 
In De Brujin Notation, variables in lambda calculus are represented by integers *n* that refer to the index of thier binder while the lambda abstractions are represented by λ.e. This way the lambda abstractions remain nameless. So if we are given the following expression in lambda calculus: 
**Example 1**
```
λx.x 
```
it becomes
```
λ.0
```
in De Brujin notation.
This is because the lambda abstraction *λx* must be changed to *λ* to help it remain nameless. Further the *x* becomes 0 because *x* is an integer that represents the index of its bound variable, which is 0.

**Example 2**
The following is a slightly more complex example that follows the same logic as the example above. 
```
λx.λy.x
```
in lambda calculus, it would look like the following with De Brujin notation
```
λ.λ.1
```
This is because the lambda abstractions, *λx.λy.*, are changed to just *λ.λ.* to prevent them from 1) being bound variables and 2) being named. Further, the *x* becomes a 1 because x represents the integer of its index, which is 1.

**More Examples**
These examples all follow the same format as the examples listed above. They are given to help further one's understanding of De Brujin Notation and to help one notice the patterns between all of the examples.

```
λz.z --> λ.0

λx.λy.λs.λz.x s (y s z) -->  λ.λ.λ.λ.3 1 (2 1 0)

(λx.x x) (λx.x x) --> (λ.0 0) (λ.0 0)

(λx.λx.x) (λy.y) --> (λ.λ.0) (λ.0)
```

