# Problem 62

a) Count the internal nodes (those that have non-empty subtrees) of a binary tree.

```
import Html exposing (text)

type Tree a
    = Empty
    | Node a (Tree a) (Tree a)

aTree = Tree 1 (Tree 2 Empty (Tree 4 Empty Empty))
                 (Tree 2 Empty Empty)

countInternalNodes : Tree a -> Int 
countInternalNodes tree = 
-- your implementation goes here

main = 
  text 
  <| toString 
  <| countInternalNodes aTree   
  
```
Result
```
2
```

b) Extract the internal nodes (those that have non-empty subtrees) of a binary tree into a list.

```
import Html exposing (text)

type Tree a
    = Empty
    | Node a (Tree a) (Tree a)

aTree = Tree 1 (Tree 2 Empty (Tree 4 Empty Empty))
                 (Tree 2 Empty Empty)

internalNodes : Tree a -> Int 
internalNodes tree = 
-- your implementation goes here

main = 
  text 
  <| toString 
  <| internalNodes aTree   
  
```
Result
```
[1,2]
```