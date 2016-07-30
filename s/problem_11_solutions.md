# Problem 11 Solutions

```
type RleCode a = Single a | Run Int a


rleEncode : List a -> List (RleCode a)
rleEncode list =
  convertSingles <|
    case list of 
      [] -> 
        []

      x :: xs ->
        rleEncode' (Run 0 x) list


rleEncode' : RleCode a -> List a -> List (RleCode a)
rleEncode' rle list =
  case rle of 
    Single x -> 
      []
    
    Run n x ->
      case list of 
        [] -> 
          [ rle ]
              
        hd :: tl -> 
          if hd == x then
            rleEncode' (Run (n+1) hd) tl
          else
            rle :: rleEncode' (Run 1 hd) tl
            

convertSingles : List (RleCode a) -> List (RleCode a)
convertSingles list = 
  case list of 
    [] ->
      []
      
    Run 1 x :: xs ->
      Single x :: convertSingles xs
      
    x :: xs ->
      x :: convertSingles xs
```