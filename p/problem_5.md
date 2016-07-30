# Problem 5
Elm provides the function ```List.reverse``` to reverse the order of elements in a list. See if you can implement it.

##Example
```
myReverse [1..4] == [4, 3, 2, 1]
```

## Unit Test
```elm
import Html exposing (text)
import List 


myReverse : List a -> List a
myReverse xs =
    -- your implementation here
    []

main =
    text
        (if (test) then
            "Your implementation passed all tests."
         else
            "Your implementation failed at least one test."
        )


test : Bool
test =
    List.all ((==) True)
        [ myReverse [1..4] == [4, 3, 2, 1] 
        , myReverse [2, 1] == [1, 2] 
        , myReverse [1] == [1] 
        , myReverse [] == [] 
        , myReverse [ 'a', 'b', 'c' ] == [ 'c', 'b', 'a' ]
        ]
        
```

## Hints
1. Use a fold, passing it a function that takes and element, and returns a list. 

[Solutions](problem_5_solutions.md)