# Problem 19

Rotate a list ```n``` places to the left (negative values will rotate to the right). Allow rotations greater than the list length. 

##Example
```
[rotate [1..10] 3, rotate [1..10] 11] == 
  [ [4, 5, 6, 7, 8, 9, 10, 1, 2, 3]
  , [2, 3, 4, 5, 6, 7, 8, 9, 10, 11]
  ]
```

## Unit Test
```
import Html exposing (text)
import List


rotate : List a -> Int-> List a
rotate list rot =
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
        [ ( rotate [1, 2, 5, 5, 2, 1] 3, [5, 2, 1, 1, 2, 5] )
        , ( rotate [1..10] 13, [4, 5, 6, 7, 8, 9, 10, 1, 2, 3])
        , ( rotate [1..5] 1, [2, 3, 4, 5, 1])
        , ( rotate [1..5] 0, [1, 2, 3, 4, 5])
        , ( rotate [1..5] -1, [5, 1, 2, 3, 4])
        , ( rotate [1..5] -6, [5, 1, 2, 3, 4])
        , ( rotate [1..5] 3, [4, 5, 1, 2, 3])
        ]
        && List.all (\(result, expect) -> result == expect)
            [( rotate ["1", "2", "3", "4"] 1, ["2", "3", "4", "1"])]
```

## Hints

##Solutions 
[Solutions](problem_19_solutions.md)