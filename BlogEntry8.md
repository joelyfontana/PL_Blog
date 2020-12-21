#Blog Entry #8

## Parsing Lambda Calculus

### Background of Lambda Calculus
Lambda calculus was created in the 1930's by Alonzo Church in order to study what functions were computable. Today, it is one of the simpliest programming languages but just as powerful as many modern day programming languages such as Java. In lambda calculus, programs are called lambda expressions (shortened to λexp). There are only three types of these programs in lambda calculus:

- **Abstraction**
If *e* is an expression containing *x*, it is written as *λx.e* because the program does not depend on *x* anymore and it is abstracted away.

- **Application**
In application, if there are two expressions, *e1* and *e2*, it is written as *e1e2* where the expression *e1* is applied to the arguemnt *e2*

- **Variable** - the basic programs. Typically a single letter such as *x* or *y*

### Syntax of Lambda Calculus
Before we can begin parsing lambda expressions, we must be able to simplify the syntax until it is a lambda program!
