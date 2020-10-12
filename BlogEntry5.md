# Blog Entry #5
## help

### Haskell Tips and Tricks

1. You can use **undefined** to define a function before it is implemented 
```                                 
add :: Int -> Int -> Int
add = undefined            
```
So after it is implemented, the function can look like this:
```
add :: Int -> Int -> Int
add = \x y -> x + y
```
1. Use pattern matching - this is helpful in developing simple declarative command line applications
1. Use Debug.Trace to  
