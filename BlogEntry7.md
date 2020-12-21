# Blog Entry #7

## Abstract Reduction Systems

### What is an Abstract Reduction System?
An abstract reduction system (ARS for short) is a set of elements that we need to rewrite and a relation, or a set of rules, that we can apply to the elements. These rules help us to simplify elements in an easier and faster format to process.

### How does an Abstract Reduction System work?
As stated above, an ARS contains a list of elements, such and *a, b,* and *c*, and a set of rules that apply to these elements. If given an ARS with the following starting condition, the rules can be used to simplify - or reduce - the starting condition until it has reached its normal form.  
_________________________________________________________________________________________________________________________________________________________________________________
**Bonus Terminology**

Normal Form - In this context, a Normal Form is when a set of elements cannot be reduced further using the given rules in an ARS. 

--> Notation - When writing the rules, an arrow --> is used to show that an element is being reduced.

[ ] Notation - Signifies that an element reduces to nothing
_________________________________________________________________________________________________________________________________________________________________________________

**aaabbccc**

bb --> [ ]

aa --> b

cc --> b

ac --> aa

Using the above starting condition and rules, we can reduce the starting condition to its normal form.

1. a(aa --> b)bbccc = abbbccc
We can reduce an *aa* in the starting condition to a *b* which results in abbbccc
1. abbb(cc --> b)c = abbbbc
We can do the same things to the *c's* and reduce *cc* to *b*
1. 




