# Blog Entry #3
## Functional vs. Imperiative Programming 

### What Functional and Imperiative Programming Are
Functional programming was created to support a purely functional approach to problem solving and is a form of declarative programming. This means that one must break their problem up into a function or several functions to solve it. In Imperiative programming, on the other hand, a programmer must write out the specific steps the computer must take to solve a problem. Knowing this, it makes sense that we are only allowed to have functions in Haskell and can not work outside of them like you can in C++, C#, and Java. 

### Key Differences
While these definitions help me to understand the key differences, breaking down the key differences between the two languages greatly helped me to understand them more. To begin, in imperative programming, both state changes and order of execution are very important. However, in functional programming neither is important. Further, imperiative programming relies on loops, conditionals, and function calls whereas functional programming relies on function calls (including recursion). Lastly, Imperative programming has structures or classes while functional programming has first class objects and data collections. 

### Imperative Code Example in C#
```
List<string> select_evens(List<string> strList)
{
 for(int i=0; i < strList.length(); ++i)
  {
    if(i%2 == 0)
      { 
         evensList.add(strList.get(i));
      }
     return evensList;
  }
}
```
### Functional Code Example in Haskell
```
select_evens :: [Int] -> [Int]
select_evens [] = []
select_evens [x] = []
select_evens (x : y : ys) = y : select_evens (ys)
```


