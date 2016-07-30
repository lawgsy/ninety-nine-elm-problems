# Problem 1 Solutions

###Solution 1:
Recursive search for the last element

```
last : List a -> Maybe a
last xs = 
  case list of
    [ ] -> Nothing
    [a] -> Just a
    y::ys -> last ys
```
###Solution 2:
Reverse and take the head.
```
last : List a -> Maybe a
last xs = 
   List.reverse xs |> List.head
```
[Back to Problem 1](problem_1.md)