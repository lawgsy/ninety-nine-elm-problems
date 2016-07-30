# Problem 15

Repeat each element of a list a given number of times.

##Example
```
repeatElements [1, 2, 3, 3] 3 == [1, 1, 1, 2, 2, 2, 3, 3, 3, 3, 3, 3]
```

## Unit Test
```
import Html exposing (text)
import List


repeatElements : List a -> Int -> List a
repeatElements list =
    -- your implementation goes here
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
    List.all (\(result, expect) -> result == expect)
        [ ( repeatElements [1, 2, 5, 5, 2, 1] 2, 
            [1, 1, 2, 2, 5, 5, 5, 5, 2, 2, 1, 1] )
        , ( repeatElements [1, 2] 4, [1, 1, 1, 1, 2, 2, 2, 2])
        , ( repeatElements [] 4, [])
        , ( repeatElements [1, 2] 0, [])
        , ( repeatElements [1, 2] (-1), [])
        , ( repeatElements [1] 40, [1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1])
        ]
        && List.all (\(result, expect) -> result == expect)
            [( repeatElements ["1", "2"] 4, ["1", "1", "1", "1", "2", "2", "2", "2"])]
```

## Hints
1. Do I need to *repeat* myself? "Recurse!"
##Solutions 
[Solutions](problem_15_solutions.md)