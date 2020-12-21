# Blog Entry #7

## Concept of Abstract Reduction Systems

### What is an Abstract Reduction System?
An abstract reduction system (ARS for short) is a set of elements that we need to rewrite, and a relation, or a set of rules, that we can apply to the elements. These rules help us to simplify elements in an easier and faster format to process.

### How does an Abstract Reduction System work?
As stated above, an ARS contains a list of elements, such and *a, b,* and *c*, and a set of rules that apply to these elements. If given an ARS with the following starting condition, the rules can be used to simplify - or reduce - the starting condition until it has reached its normal form.  
_________________________________________________________________________________________________________________________________________________________________________________
**Bonus Terminology**

Normal Form - In this context, a Normal Form is when a set of elements cannot be reduced further using the given rules in an ARS. 

--> Notation - When writing the rules, an arrow --> is used to show that an element is being reduced.

[ ] Notation - Signifies that an element reduces to nothing
_________________________________________________________________________________________________________________________________________________________________________________

**Example ARS**

*Starting condition* - 

aaabbccc

*Rules* - 

bb --> [ ]

aa --> b

cc --> b

ac --> aa

Using the above starting condition and rules, we can reduce the starting condition to its normal form.

1. a(aa --> b)bbccc = abbbccc

*Explaination: We can reduce an aa in the starting condition to a b which results in abbbccc*

2. abbb(cc --> b)c = abbbbc

*Explaination: We can do the same things to the c's and reduce cc to b*

3. a(bb --> [ ])bbc = abbc

*Explaination: bb reduces to nothing*

4. a(bb -->)c = ac

*Explaination: We can reduce bb to nothing once more*

5. ac --> aa

*Explaintion: ac reduces to aa. Check to see if this is its normal form. (Hint: keep going!)*

6. aa --> b

*Explaination: aa can be reduced to b. A single b can not be reduced any further, so we have reached its normal form!*

You may notice that there are many different ways you can do these steps. You can apply the rules in any order that you would like and still reach the same normal form! This means that the ARS system is **confluent**. If a system is confluent, it means that no matter how you apply the rules to the starting condition, you will always reach the same normal form. Further, this system is also **terminating**. This means that the system reaches a normal form and does not get stuck cycling between two rules. This is best explained in the example below.

**Non-Terminating ARS Example**

*Starting condition* - 

aaabbccc

*Rules* - 

bb --> [ ]

aa --> b

cc --> b

ac --> aa

b --> aa

As you can see, this ARS follows the same rules as the one in the example above with the exception of one additional rule. When you reduce the system (following the same steps as above) you reach the step where
aa --> b
 
However, unlike the system above, we are not finished. Because of the new additional rule, b can also be reduced.
 
b --> aa
 
This results in an endless cycle because of how aa --> b and b --> aa. This means that the system is non-terminating and will never reach its normal form!
 
_________________________________________________________________________________________________________________________________________________________________________________
**Definition Recap**
Confluence - The ARS reaches a unique normal form and is terminating 
Terminating - The ARS reaches a normal form and can not be reduced any further
Non- Terminating - The ARS does not have a normal form and can continuously be reduced forever
_________________________________________________________________________________________________________________________________________________________________________________


### This blog contains just the basic concepts of an ARS system without much of the discrete notation. This is because, for whatever reason, the notation distracted me from the overall basic concepts that comprised an ARS system. This helped me to figure out what the basic concepts were and then I was able to add in the notation later.






